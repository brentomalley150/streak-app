# Summer Slide PRD — Gap Analysis

**Reviewed:** `prd.html` (Founders Hub PRD)
**Benchmarked against:** `PRD-v2-NewVersion.md` — CrewCares / BuildtheCrew v2 (the latest PRD)
**Owner:** Kate O'Malley · **Date:** 2026-05-30

---

## TL;DR

The Summer Slide PRD is a **5-section scaffold of prompts** — correct headings, but every section is a "fill this in" placeholder with no real content. The CrewCares v2 PRD is a near-review-ready Stage-4 document with **14 sections**. Measured against it, the Summer Slide PRD is missing not only content but **seven whole sections that v2 treats as core**: a testable hypothesis, strategic fit/competition, a defensibility (MOAT) argument, a "why agentic" justification, an AI behavior spec with safety guardrails, an eval-driven roadmap, and open questions with working positions. Because Summer Slide targets **children**, the absent child-safety / COPPA / consent posture is the single most urgent gap — it's the analogue of v2's consent + HIPAA-aligned + moderation thinking.

---

## What CrewCares v2 does (the bar)

v2's structure: **What this doc is → Hypothesis → Problem → Personas → Strategic Fit → Defensibility → Solution → Non-Goals → Success Metrics → Roadmap → Open Questions → What changed → Stage Checklist → Gaps.** The things that make it strong — and that the Summer Slide PRD should match:

- **Falsifiable hypothesis** with a named outcome metric (+10pp aging-in-place over a ~75% NHATS baseline), **leading indicators** at 6 months, a **validated instrument** (Zarit Burden Interview), and an explicit **falsification condition**.
- **Problem with cited evidence** — real AARP/NAC 2025 and Census stats, current workarounds, and a "if we don't solve it" cost (quotes still flagged `[NEED]`, honestly).
- **Three deep personas** (Maya, Daniel, Patricia) with jobs-to-be-done, pains, the key product moment, and explicit **build-for / cut-for** lists, plus cross-persona design principles.
- **Strategic fit** — why-now, a **brand wedge** ("the Signal of family caregiving"), four design pillars, and a **named competitive table** with the structural gap of each rival.
- A standalone **Defensibility / MOAT** section: four pillars (coordination graph, longitudinal context, services flywheel, trust), an honest "what we do NOT have yet," and **falsifiable watch metrics**.
- A **"why agentic, not rule-based"** section that states the counter-argument and draws the line: agent judgment on soft cases, **deterministic rules on safety-critical ones**.
- A **solution spec** with user flow, key states, an **AI behavior table (20 input→output examples)** and **hard rejection/safety criteria**.
- A **roadmap built by method**: component breakdown → ML risk assessment per component → scope narrowing to the **single riskiest AI assumption (the MVP bet)** → phased rollout with **quantified go/no-go eval gates** (intent accuracy ≥85%, retrieval top-1 ≥80%, hallucinated-fact <2%, 100% citation coverage) → rollback with auto-revert. An **eval harness from day one**.
- A **metrics table** (metric · type · baseline · target · timeframe) + **guardrails** + a "how these targets were set" rationale.
- **Open questions paired with working positions** (pricing, consent, crew size, moderation, HIPAA, vetting, brand, commerce) — reviewers pressure-test positions, not blanks.
- A **Stage-4 checklist** and an explicit list of remaining gaps.

---

## Section-by-section gap table

| CrewCares v2 section | Summer Slide PRD status | Gap |
|---|---|---|
| **0. What this document is** | Missing | No provenance, scope, or source-synthesis note. |
| **1. Hypothesis** | **Missing entirely** | No testable belief, no outcome metric, no leading indicators, no falsification condition. |
| **2. Problem** | Heading + prompts | No cited learning-loss/market stats, no parent/teacher quotes, no current-workarounds, no cost-of-inaction. |
| **3. Personas** | Lists *user types* (students, buyers, admins) | Zero developed personas. No JTBD, pains/gains, trigger or key product moment, no build/cut. v2 has 3 deep personas. |
| **4. Strategic Fit / Competition** | **Missing entirely** | No why-now, no brand wedge, no competitive table (Beanstack, Scholastic, Renaissance/AR, library programs, Epic!), no "why we win." |
| **5. Defensibility / MOAT** | **Missing entirely** | No moat thesis, no data/network-effect argument, no honest "what we don't have yet," no watch metrics. |
| **— Why agentic, not rule-based** | **Missing entirely** | No justification that AI is the right tool, no agent-vs-rules line, no acknowledgement of AI risk. |
| **6. Solution** | "Scope & Requirements" prompts | No user flow, no key states, and — critically — **no AI behavior spec and no rejection/safety criteria**. |
| **7. Non-Goals** | One sub-bullet | Not a developed "we are NOT building…" list. |
| **8. Success Metrics** | Prompts only | No table, no baselines, no numeric targets/timeframes, **no guardrails**, no target rationale. |
| **9. Roadmap** | "milestones tied to summer" prompt | No component breakdown, no risk assessment, **no MVP "riskiest assumption" bet, no eval harness/gates**, no phases, no rollback. |
| **10. Open Questions** | Prompt only | No questions, and none with working positions/owners. |
| **12. Stage Checklist** | Missing | No readiness self-assessment. |

---

## The highest-priority gaps (fix these first)

### 1. Child-safety, privacy & consent — the domain-critical gap
v2 spends real space on consent (three loved-one consent states), a HIPAA-aligned posture, and moderation because it touches a vulnerable population. Summer Slide touches **children** and the PRD says nothing about it. Essential and currently absent:
- **COPPA** posture (under-13 data, verifiable parental consent), and **FERPA** if selling into schools.
- Parent/teacher consent and account-control model; who can see a child's activity and leaderboards.
- Data minimization for minors; safe leaderboard/social design (no exposing kids' names, locations, or contact to strangers).

Treat it as a first-class section the way v2 treats consent + guardrails. It's both a legal requirement and a trust/positioning asset.

### 2. A testable hypothesis with a falsification condition
v2 opens with one and even names what result would prove it *wrong*. Summer Slide jumps to "Overview." Add:
> *"We believe a competitive, streak-based summer reading app will reduce summer reading loss for K-8 students, measured by fall reading-benchmark change vs. a control, target +X. Leading indicators: weekly active readers and reading-minutes/week. If engagement rises but the fall benchmark doesn't move, the hypothesis is refuted."*

### 3. AI behavior spec + "why agentic" + hard safety rules (this is the AI-PM core)
v2's strongest material is the agent-vs-rules argument plus 20 input→output examples and non-negotiable safety rules. The Summer Slide PRD specifies **no AI behavior at all**. Decide what the AI does (level-appropriate book recommendations? comprehension check-ins? parent progress summaries? motivational nudges?), justify why an agent beats static rules, then spec ~15–20 examples and the refusals — e.g., never recommend age-inappropriate content, never message a child without guardian visibility, never expose one child's data to another.

### 4. Real personas, not user-type labels
Replace "students / buyers / admins" with 2–3 developed personas — e.g., **the reluctant 4th-grade reader**, **the motivated-but-time-starved parent**, **the summer-program coordinator/teacher** — each with JTBD, pains, the trigger moment, the key product moment, and build-for/cut-for, mirroring Maya/Daniel/Patricia.

### 5. Strategic fit, competition, and a defensibility (MOAT) story
Two missing sections in one theme. Add a why-now + brand wedge + a named competitive table (Beanstack, Scholastic Summer Reading, Renaissance/Accelerated Reader, library programs, Epic!/Reading Eggs) with each rival's structural gap. Then a defensibility section: what compounds with use (engagement data, a school/district graph, a reading-level model, brand trust with parents), an honest "what we don't have on day one," and watch metrics.

### 6. Reading verification / anti-gaming
A reading *competition* invites cheating; v2 anticipates abuse (rogue members, unauthorized access, the $250 booking ceiling). Summer Slide should specify how reading is verified (quizzes, timers, comprehension checks, parent confirmation) and how leaderboard manipulation is prevented — and fold the gaming rate into the guardrail metrics.

### 7. Metrics table with guardrails + an eval-driven roadmap
Convert the metric prompts into a table (metric · type · baseline · target · timeframe) with guardrails that must not get worse (e.g., verification-gaming rate, parent-reported pressure/stress, week-1 churn). Then build the roadmap the way v2 does: name the **single riskiest assumption**, define the MVP that tests it, set **quantified go/no-go gates and an eval harness** (especially for any AI recommendation quality), and add phases + rollback.

### 8. Non-goals, open questions with positions, stage checklist
Add a true "we are NOT building" list; an open-questions list with **working positions** and owners (pricing model, school vs. consumer GTM, content/book sourcing, age bands, prizes/incentive design); and a Stage-readiness checklist.

---

## Suggested next step

Filling Sections 1–3 (hypothesis + evidence-backed problem + real personas) plus the **AI behavior spec** and the **child-safety section** closes roughly two-thirds of the distance to the v2 bar. I can draft any of these directly into `prd.html` — the child-safety section and the AI behavior spec are the two I'd start with, since they're both load-bearing and currently empty.

---

*Sources: PRD-v2-NewVersion.md (uploaded) · [BuildtheCrew-PRD.md](https://docs.google.com/document/d/1ApqknSa6Rycp5MVsO_SzzRP9G6xlFzRG1pNtkJgyFoE/edit) · Summer Slide `prd.html` (Founders Hub).*
