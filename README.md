# Streak — Founders Hub

The product, vision, and investor-facing home for **Streak** — the year-round
evolution of the SummerStreak reading challenge.

**Live:** https://beattheslide.com

> This repo is the **hub** (docs, vision, PRD, prototype, decks).
> It is not the app. See "Where everything lives" below.

## Where everything lives

| What | Repo | Live at |
|---|---|---|
| **Founders hub** (this repo) | `streak-app` | https://beattheslide.com |
| **v2 app** — what Kate & Brent are building now | `streak-v2` | — (in development) |
| **v1 app** — the live, proven SummerStreak app | `declansummerlearning` (private) | https://beatthesummerslide.com |

`streak-landing` is **archived** — its landing page concept now lives here as `landing.html`.

## Pages in this repo

| File | What it is |
|---|---|
| `index.html` | Vision Hub — the front door; links to everything below |
| `proof.html` | What we've already proven (v1 results & traction) |
| `PRD.html` / `PRD.md` | Product Requirements Document v2.0 |
| `prototype.html` | Interactive prototype — 9 screens, 3 personas |
| `landing.html` | Future marketing landing page concept |
| `story.html` | "How I vibe-coded a reading app for my 10-year-old" |
| `vision.md` | Product vision + marketing strategy |
| `founders-84538ab568/` | Unlisted founders docs — pitch deck, gap analysis, feature breakdown |

Investor decks: `Streak-Investor-Deck-v0.1-DRAFT.pptx`, `SummerStreak-Investor-Deck.pptx`

## Team

- **Kate** — Founder
- **Brent** — Advisor

## Notes

- Static HTML, no build step. GitHub Pages serves `main` at the repo root.
- This repo intentionally contains **no Firebase config and no app code**. The v1
  dashboard and admin pages were removed from here so nothing in the hub can write
  to the live v1 database. The real ones live in `declansummerlearning`.
