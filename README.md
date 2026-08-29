# Beat the Slide — public site

**https://beattheslide.com**

| Path | What it is |
|---|---|
| `/` | Landing page — `index.html` |
| `/app/` | **The live app** — a built copy of `streak-v2` |
| `/prototype.html` | Interactive prototype (concept demo) |
| `/story.html` | "How I vibe-coded a reading app for my 10-year-old" |

Everything here is **public**. Nothing founder-facing or internal belongs in
this repo — that lives in `beat-the-slide-hub` (private).

## Updating the app

`/app` is build output, not source. Never edit it by hand.

```bash
cd ~/Documents/streak-v2
npm run build

cd ~/Documents/streak-app
rm -rf app && mkdir app
cp -R ~/Documents/streak-v2/dist/* app/
rm -f app/assets/*.map          # don't ship source maps publicly
git add -A && git commit -m "Update app build" && git push
```

Source maps are stripped deliberately: they would expose the full TypeScript
source. The Firebase web API key in the bundle is public by design — it
identifies the project and authorises nothing. Security comes from the
Realtime Database rules, which live in `streak-v2/firebase.rules.json`.

## Where everything else lives

| What | Repo | URL |
|---|---|---|
| **App source** | `streak-v2` | — |
| **Founders hub** | `beat-the-slide-hub` (private) | https://brentomalley150.github.io/beat-the-slide-hub/ |
| **v1 app** — the live original | `declansummerlearning` (private) | https://beatthesummerslide.com |

## Before you add a page here

Would you be comfortable with a competitor, an investor, or a journalist
reading it? If not, it belongs in the hub repo.
