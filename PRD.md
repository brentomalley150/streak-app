# STREAK

**The kid habit platform that started as a summer reading dashboard.**

**Product Requirements Document · v2.0**

**Author:** Brent O'Malley · **Date:** June 2026 · **Status:** Draft · **Supersedes:** SummerStreak PRD v1.0 (May 29, 2026)

**Live demo (v1, summer track):** [beatthesummerslide.com](https://beatthesummerslide.com)
**Vision hub:** [brentomalley150.github.io/streak-app](https://brentomalley150.github.io/streak-app)

---

## 1. Executive Summary

### Problem Statement

Elementary-school kids fall behind on foundational skills not because they don't have access to learning content, but because they don't sustain the *habit*. The summer slide is the most visible symptom — average K-5 student loses 1-2 months of reading skill every June-August. But the same dynamic plays out year-round: math fluency stalls between tests, music practice falters between lessons, homework consistency collapses in the second half of every semester. Parents want to intervene, but lack a single tool that turns any kid skill goal into a daily routine the kid *actually opens*.

### Proposed Solution

**Streak is a year-round, multi-track kid habit platform.** It runs on the same gamified engine across content domains — daily activity check-ins, theme-aware idea prompts, points → ranks → leaderboards → real-world prizes, real-time cross-device sync, and parent-side outcome projection. Each *track* is a 12-week themed program (Reading Slide, Back to School, Math Facts, Music Practice, Mindful Kid, and more). A family enrolls in one track free; multi-track families pay $4.99/mo; schools and tutors pay $5/student/year for classroom dashboards.

The engine is already proven in a single-track pilot (SummerStreak). The Streak vision generalizes it.

### Business Impact

- **$11B TAM** in US K-5 supplemental learning + adjacent kid SaaS (Grand View Research 2024)
- **Year-round retention** — families have a reason to engage 12 months instead of 3, ~4× the lifetime value per acquisition
- **Network effects** — friend leaderboards across tracks (a kid on Math track can see siblings on Music track on their family dashboard)
- **Parent-built brand** as the wedge: the SummerStreak case study + the "vibe-coded by a dad" narrative is the most defensible acquisition story in the category
- **$0 marginal cost** per free user (free-tier infrastructure); ~$2 ARPU/mo at scale on Premium

### Key Milestones

| Milestone | Target Date | Status |
|---|---|---|
| SummerStreak v1 (Reading track) shipped | May 29, 2026 | DONE |
| First fall test validation (n=1 founder kid + cohort) | Sep 2026 | In progress |
| Brand transition: SummerStreak → Streak | Aug 2026 | Planned |
| Phase 2: Back to School track shipped | Oct 2026 | Planned |
| Phase 3: Track marketplace + paid Family tier | Mar 2027 | Planned |
| Phase 4: School pilot (3 schools, classroom dashboards) | Aug 2027 | Planned |

### Success Metrics

| Metric | Baseline (v1) | Target (Year 1 of v2) |
|---|---|---|
| Active families across all tracks | 6 | 500 |
| Tracks live | 1 (Reading Slide) | 5 (Reading, BTS, Math, Music, Mindful) |
| 7-day active rate (kid logged ≥1 activity) | TBD | ≥60% |
| Median tracks-per-family | 1.0 | 2.0 |
| Premium conversion (Family tier) | n/a | 8% of active families |
| School pilots | 0 | 3 (≥1 with renewal commit) |
| Net Promoter Score (parent) | n/a | ≥55 |

---

## 2. Problem Definition

### 2.1 Customer Problem

**Who:** Parents of K-5 students (ages 5-11) who have specific habit goals for their child — academic (reading, math), creative (music, writing), or developmental (mindfulness, daily movement) — that the school year alone doesn't address.

**What:** No single tool that turns any kid skill goal into a daily routine the kid voluntarily opens. Existing solutions are either single-purpose (Khan Kids for math), tutor-mediated (Outschool), invisible to the kid (assessment portals), or just lists (library reading challenges).

**When:** Year-round. Different goals are urgent at different times — summer (reading regression), August (school routine reset), throughout the year (music practice, math fluency).

**Where:** At home, without the structure or accountability that school provides — but ALSO during the school year when parents want supplementary practice without it feeling like homework #2.

**Why current tools fail:** They're built around content. Streak is built around habit. A kid on Khan Kids gets math problems; a kid on Streak gets a streak, a rank, a leaderboard, and a real-world prize tied to their kid-chosen theme — and the math problems are just one of the activities that move the loop forward.

**Impact:** A kid who doesn't sustain a daily habit on any single skill goal compounds the loss across all of them. The same gamified engine, applied across goals, lets parents build multiple habits in parallel without buying multiple apps.

### 2.2 Market Opportunity

US K-5 supplemental learning + adjacent kid productivity SaaS is an $11B market growing at 12% annually. The serviceable addressable segment — families willing to pay $5-15/mo for structured kid habit tools — represents approximately $1.5B. Year-one obtainable market (SOM) is $300K based on 500 paying families at $59/year.

**Why existing solutions fall short:**

| Solution | Price | Gap |
|---|---|---|
| Khan Academy Kids | Free | Single domain (math/early literacy); no habit/streak layer; no social |
| Prodigy Math | Free + $7/mo | Math-only; gamified but no parent-facing outcome projection |
| Outschool | $30-75/session | Tutor-dependent; expensive; not daily |
| Kumon | $150-300/mo | Generic worksheets; no kid-facing motivation; no real-time data |
| Atom Learning / IXL | $20-30/mo | Curriculum-focused, not habit-focused; feels like school |
| Marco Polo Learning, Lingokids | $10-15/mo | Single domain; gamification thin; not multi-track |
| **Streak (proposed)** | **Free / $4.99/mo / $5/student/yr** | **Multi-track engine + habit-first + parent outcome projection + cross-family social** |

**Why now:**
- Post-COVID skill regression created a multi-year cohort effect; parental anxiety is at a structural high (NAEP 2024 4th grade reading at 32-year low)
- AI inference cost dropped ~80% in 18 months, making per-track personalized prompts viable at <$0.01/family/month
- Static-hosting + AI-assisted build economics make multi-track expansion achievable as a solo + contributor build, not a "raise $1M" project
- The SummerStreak pilot already proved the engine works for one track — extending to five is content authoring, not new engineering

### 2.3 Business Case

**Revenue Potential:**
- Year 1: 500 paid families × $59/yr = $29K ARR, school pilot adds $5K-15K
- Year 3: 5K paid families × $59/yr + 10 schools × $2.5K/yr = ~$320K ARR
- Year 5: 25K paid families + 50 schools at scale = ~$1.6M ARR

**Cost Savings vs. v1 model:**
- Free tier remains $0 infra (GitHub Pages + Firebase free tier)
- Premium tier adds ~$3K/mo at 5K paid users (Firebase paid tier + AI prompt costs)
- No employee headcount until Year 2

**Strategic Position:** Streak is positioned to own "kid habit tracking" as a category — the same way Duolingo owns "language streaks" and Headspace owns "adult meditation." First-mover advantage on the parent-built brand narrative; defensibility comes from the multi-track network (family stays for reading, discovers math, adds music — single-track competitors can't match).

**Risk of inaction:** If a well-resourced kid-tech competitor (Khan, IXL, Duolingo Kids) ships a multi-track habit platform first, the category leader position is lost. The 4-week head start from the SummerStreak pilot is the wedge; turning that into a year-round product before competitors notice is the strategic priority.

---

## 3. Solution Overview

### 3.1 What We're Building

A single-page web application (mobile + desktop responsive) hosted on GitHub Pages with a Firebase backend. The Streak app loads a **Track** the kid is currently enrolled in. Each track defines a daily activity grid + a 12-week themed challenge schedule + a curated idea pool. The kid sees their dashboard — Read/Write/Math (for Reading Slide), or Homework Started/20-min practice/Pack-the-bag-streak (for Back to School), or Practice/Listen/Learn-a-piece (for Music Practice). Same gamified loop, swappable content.

Parents access a PIN-gated section with hypothesis tracking + outcome projection (where applicable per track), prize editor, multi-kid switcher, and Family Summary export. Families can enroll a child in multiple tracks; the parent dashboard rolls up across them.

### 3.2 In Scope

**P0 — Required for v2 launch (Phase 2-3):**

| Feature | Description |
|---|---|
| Track abstraction in data model | Every leaderboard entry, weekly challenge, activity log includes a `trackId` |
| Track switcher in hero | Kid can toggle between active tracks (like multi-kid profile switcher) |
| Track marketplace (parent settings) | Browse, enroll, deactivate tracks |
| Per-track leaderboards | Kids on the same track compete; cross-track aggregate is parent-only |
| Reading Slide track (existing v1) | Already shipped; ports to new data model |
| Back to School track | NEW — fall semester habit-building (homework, practice routines, bag-packing streak) |
| Math Facts Master track | NEW — times-tables fluency with theme-aware prompts |
| Music Practice track | NEW — practice / listen / learn-a-piece daily structure |
| Mindful Kid track | NEW — 5-min breathing, gratitude, check-in |
| Per-track theme picker | Themes stay per-track (chess for reading, gaming for math, etc.) |
| Stable Google identity | Already shipped (v1); reused without change |
| Cross-device sync | Already shipped (v1); reused without change |
| Multi-profile per parent account | Already shipped (v1); reused without change |
| Parent dashboard cross-track roll-up | NEW — see all kids across all enrolled tracks in one summary |

**P1 — Important, post-launch within 90 days:**

| Feature | Description |
|---|---|
| AI-personalized weekly challenge | Replaces curated pool with per-kid generated challenges (Premium) |
| Track recommender for parents | Based on kid age + stated goals, suggest 2-3 tracks |
| Family digest email (weekly, auto-send) | Scheduled via cron — was a manual button in v1 |
| Achievement export | PDF of "Streak Resume" at end of each completed track |
| Friend invite by track | Invite Cooper to your Math track without exposing your Reading streak |
| Light theme + dark theme | v1 was dark-only; add light theme for parent-facing surfaces |

**P2 — Nice-to-have, year 2:**

| Feature | Description |
|---|---|
| Native iOS / Android wrappers | Wrapping the PWA; push notifications |
| Teacher / classroom portal | Cohort progress reporting, parent-teacher messaging |
| Custom track authoring | Parents/teachers/tutors build their own 12-week programs |
| Track community pages | Public discussion + leaderboards per track for top families |
| AI-graded writing samples (Reading track) | Premium add-on; rubric-based feedback on uploaded writing |

### 3.3 Out of Scope (v2)

- Curriculum authoring tools for parents (Phase 4 if at all)
- Real-time multiplayer challenges (e.g., kids racing each other live)
- Voice / video features (privacy + COPPA complexity)
- Integration with school assessment portals (manual baseline entry continues)
- Hardware accessories (no smart-watch companion, no physical kit)
- Adult version (Streak Adult) — focus stays on K-5 in v2

### 3.4 v2 MVP Definition

Phase 2 (October 2026) ships:
- Track-aware data model deployed
- Reading Slide track migrated to new model
- Back to School track live, paired with the start of school
- Track switcher in hero
- Track marketplace in parent settings
- Existing v1 families seamlessly upgraded (their Reading data preserved)

**Learning goals from Phase 2:**
1. Do existing summer families re-engage when Back to School ships, instead of churning?
2. Does the track abstraction actually generalize, or do we hit unexpected coupling?
3. What % of families enrolled in 1 track add a 2nd within 30 days? (Strong predictor for paid tier viability.)

---

## 4. User Stories & Requirements

### 4.1 User Stories

**US-1: Track switching (Kid)**
> As Declan (10yo), I want to switch between my Reading and Math tracks with one tap, so I can do one in the morning and the other before bed without re-enrolling.

Acceptance:
- Switch-track button in hero, visible when 2+ tracks active
- Switch persists across sessions
- Each track has its own theme, points, leaderboard

**US-2: Track marketplace (Parent)**
> As Brent (parent), I want to browse available tracks and enroll my kid in a second one (Math Facts), so my reading-focused summer routine becomes a year-round math + reading habit.

Acceptance:
- Marketplace shows all available tracks with description, recommended age, expected daily time
- Enroll = one click; sets up activity grid + leaderboard automatically
- Free tier supports 1 active track at a time; Premium supports unlimited

**US-3: Cross-track parent rollup (Parent)**
> As a parent of two kids each in two tracks, I want one dashboard view showing all 4 streaks at once, so I don't have to context-switch between profiles + tracks.

Acceptance:
- Parent dashboard groups by kid first, then by track
- Each row shows: kid · track · current week · current streak · last activity time
- Click any row to deep-link into that kid + track view

**US-4: Friend invite by track (Kid)**
> As Declan, I want to invite my friend Sebastian to the Math track without him seeing my Reading progress, so we can compete on math without baring all my stats.

Acceptance:
- Invite link includes trackId
- Friend's dashboard auto-enrolls them in the linked track
- Cross-track visibility limited to family-only (kids can't browse strangers' other tracks)

**US-5: Streak Resume (Parent + Kid)**
> As Declan (and proudly his parents), I want a printable "Streak Resume" at the end of a completed track, so we can show grandparents / save in a school portfolio / start a new track with momentum.

Acceptance:
- Auto-generated PDF on track completion (12 weeks)
- Includes: kid name, track, dates, total activities, rank achieved, weekly winner badges, prizes claimed, baseline-to-outcome data if available
- One-click download or email-to-parent

### 4.2 Functional Requirements

| ID | Requirement | Priority |
|---|---|---|
| FR1 | All v1 functional requirements preserved (single-tap completion, localStorage + Firebase sync, Google Sign-In, multi-profile, etc.) | P0 |
| FR2 | `trackId` field on every leaderboard entry, weekly challenge, day entry, weekly winner | P0 |
| FR3 | Track switcher UI in dashboard hero | P0 |
| FR4 | Track marketplace UI in parent settings | P0 |
| FR5 | Per-track Firebase leaderboard isolation (kids on different tracks don't see each other on the leaderboard) | P0 |
| FR6 | Parent rollup view aggregating all kids × all tracks | P0 |
| FR7 | Free tier enforces 1 active track per kid; Premium allows unlimited | P0 |
| FR8 | Auto-migration of existing v1 users into the new track-aware data model | P0 |
| FR9 | AI-personalized weekly challenges (Premium) | P1 |
| FR10 | Weekly auto-send Family Summary email | P1 |
| FR11 | PDF "Streak Resume" export at track completion | P1 |
| FR12 | Track recommender based on kid age + stated goals | P1 |

### 4.3 Non-Functional Requirements

- **Performance:** Initial page load < 2s on 4G mobile. Track switch < 200ms. Cross-device sync latency < 5s under normal load.
- **Scalability:** Static front-end CDN-served via GitHub Pages. Firebase backend scales to ~10K active families on Spark plan; cross over to Blaze plan at ~5K to avoid surprise (estimated $30-80/mo at that size).
- **Security:** Google OAuth via Firebase Auth (no password storage). Per-track Firebase security rules ensure kids can only write to their own track entries. PIN-gated parent section persists.
- **Reliability:** 99.9% uptime via GitHub Pages + Firebase SLA. Daily Firebase data backup to a cold-storage bucket.
- **Usability:** Kid-facing copy at ~2nd grade Lexile. Parent-facing copy reads at adult professional level. Mobile-first; WCAG AA contrast.
- **Compliance:** v2 launch requires COPPA-compliant parental consent flow before paid tier opens. Marketing site adds privacy policy + data deletion request handling.

---

## 5. Go-to-Market Strategy

### 5.1 Launch Plan

**Phase 1 (Now → August 2026): Win the SummerStreak story**
- Continue iterating on the Reading track
- Run the September MAP retest with the founder kid + cohort
- Build the audience around the build story (see Marketing Plan, separate doc)
- Brand stays SummerStreak; the URL stays beatthesummerslide.com

**Phase 2 (August → November 2026): Add Back to School + brand transition**
- Ship Back to School track in time for fall semester
- Brand transition: SummerStreak → Streak. New marketing site at streak-something.com (TBD)
- Existing families get a "We evolved" splash; data migrates automatically
- All summer users get free access to the new fall track
- Goal: 60%+ of summer users come back for fall

**Phase 3 (November 2026 → March 2027): Marketplace + paid tier**
- Ship 3 more tracks (Math Facts, Music Practice, Mindful Kid)
- Open the track marketplace; default to free 1-track, paywall the second
- Pilot the $4.99/mo Family tier with 50 families
- ProductHunt launch (~Feb 2027) — wait for ≥3 tracks live + retention data + September results

**Phase 4 (March 2027+): Schools & teachers**
- Teacher dashboard for classroom-wide use
- Pilot with 3-5 elementary schools in Jefferson County at $5/student/year
- B2B sales motion begins

### 5.2 Distribution Channels

| Channel | Stage | Why |
|---|---|---|
| LinkedIn | Phase 1-3 | Warmest audience for the vibe-coded-by-a-dad narrative; PM-curious parents amplify |
| Substack | Phase 1-3 | Long-form home for the case study; build to September reveal |
| Reddit (r/Parenting, r/Education) | Phase 2-3 | Where the actual end users live; story-first, not pitchy |
| X / Build-in-public | Phase 1-3 | Micro-updates; tag Anthropic + ed-tech voices |
| ProductHunt launch | Phase 3 | One-shot amplifier once ≥3 tracks live + September data is real |
| Parent Facebook groups | Phase 3-4 | High-trust referrals from existing families |
| Reading specialists + tutors | Phase 3-4 | Specific track recommendation channel (Reading + Math) |
| School counselors | Phase 4 | B2B wedge for the teacher portal |
| Parent podcasts (ed-tech adjacent) | Phase 3-4 | Founder interviews drive trust and reach |

### 5.3 Pricing

| Tier | Price | Features |
|---|---|---|
| **Free** | $0 | 1 active track per kid, unlimited kids per Google account, all core features (dashboard, leaderboard, rank, prizes, weekly challenges, parent controls) |
| **Family** | $4.99/mo or $39/yr | Unlimited active tracks, AI-personalized weekly challenges, multi-kid roll-up dashboard, weekly auto-email, Streak Resume PDF export |
| **Schools** | $5/student/yr | Teacher classroom dashboard, cohort reporting, parent-teacher messaging, custom track support |

Free tier deliberately generous — it's the lead magnet. The Family tier sells on **multi-track + AI personalization + parent ergonomics**. The Schools tier is sold separately B2B and unlocks the teacher dashboard.

---

## 6. Risks & Mitigations

| Risk | Probability | Impact | Mitigation |
|---|---|---|---|
| September MAP retest doesn't show improvement → outcome claim weakens | Medium | High | Lean into engagement-based marketing; honest post-mortem; iterate the Reading track for v2.1 |
| Brand transition (SummerStreak → Streak) loses existing users | Medium | High | Splash-page bridge; preserve all data; offer one new track free to existing families |
| Track abstraction breaks coupling assumptions in the engine | Medium | Medium | Pilot Phase 2 with internal family + 5-10 beta families before public release |
| Free → Paid conversion stalls below 5% | Medium | High | Add lifecycle hooks (email digests, achievement unlocks) before paywall; iterate paywall placement |
| COPPA scrutiny at paid scale | High | High | Add verifiable parental consent flow as part of Phase 3 ship; engage specialist counsel ($5K-10K) |
| Competitor (Khan, IXL, Duolingo Kids) ships multi-track first | Medium | High | Move fast on Phase 2; lock down the brand narrative; focus on the unique "parent-built" position |
| Single-dev velocity caps Phase 3+ | High | Medium | Plan for one contributor at Phase 3 inflection; budget $15-30K for a part-time engineer |
| Track quality varies (Reading great, Music mediocre) | Medium | Medium | Co-author tracks with subject-matter experts before launch; A/B test track engagement before promoting |
| Firebase free tier crossed unexpectedly | Low | Low | Active monitoring at 50% threshold; sharded leaderboard refactor in roadmap |

---

## 7. Timeline & Milestones

| Milestone | Date | Deliverables | Success Criteria |
|---|---|---|---|
| **Phase 1: Win SummerStreak** | Now → Aug 2026 | Iterate Reading track; build audience | ≥10 enrolled families, MAP retest scheduled |
| September MAP retest | Sep 2026 | Real outcome data | Honest debrief regardless of result |
| **Phase 2: Brand + BTS** | Aug → Nov 2026 | Streak rebrand, Back to School track, track-aware data model | 60%+ summer users re-engage |
| **Phase 3: Marketplace** | Nov 2026 → Mar 2027 | 3 more tracks live, paid Family tier, ProductHunt | 50 paying families, ≥2 tracks-per-family median |
| **Phase 4: Schools** | Mar → Aug 2027 | Teacher dashboard, 3-5 school pilots | ≥1 school commits to renewal |
| Year 1 outcome review | Aug 2027 | Annual retrospective, v3 PRD | $30K+ ARR, 500+ active families, 1+ school renewal |

---

## 8. Team & Resources

| Role | Allocation | Notes |
|---|---|---|
| Founder / PM / Builder | Brent O'Malley (100%) | AI PM; continues vibe-coding through Phase 2-3 |
| Part-time engineer | 1 contractor, ~10 hrs/wk from Phase 3 | $20-30K for 6 months |
| Subject-matter experts (per track) | $500-1500/track | Reading specialist (track exists), math teacher, music teacher, SEL specialist |
| COPPA legal review | One-time, before Phase 3 paid launch | $5-10K |
| Design polish (marketing site) | 1 contractor, 40 hrs | $3-5K |
| Marketing / content | Brent owns Phase 1-2; consider freelance ghostwriter for Substack at Phase 3 | $5-10K/yr |

**Phase 2 budget (Aug-Nov 2026):** $5K (mostly SME for Back to School track + design)
**Phase 3 budget (Nov 2026 - Mar 2027):** $35K (engineer + legal + design + SMEs for 3 new tracks)
**Phase 4 budget (Mar - Aug 2027):** $25K (school pilot motion, teacher portal SME)

---

## 9. Open Questions

1. **Brand:** Streak is the placeholder. Does it stick, or do we land on KidStreak, Quest, or something else? Decision needed before Phase 2 marketing.
2. **Domain:** Stay on beatthesummerslide.com indefinitely (with `/streak` paths)? Buy a new primary domain? Decision drives Phase 2 marketing site build.
3. **First paid track:** Math Facts has biggest TAM; Music has highest willingness-to-pay (parents already pay for lessons). Which behind the paywall first?
4. **Migration path for v1 users:** Do they wake up to a new dashboard one day, or get a "Hey, we evolved" splash screen? UX research needed.
5. **AI prompt economics:** Per-kid AI-generated challenges add real cost. Need a usage model — generate once per week and cache vs. on-demand?
6. **Teacher portal scope:** Same dashboard with read-only multi-student view, or a separate experience? Latter is bigger investment; pilot with one school to learn before deciding.
7. **Outcome projection for non-academic tracks:** Reading has MAP RIT. What's the equivalent for Music? Mindful Kid? Some tracks may not have an outcome projection at all — is that OK or does it weaken the brand?

---

## 10. Assumptions Made

- The SummerStreak engine generalizes to other content domains without major refactor (≥80% reusable). Validated in part by the Phase 1 build.
- Parents will pay $4.99/mo for unlimited tracks if they get genuine value from the first free track. Untested.
- Schools will adopt at $5/student/year IF the teacher portal is genuinely useful and parents like the product first. Untested.
- The vibe-coded-by-a-dad narrative remains a defensible acquisition story through Year 2 (it gets less novel over time).
- Firebase free tier supports ~100 active families per project before hitting limits. Need to actively monitor.
- COPPA compliance is achievable as a parental-consent layer on top of Google OAuth, not a full rebuild. Confirm with counsel.
- The September MAP result for the founder kid is broadly representative; it isn't, but it's the strongest single data point we'll have at launch.

---

## Appendix A — What carries over from v1 unchanged

The Streak v2 PRD assumes these v1 components ship-as-is, no refactor:

- Single-page HTML architecture
- Firebase Realtime Database backend
- Google Sign-In via Firebase Auth
- Per-parent stable UID + multi-profile model
- Composite leaderboard keys (`{googleUid}_{profileId}`)
- Per-week point adjustments bucket
- Firebase-backed canonical weekly winners
- Theme picker (chess / sports / music / gaming)
- One-click-per-day anti-spam locks
- Days Done active-entry filter
- Hub / Story / Admin / Vision-page surface

## Appendix B — Source documents

- v1 PRD: `SummerStreak-PRD.docx` (May 29, 2026)
- Vision strategy: `vision.md` (`streak-app/vision.md`)
- Proof reference: `proof.md` (`streak-app/proof.md`) + `proof.html`
- Live v1 demo: [beatthesummerslide.com](https://beatthesummerslide.com)
- Vision hub: [brentomalley150.github.io/streak-app](https://brentomalley150.github.io/streak-app)
