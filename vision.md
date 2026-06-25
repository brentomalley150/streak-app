# SummerStreak — Marketing + Year-Round Product Strategy

**Last updated:** June 2026 · Founder: Kate O'Malley · Strategy advisor: Brent O'Malley

---

## Part 1 — Social Media Marketing Plan

### Audience segments

| Segment | Why they care | Where they hang out |
|---|---|---|
| **PM-curious parents** | Loved the "vibe-coded by a dad" angle. Will share to inspire other parents/PMs. | LinkedIn, X, Substack, IndieHackers |
| **Parents of struggling readers** | Their kid is behind grade level. Need something that actually gets the kid to read. | Facebook parent groups, Reddit r/Parenting, school listservs, Nextdoor |
| **Ed-tech / EdReform community** | Interested in low-cost, parent-built tools. Could amplify. | X, EdSurge, LinkedIn ed-tech circles |
| **Curious onlookers (builders)** | Want to see how vibe-coding plays out longitudinally. Will follow your build log. | X, IndieHackers, ProductHunt, Hacker News |

The strongest organic flywheel: the **PM-curious parent** segment because they share. They're not your end users, but they spread the meta-story (parent + AI + child outcome) which drives the actual end users (parents of struggling kids) to you.

### Channel mix — priority order

**1. LinkedIn (highest leverage right now)**
Your existing PM network is the warmest audience. The vibe-coding case study lands here. Post a story-driven piece monthly with: (a) what shipped, (b) what kids did with it, (c) what the data says. End each with a soft CTA — "follow if you want the fall MAP score reveal."

**2. Substack (own the narrative long-form)**
Convert your story.html into a newsletter. One post per month is plenty. The September fall-score reveal is the headline post — build subscribers in the lead-up so it lands with an audience.

**3. X / Twitter (build in public micro-updates)**
Short, frequent. "Shipped X today, here's what Declan did with it." Visuals always. Tag the AI PM course cohort, tag Anthropic. Hashtags only sparingly: #VibeCoding, #BuildInPublic, #EdTech.

**4. Reddit (where your real users are)**
r/Parenting, r/HomeschoolRecovery (lots of struggling-reader parents), r/Education, r/ChatGPT (the meta-build angle resonates). Don't post as marketing — post as "I built this for my kid, here's the link, AMA." Mods are sensitive to promotional tone.

**5. TikTok / Instagram Reels (year 2 — if you have stomach for it)**
Most-different audience from the rest. Emotional 30-sec videos: kid's reaction to unlocking a prize, time-lapse of a fort being built for Reading Fort Week, before/after stats. Highest reach potential, highest production cost.

### 30 / 60 / 90 day plan

**Days 1-30 — Build the foundation**

- **Day 1:** Post the existing **Story page** to LinkedIn (with the link). Pin to your profile. Same content as a Substack post (gets you your first 50 subscribers from your network).
- **Week 1:** Twitter/X thread version of the same story (5-7 tweets). Tag @AnthropicAI, your AI PM course, a few ed-tech voices.
- **Week 2:** Reddit posts to 2-3 subs (r/Parenting, r/learnprogramming, r/ChatGPT). Lead with the kid story, not the tech.
- **Week 3:** Personal outreach — 20 DMs to PM friends, asking them to try it with their kids. Goal: 5 more families enrolled.
- **Week 4:** First **Declan's Week** mini-update post on LinkedIn (a screenshot of the dashboard, his Knight rank, his streak). 200 words. Shows the product working over time.

**Days 31-60 — Validate the pattern**

- Weekly "Declan's Week" cadence (Mondays). Same template — screenshot, stat, anecdote, link.
- Mid-month: ship a feature kids asked for, post about it ("Sebastian wanted a fort week, so I added it"). This positions you as a parent-builder, not a tech vendor.
- Approach 1-2 small ed-tech newsletters for a guest post. The Substack network has a "boost" feature — use it.
- Quietly start logging: where did each enrolled family come from? (LinkedIn, Reddit, word of mouth?) The mix tells you what's working.

**Days 61-90 — Build to the September reveal**

- Pre-tease the MAP retest. Frame it as: "8 weeks ago I built this. In 3 weeks we'll know if it worked."
- Substack: a piece called **"What I'd Have Done Differently"** — vulnerable, builder-honest. Big share-bait.
- One concrete external partnership attempt: reach out to a local elementary school principal in Jefferson County. Offer free deployment to 1 class for fall semester in exchange for a case study.
- **September: the big reveal post.** Whatever Declan's fall MAP score is. Either it worked (lean into the story) or it didn't (write the post-mortem). Both are content. The honest version always lands harder than a victory lap.

### Content templates you can reuse

**LinkedIn "weekly update" template:**
```
Week N of the SummerStreak experiment.

📊 Declan: [points] ★ · [rank] · [days done] active days · [books finished] books

[2-3 sentence anecdote about something he did this week]

What I shipped this week: [feature]

Still proving the hypothesis: 8+ MAP RIT points by September.

beatthesummerslide.com
```

**X thread template (5 tweets):**
```
1/ My 4th-grader's reading scores were below grade level. I spent a weekend vibe-coding him a summer reading dashboard. [link to dashboard]

2/ He's not an early adopter. He's a normal kid. But the dashboard hooks him because [emotional hook — streak / leaderboard / prize / friend competition].

3/ Week N: [stat that shows it's working]

4/ Free, no signup, built on Firebase + GitHub Pages. The whole repo is open. [link to GitHub]

5/ September: MAP retest. Either it worked or I'll tell you why it didn't. Follow if you want to see how it lands.
```

**Reddit post template (lead with the kid, not the tech):**
```
Title: My 10yo finished 4th grade below grade level. I built him a dashboard to fight the summer slide and other parents can use it too.

[2 paragraphs: the problem, what you built, the early signs]

It's free, no signup. beatthesummerslide.com

(I'm not selling anything. I'm a PM, not a developer, and I built this in a weekend using Claude. Happy to share the code if you want to fork it for your own kid.)
```

### Metrics that matter

Don't track impressions or follower count — they lie. Track:
- **Enrolled families** (the only true acquisition metric — count `/leaderboard` entries with a real name)
- **Weekly active kids** (`weeklyHistory/{wk}` entry count where `weeklyPoints > 0`)
- **Story page sessions** from referrer (GitHub Pages doesn't track, but if you add a one-line Plausible or Cloudflare web analytics script it's free)
- **Inbound DMs / emails** asking about it — qualitative but the strongest signal

A North Star Metric for now: **"families whose kid logged at least one activity in the last 7 days."** That's the only number that proves the product works.

---

## Part 2 — Year-Round Product Vision

### The problem with "Beat the Summer Slide" as a permanent brand

The current frame is seasonal — June to August. Three months of relevance, nine months of dormancy. Parents discover it in June, abandon it in August, and have no reason to return. That's a fatal acquisition cost-per-retention ratio.

To go year-round, the product needs a frame that's **goal-shape-agnostic**: any kid, any 12-week habit, any season.

### The reframe: "Streak"

Drop "Summer." The core engine — points + ranks + leaderboards + prizes + weekly challenges + parent dashboards + Firebase sync — is content-agnostic. It works for reading. It works for math facts. It works for piano. It works for soccer drills. It works for mindfulness.

Working brand candidates:
- **Streak** (clean, owned, expandable)
- **Quest** (gamier, evokes "12-week quest")
- **Kid Habits** (descriptive, less brandable)
- **Streak School** (positions it adjacent to education)

I lean toward **Streak** for the noun (the product) with **Streak Tracks** as the unit of curriculum (a "track" is a 12-week themed program: Reading Track, Math Track, Music Track, etc.).

### The track model

Each track is:
- A 12-week program with weekly challenges
- A daily activity grid (currently: Read, Write, Math — would vary by track)
- A theme picker (chess, sports, music, gaming — already built and can stay shared across tracks)
- A leaderboard + rank ladder (already built)
- A prize shop (already built)

Example tracks to ship over year 1:

| Track | When | Daily activities | Weekly challenges |
|---|---|---|---|
| **Reading Slide** (current) | Summer (Jun-Aug) | Read, Write, Math | Reading Fort, Comic Creator, etc. |
| **Back to School** | Aug-Oct | Read, Homework Started, 20-min Practice | "Pack your bag the night before," "Ask one question in class," "Help a friend" |
| **Math Facts Master** | Year-round | Times Tables, Word Problem, Math App | "Beat your time," "Teach a parent," "Hardest table day" |
| **Read Across America** | Mar-May | Read, Discuss, Write | Themed around Read Across America Day in March |
| **Music Practice** | Year-round | Practice, Listen, Learn-a-piece | "Perform for someone," "Record yourself," "Try a new instrument" |
| **Mindful Kid** | Year-round | 5-min breathing, Gratitude, Check-in | "Tech-free dinner," "Help someone without being asked" |

A kid can be enrolled in one or multiple tracks. Parent picks which tracks are active at any time. Leaderboards are per-track (kids on Reading compete with other readers; math kids with math kids).

### What's reusable from today

Most of the engine. Specifically:
- ✅ Firebase data model (leaderboard, weeklyHistory, weeklyWinners, admins)
- ✅ Per-profile architecture
- ✅ Google Sign-In
- ✅ Theme picker (chess/sports/music/gaming)
- ✅ Points → rank → leaderboard → prize loop
- ✅ Weekly challenges system
- ✅ Daily activity toggle pattern
- ✅ Parent dashboard, PIN gate, admin tool

What needs to change:
- **Track-aware data model**: every entry, every leaderboard entry, every weekly challenge needs a `trackId` field. Leaderboards filter by track.
- **Track switcher** in the hero (similar to the multi-kid switcher, but for active tracks)
- **Track marketplace** in admin/parent settings: browse and enroll in tracks
- **Curriculum authoring tool** (eventually): so parents/teachers/tutors can build their own tracks

### Phased rollout

**Phase 1 (now → August 2026): Prove the Reading track works**
- Hold the line on current product
- Win September with real outcomes data
- Build the audience (Part 1 above)
- Position the brand as "the family that vibe-coded their way out of the summer slide"

**Phase 2 (August → November 2026): Add the second track**
- Ship **Back to School Track** for fall semester
- Use it as the first proof that the engine generalizes
- Same families re-engage in August instead of churning
- Marketing angle: "Same dashboard, new track — your kid's homework habits this fall"

**Phase 3 (November → March 2027): Track marketplace**
- Add 3-4 more tracks (Math Facts, Music, Mindfulness, Movement)
- Add a parent-facing track picker
- Soft-launch a paid tier ($5-9/mo for unlimited tracks; first track always free)
- Pilot with 50 families paying

**Phase 4 (March 2027+): Schools and teachers**
- Teacher dashboard for classroom-wide use
- Co-create tracks with educators (validates curriculum quality)
- B2B pilot: 3-5 elementary schools at $5/student/year
- Existing roadmap already mentions a Jefferson County school pilot — fold this in

### Pricing — when it's time

Today: free, no signup. Don't break that — it's your acquisition channel.

When you have ~100 active families and 30 enrolled in a second track, introduce:

- **Free forever**: 1 kid, 1 active track, basic dashboard
- **Family ($4.99/mo)**: Unlimited kids, unlimited active tracks, AI-personalized weekly challenges, parent insights dashboard, weekly digest emails
- **School ($5/student/year)**: Teacher dashboard, classroom roll-up reporting, co-branded landing page

The free tier needs to stay genuinely useful — that's the lead magnet. The family tier sells on the **multi-track + AI personalization** angle, both of which require real cost to deliver (Firebase + Anthropic API calls) and both of which deepen the parent buy-in.

### What changes about the marketing story

The vibe-coded-by-a-dad story stays the origin. But the brand voice shifts:

- **Now**: "I built this for my son."
- **Phase 2**: "I built this for my son. Now it works for your kid too."
- **Phase 3**: "Built by a parent, used by families everywhere."
- **Phase 4**: "Built by a parent. Trusted by teachers."

Each shift requires a fresh content moment — a Substack piece, a redesigned landing page, a relaunch on Product Hunt.

### The one thing that has to be true for this whole vision

The September MAP retest is the keystone. If Declan's score moves, every subsequent expansion has a real foundation. If it doesn't move, you'll need to either (a) iterate the Reading track until it does, or (b) pivot the story to be about engagement and habit-building, not outcomes.

Don't ship Track #2 until the Reading track has its September proof point. The brand depends on it.

---

## Part 3 — Launch Website Plan

### Current site vs. launch site

The current beatthesummerslide.com is **product-first**: landing page → enroll my child → dashboard. That works for kids whose parents already know they're coming. But a launch site needs a **story-first** funnel for adults arriving cold from LinkedIn, Substack, Reddit, or Google.

The fix isn't a separate URL — keep beatthesummerslide.com as your only domain. The fix is to **layer in marketing-site surface** to the existing site so the homepage works for BOTH grown-ups doing research AND kids being onboarded by their parents.

### Site architecture (proposed)

```
beatthesummerslide.com/
├── /                       ← REDESIGNED: marketing-first landing
├── /dashboard.html          ← unchanged (the app)
├── /story.html              ← exists; refresh with September data
├── /how-it-works.html       ← NEW: 60-sec explainer
├── /for-parents.html        ← NEW: deeper marketing page for the segment you want
├── /research.html           ← NEW: the science behind "summer slide" + your hypothesis
├── /founders.html           ← unchanged (Docs Hub)
└── /admin.html              ← unchanged (internal)
```

Five public-facing pages total. None of them need to be more than a single HTML file (your existing pattern).

### Homepage (the new "/")

The single most important page. Should answer in **5 seconds** for a cold visitor:
1. What is this?
2. Who is it for?
3. Does it actually work?
4. What do I do next?

**Section-by-section blueprint:**

**Hero (top fold)** — Big claim, real proof, one CTA.
```
SummerStreak
Your kid will actually open this.

A free dashboard that turns the summer reading slide into a streak.
Built in a weekend by a dad. Already used by [N] families.

[🚀 Start Your Kid's Streak]   [📖 Read the story]

[3 small stats below: families enrolled · books finished · words written]
```

**Section 2 — The problem (45 seconds of reading)** — Establishes urgency.
- Summer slide: average kid loses 2-3 months of reading progress
- For kids already behind, the gap compounds every year
- Worksheets don't work. Apps with ads don't work. They need a habit.

**Section 3 — How it works (visual)** — A 4-card row:
1. 📖 Read 15 min · ✏️ Write 50 words · 🧮 Math 5 min — every day
2. ★ Earn points · 🏆 Climb ranks · 🎁 Unlock real-world prizes (parents pick)
3. 🏅 Compete with friends — weekly + lifetime leaderboards
4. 📊 Hypothesis tracker projects fall scores so you'll know if it's working

**Section 4 — Real signal (the credibility moment)** — Live or near-live stats from Firebase. Even simpler: a screenshot of Declan's Knight rank + streak with the date stamp. Show, don't tell.

**Section 5 — The story behind it** — 2 paragraphs from the case study, ending with "[Read the full story →](/story.html)"

**Section 6 — Try it (final CTA)** — Re-emphasizes free, no signup. Same enrollment widget as today.

**Section 7 — Footer** — Story · Docs · GitHub repo · Twitter · Substack.

### /how-it-works.html (90-sec explainer)

The "I'm interested but skeptical" page. Walks through one full week as a kid:

- **Monday morning:** Kid opens dashboard. Sees today's 3 things + this week's challenge ("Build a Reading Fort").
- **Throughout the day:** Reads, writes, does math. Taps each box. Watches points climb. Sees friends' standings update in real time.
- **Friday:** Hits the weekly target. Unlocks a prize (parent buys/gives).
- **Sunday:** Week ends. Monday's dashboard shows new challenge + last week's leaderboard winner.

End with: "Built on the science of habit formation, gamified for elementary kids, parent-controlled. [Try it →]"

### /for-parents.html (deeper sell)

The page that converts the parent doing research. Sections:

- **What your kid sees** (dashboard screenshot, kid view)
- **What you control** (parent screenshot — PIN gate, prize editor, baseline scores, sync settings)
- **The science** (link to /research.html — quick blurbs on consistency > intensity, gamified habits, social motivation)
- **Privacy + safety** (no ads, no kid data collection, parent owns the account, COPPA caveats)
- **What it costs** (free forever for one kid, one track — full transparency)
- **FAQ** (10 questions: how does it work without an app store? what if my kid hates writing? can I customize prizes? what about screen time? etc.)
- **Big enrollment CTA at the bottom**

### /research.html (credibility)

A simple page that cites the science you're betting on. Three sections:
- **The summer slide is real** — link to RAND or NWEA research
- **Consistency beats intensity** — 15 min daily > 75 min weekly
- **Social motivation works for elementary kids** — peer leaderboards
- **The hypothesis you're testing** — your own MAP RIT prediction, dates, criteria for success

This page does double duty: it convinces skeptical parents you're not winging it, AND it serves as your accountability log — "here's exactly what I claimed at the start, here's what happened."

### Visual / brand direction

**Keep the dashboard's brand** — dark navy + gold + soft purple. Don't rebrand for the marketing site. Continuity matters; the marketing site should feel like an extension of the product, not an upsell page.

**Add three things you don't have today:**
1. **A real product screenshot above the fold.** Either render one from the dashboard (Chrome screenshot at 1280×800), or build a marketing-only "demo dashboard" with seeded fake data.
2. **A logo / wordmark.** Right now "SUMMERSTREAK" is just text. A tiny mark (a star with a streak line through it, a stylized 📖, something) makes the brand cohere.
3. **Open Graph images.** Every shared link should preview with a beautiful card, not a screenshot of the URL bar. Set OG tags on every page (story.html already has this — extend to the new pages).

### Build approach — keep it cheap

Don't rebuild on a framework. Keep the single-file HTML pattern. Each new page is one self-contained HTML file with inline CSS, like the existing pages. No build step, no React, no Next.js. Reasons:
- Match your repo conventions (the whole site is hand-written HTML)
- GitHub Pages serves it for free, no toolchain breakage risk
- Lighthouse score stays high (instant TTI)
- Anyone can clone and remix it

The whole launch site is ~5 new HTML files + a homepage redesign. Two to three weekends of work, parallelizable with everything else.

### Launch sequence (3-week ramp)

**Week 1 — Build pages**
- Mon-Wed: New homepage (the biggest piece)
- Thu-Fri: /how-it-works.html
- Weekend: /for-parents.html and /research.html

**Week 2 — Polish and pre-tease**
- Add Plausible Analytics
- Add Open Graph tags + a unified OG image
- Set up a Buttondown/Substack newsletter capture on the homepage
- Pre-tease on LinkedIn: "Big update to beatthesummerslide.com going live next week."

**Week 3 — Launch day**
- Push live Monday morning
- Coordinated posts: LinkedIn, X, Substack, 2 Reddit subs
- DM 15 people who said "this is cool" earlier in the year and ask them to share
- Submit to ProductHunt for following week (PH launch needs its own prep — see below)
- Monitor Plausible. The metric to watch: **homepage → "Start Your Kid's Streak" click-through rate**. Target: > 5%.

### A ProductHunt launch (optional, after the website is solid)

Worth doing once. Timing it ~1 week after the September MAP reveal so you have a real outcome to lead with. ProductHunt rules:
- Launch Tuesday 12:01 AM PT (most upvote time)
- Get 5-10 friends to upvote in the first hour (do NOT ask for vague "support" — ask for specific upvotes; vote rings get penalized)
- Tagline: punchy and curious. e.g. "Built a reading app for my 10-year-old in a weekend. He's reading consistently for the first time."
- First comment by you: the story, the data, the link
- Stay in the thread all day answering questions

A successful PH launch puts you in front of 5,000-30,000 people. Not all parents, but the ones who care will share.

### Content checklist (assets to gather before launch)

- [ ] Real screenshots of the dashboard at 3 different states: empty, mid-week, end-of-week with friends
- [ ] One short demo video (30 sec, screencast, voice-over): "Here's what your kid does."
- [ ] OG image (1200×630) — gold + navy, big "SummerStreak" wordmark, the tagline
- [ ] Updated favicon (currently default GitHub)
- [ ] A logo or wordmark
- [ ] Real testimonials from at least 3 enrolled families (text + 1 photo each, with permission)
- [ ] Press kit page (eventually): logo files, hero shot, founder photo, one-liner, longer description
- [ ] Email signup form (Substack works for free)

---

## Immediate next steps (this week)

1. **Post the story to LinkedIn** — the asset already exists at beatthesummerslide.com/story.html. Just paste a 200-word version with the link. Pin to your profile.
2. **Set up Substack** at brentomalley.substack.com (or similar). Cross-post the story as your first piece.
3. **Add Plausible Analytics** to the site (one-line script, free for hobby use, no cookie banner needed). Without analytics you're flying blind on referral sources.
4. **Schedule the September reveal**: pick the date you'll re-test Declan and put it on your calendar. Plan the post 2 weeks before.
5. **Pick a Phase-2 track to start designing** — even just on paper. "Back to School" is the obvious one. What 12 weekly challenges would land for the first quarter of school?
6. **Draft the new homepage hero** — just the top fold. Even before building, write the copy on paper. The right hero unlocks everything downstream.

Each of these is < 30 min of work (except the homepage rebuild). The whole plan is to compound: build → share → learn → repeat.
