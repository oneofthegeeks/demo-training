# CLAUDE.md — Demo Training Project

## What This Project Is
GoTo Connect Solution Consultant training materials. The goal is to give SCs realistic roleplay scenarios for demoing GoTo Connect to a small business customer named Taylor (owner of Shear Bliss Salon).

## Project Structure
```
docs/
  scenarios/
    README.md                                      # Trainer guide + assessment rubric
    scenario-01-we-just-use-cell-phones.md         # Basic
    scenario-02-dont-know-calls-we-miss.md         # Basic–Intermediate
    scenario-03-clients-texting-personal-numbers.md # Intermediate
    scenario-04-need-to-look-more-professional.md  # Intermediate–Advanced
    scenario-05-opening-second-location.md         # Advanced
  superpowers/
    specs/2026-03-12-goto-connect-demo-scenarios-design.md
    plans/2026-03-12-goto-connect-demo-scenarios.md
```

## Customer Persona: Taylor
- Owner of Shear Bliss Salon, small team of 6 (grows to 8 in Scenario 5)
- Started with no phone system — all personal cell phones
- Friendly, practical, non-technical
- Use her language: "clients" (not customers), "bookings" (not leads), "my team" (not employees)
- Decision maker — no approvals needed from others

## Core Training Principles (never violate these)
1. **Discovery before demo** — SCs must surface the pain through questions before showing any feature
2. **No jargon** — Taylor doesn't know VoIP, SIP, PBX, softphone, hosted telephony
3. **Features tied to outcomes** — every demo point connects back to a business problem Taylor named
4. **No click-path instructions** — SCs figure out the UI themselves; Taylor coaches after the fact

## Scenario Format (every scenario must have)
- Business Context (Taylor's mindset going in)
- Customer Profile table
- Pain Points to Surface (bulleted, for SC to uncover — not state)
- Sample Dialogue (full roleplay, discovery through demo)
- Features Demoed (bulleted)
- Trainer Notes (what good looks like, SC mistakes to watch for, optional objections)

## Objections
Each scenario has 3 optional objections in Trainer Notes. These are for trainers to introduce after SCs have the basic flow. Don't introduce objections on the first run of a scenario.

## Scoring Rubric
- File: `docs/rubric/scoring-rubric.md`
- Based on Demo2Win methodology (Peter Cohan)
- 13 scored criteria across 5 sections, 52 points max
- 4 performance bands: Demo-Ready, Developing, Building, Foundational
- Includes debrief guide for Taylor to use after each session
- Version: v1.0 — update version number at bottom of file when criteria change

## Pending Work
- Taylor to review all 5 scenarios and provide feedback
- Refine rubric after first live training session
- Roadmap: SC self-assessment checklist, video examples, additional verticals (dental, auto shop, law firm)

## How to Make Changes
- To update a scenario: read it first, then edit only what changed — don't rewrite the whole file
- To add a new scenario: follow the exact format of existing scenarios
- To add objections: add to the "Optional objections for trainer use" block in Trainer Notes
- To update the persona: update both this file AND `memory/MEMORY.md`
