# Declan's Summer Reading Dashboard

A 12-week summer reading challenge tracker, themed around chess and strategy.

**Live site:** https://brentomalley150.github.io/declansummerlearning/

## What it does

- **Summer tab** — 12-week calendar grid; click any day to log activity
- **Day tab** — daily check-in for read / write / wrap-up activities
- **Friends tab** — leaderboard, invite links, goals per friend, score-code sharing
- **My Rank tab** — chess-themed rank progression (Pawn → Grandmaster) and streak calendar
- **Trophies tab** — 24 unlockable achievements
- **Prizes tab** — point-redeemable rewards, capped by an ultimate end-of-challenge prize (Elitch Gardens trip)
- **Parent section** (collapsible on the Summer tab) — hypothesis tracker with leading indicators, fall test projections, and a Family Summary email button

## The hypothesis

If Declan completes 70%+ of daily activities, reads 1,000+ minutes, and finishes 4+ books over the 12-week summer plan, his fall MAP Reading RIT will improve from 185 → 193+ and Written Expression from 17% → 32%+.

## Technical notes

- Single-file static HTML — no backend required
- All progress stored in `localStorage` on the device
- Friends compete cross-device via share codes and invite URLs
- Hosted via GitHub Pages

## Sharing the dashboard

Once Pages is enabled, the live URL is shareable. The dashboard's built-in invite link feature generates URLs that bootstrap each friend's own profile automatically when they open the link.
