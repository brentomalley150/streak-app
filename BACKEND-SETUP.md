# SummerStreak Backend Setup (Firebase Realtime Database)

The dashboard works fully offline with localStorage. Firebase enables:
- **Real-time leaderboard updates** — friends' scores update instantly across devices
- **Cross-device admin** — Founders Hub shows every kid signed up, editable in one place
- **Stable identity per parent** — Google Sign-In replaces the old anonymous auth, so a parent has ONE Firebase UID forever (no more ghost duplicates when switching browsers)

## Architecture

- **Auth**: Google Sign-In (one Google account per parent → one stable UID)
- **Profiles**: Multiple kid profiles live under one parent's Google account in localStorage
- **Leaderboard key**: composite `{googleUid}_{profileId}` — so a parent with Declan AND Sophie gets two distinct leaderboard slots under the same Google account

## Firebase Console setup

### 1. Create the Firebase project (once)
1. https://console.firebase.google.com → **Add project** → name it `summerstreak` → continue without Analytics → **Create project**

### 2. Add a web app (once)
1. Project home → **`</>`** (web) icon → app nickname `SummerStreak Web` → **Register app**
2. Copy the `firebaseConfig` block — it's already pasted into `firebase-config.js` for the deployed site

### 3. Enable Realtime Database (once)
1. Sidebar → **Build → Realtime Database** → **Create Database** → US default → **Start in locked mode** → **Enable**
2. **Rules** tab → paste **exactly this** and **Publish**:

```json
{
  "rules": {
    "leaderboard": {
      ".read": "auth != null",
      "$entry": {
        ".write": "auth != null && ($entry.beginsWith(auth.uid) || root.child('admins').child(auth.uid).val() === true)"
      }
    },
    "weeklyHistory": {
      ".read": "auth != null",
      "$weekNum": {
        "$entry": {
          ".write": "auth != null && ($entry.beginsWith(auth.uid) || root.child('admins').child(auth.uid).val() === true)"
        }
      }
    },
    "weeklyWinners": {
      ".read": "auth != null",
      "$weekNum": {
        ".write": "auth != null && (!data.exists() || root.child('admins').child(auth.uid).val() === true)"
      }
    },
    "admins": {
      ".read": "auth != null && root.child('admins').child(auth.uid).val() === true",
      ".write": false
    }
  }
}
```

**What the new nodes do:**
- `weeklyHistory/{weekNum}/{leaderboardKey}` — every kid's device writes their current weekly stats here on every sync. Survives Monday rollover so winner can be computed from real data, not stale local cache.
- `weeklyWinners/{weekNum}` — write-once. First device to detect "last week is over" reads `weeklyHistory/{lastWeek}`, picks the top scorer, and locks them in. Subsequent writes are blocked by `!data.exists()`. Admins can overwrite if they need to correct a recorded winner.

The `$entry.beginsWith(auth.uid)` rule is what makes the new composite key safe: every leaderboard entry must start with the signed-in user's Google UID. A parent can write entries for all their kid profiles (different `_profileId` suffixes), but can't touch anyone else's slot.

### 4. Enable Google Sign-In (ONE-TIME, important!)
1. Sidebar → **Build → Authentication**
2. **Get Started** (if first time)
3. **Sign-in method** tab → **Add new provider** → **Google** → **Enable**
4. Set the project support email → **Save**

> 🔥 **If you skip this**: the dashboard will load but every sign-in attempt will fail with "auth-failed."

### 5. (One-time) Authorize the production domain
1. Authentication → **Settings** → **Authorized domains**
2. Add `beatthesummerslide.com` if it isn't already listed (localhost and `*.firebaseapp.com` are pre-authorized)

### 6. Grant yourself admin access (one-time, after first sign-in)
1. Open https://beatthesummerslide.com/admin.html
2. Click **Sign in with Google** → use your Gmail
3. Open browser DevTools console: paste `Backend.uid` → copy the printed UID
4. Firebase Console → Realtime Database → Data tab → Add child `admins/{your-uid}` with value `true`

That's it forever — your Google UID never changes, so admin access persists across every browser, every device, every "clear site data."

## What syncs to Firebase

The dashboard writes one record per kid profile to `/leaderboard/{googleUid}_{profileId}`:
```json
{
  "uid": "googleUid123",
  "profileId": "prof_1717000000_abc12",
  "leaderboardKey": "googleUid123_prof_1717000000_abc12",
  "ownerEmail": "parent@gmail.com",
  "name": "Declan O'Malley",
  "avatar": "👑",
  "theme": "chess",
  "points": 42,
  "rank": "Knight",
  "rankPiece": "♘",
  "booksFinished": 2,
  "totalMinutes": 145,
  "totalWords": 320,
  "currentStreak": 7,
  "lastSeen": 1716321234567
}
```

**Daily entries, parent PINs, prizes, prize-claim history, and goals are NOT synced** — those stay on the device. Only the data needed for the public leaderboard goes to Firebase.

## Migrating from anonymous auth (one-time cleanup)

If you upgraded from the previous anonymous-auth version, you'll have:
- Old `/leaderboard/{anonUid}` entries (ghosts) — safely orphaned, delete them in admin
- Old `/admins/{anonUid}` entries — won't grant admin access anymore (anonymous UIDs are different from Google UIDs)
- Re-add yourself as admin using step 6 above with your Google UID

## Cost

Firebase Realtime Database free tier ("Spark plan"):
- 1 GB storage
- 10 GB/month download
- 100 simultaneous connections

For 100 kids playing daily, expected usage is < 1% of the free tier. No credit card required. Past ~100 active families, sharded leaderboard refactor on the roadmap.

## Privacy & COPPA

The Google Sign-In flow uses the **parent's** Google account — kids under 13 should never enter their own. This is the foundation for COPPA compliance but does NOT yet satisfy COPPA on its own. Before opening to families you don't personally know:
- Verifiable parental consent screen at first sign-in
- Data deletion request handling
- Parent-only PII review

See the PRD's Phase 2 plan.

## Troubleshooting

| Symptom | Fix |
|---|---|
| Status says "auth-failed" | Enable Google Sign-In in Firebase Console → Authentication → Sign-in method |
| Sign-in popup blocked | Allow popups for beatthesummerslide.com, or it will fall back to redirect automatically |
| "Unauthorized domain" error | Add `beatthesummerslide.com` to Authentication → Settings → Authorized domains |
| Edit on admin.html fails "permission denied" | Your Google UID isn't in `/admins`. Repeat step 6. |
| Leaderboard never populates | Each kid profile syncs on first dashboard load after sign-in. Open dashboard.html while signed in. |
| Status stuck "checking-auth" | Hard refresh (Cmd-Shift-R) — usually a stale service worker |
