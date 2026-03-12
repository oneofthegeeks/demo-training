# GoTo Connect Demo Scenarios Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Write 5 full GoTo Connect demo scenario documents with sample dialogue for Solution Consultant training.

**Architecture:** Each scenario is a standalone Markdown file in `docs/scenarios/`. Files follow a consistent structure: Business Context → Pain Points → Sample Dialogue → Trainer Notes. A companion `docs/scenarios/README.md` ties them together.

**Tech Stack:** Markdown, no code dependencies.

**Spec:** `docs/superpowers/specs/2026-03-12-goto-connect-demo-scenarios-design.md`

---

## File Structure

| File | Purpose |
|---|---|
| `docs/scenarios/README.md` | Index and trainer guide |
| `docs/scenarios/scenario-01-we-just-use-cell-phones.md` | Basic — personal cell phones, no business number |
| `docs/scenarios/scenario-02-dont-know-calls-we-miss.md` | Basic–Intermediate — missed call visibility |
| `docs/scenarios/scenario-03-clients-texting-personal-numbers.md` | Intermediate — business SMS |
| `docs/scenarios/scenario-04-need-to-look-more-professional.md` | Intermediate–Advanced — auto-attendant, IVR, hold music |
| `docs/scenarios/scenario-05-opening-second-location.md` | Advanced — multi-location, admin portal |

---

## Chunk 1: Scenario 1 + Scenario 2

### Task 1: Write Scenario 1 — "We Just Use Our Cell Phones"

**Files:**
- Create: `docs/scenarios/scenario-01-we-just-use-cell-phones.md`

- [ ] **Step 1: Write the scenario document**

Full content including: Business Context, Customer Profile, Pain Points to Surface, Sample Dialogue (full roleplay), Features to Demo callout, Trainer Notes.

- [ ] **Step 2: Review for SC usability**

Read through as if you are an SC with no prior context. Can you run this scenario cold? Is Taylor's persona clear? Does the dialogue feel natural?

- [ ] **Step 3: Commit**

```bash
git add docs/scenarios/scenario-01-we-just-use-cell-phones.md
git commit -m "feat: add scenario 1 - we just use cell phones"
```

---

### Task 2: Write Scenario 2 — "I Don't Know How Many Calls We Miss"

**Files:**
- Create: `docs/scenarios/scenario-02-dont-know-calls-we-miss.md`

- [ ] **Step 1: Write the scenario document**

Full content including: Business Context, Customer Profile, Pain Points to Surface, Sample Dialogue, Features to Demo callout, Trainer Notes.

- [ ] **Step 2: Review for SC usability**

Does the dialogue naturally surface the "lost bookings" fear before demoing reporting?

- [ ] **Step 3: Commit**

```bash
git add docs/scenarios/scenario-02-dont-know-calls-we-miss.md
git commit -m "feat: add scenario 2 - missed call visibility"
```

---

## Chunk 2: Scenario 3 + Scenario 4

### Task 3: Write Scenario 3 — "Clients Keep Texting Our Personal Numbers"

**Files:**
- Create: `docs/scenarios/scenario-03-clients-texting-personal-numbers.md`

- [ ] **Step 1: Write the scenario document**

Full content including: Business Context, Customer Profile, Pain Points to Surface, Sample Dialogue, Features to Demo callout, Trainer Notes. Include an optional objection for trainer use.

- [ ] **Step 2: Review for SC usability**

Does the dialogue surface both staff frustration AND client experience risk before demoing SMS?

- [ ] **Step 3: Commit**

```bash
git add docs/scenarios/scenario-03-clients-texting-personal-numbers.md
git commit -m "feat: add scenario 3 - business SMS"
```

---

### Task 4: Write Scenario 4 — "We Need to Look More Professional"

**Files:**
- Create: `docs/scenarios/scenario-04-need-to-look-more-professional.md`

- [ ] **Step 1: Write the scenario document**

Full content including: Business Context, Customer Profile, Pain Points to Surface, Sample Dialogue, Features to Demo callout, Trainer Notes. Include a competitor-pressure angle. Include an optional objection.

- [ ] **Step 2: Review for SC usability**

Does the demo walk through a full caller journey end-to-end?

- [ ] **Step 3: Commit**

```bash
git add docs/scenarios/scenario-04-need-to-look-more-professional.md
git commit -m "feat: add scenario 4 - auto-attendant and professional experience"
```

---

## Chunk 3: Scenario 5 + README

### Task 5: Write Scenario 5 — "We're Opening a Second Location"

**Files:**
- Create: `docs/scenarios/scenario-05-opening-second-location.md`

- [ ] **Step 1: Write the scenario document**

Full content including: Business Context, Customer Profile, Pain Points to Surface, Sample Dialogue, Features to Demo callout, Trainer Notes. This is the capstone — make sure it builds on all prior scenarios.

- [ ] **Step 2: Review for SC usability**

Does the demo position GoTo Connect as scalable infrastructure? Is the admin portal shown as Taylor's control center?

- [ ] **Step 3: Commit**

```bash
git add docs/scenarios/scenario-05-opening-second-location.md
git commit -m "feat: add scenario 5 - multi-location expansion"
```

---

### Task 6: Write README / Trainer Guide

**Files:**
- Create: `docs/scenarios/README.md`

- [ ] **Step 1: Write the README**

Include: overview of the training program, how to use the scenarios, Taylor's full customer profile, tips for trainers running the roleplay sessions, scenario index with one-line descriptions.

- [ ] **Step 2: Commit**

```bash
git add docs/scenarios/README.md
git commit -m "feat: add scenario trainer guide README"
```
