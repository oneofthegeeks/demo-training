# GoTo Connect Demo Training

Roleplay scenarios and scoring materials for Solution Consultant demo training. SCs practice live GoTo Connect demos in a structured roleplay format with Taylor (owner of Shear Bliss Salon) as the customer.

---

## What's in This Repo

```
docs/
  scenarios/
    README.md                                        # Trainer guide + how to run sessions
    scenario-01-we-just-use-cell-phones.md           # Basic
    scenario-02-dont-know-calls-we-miss.md           # Basic–Intermediate
    scenario-03-clients-texting-personal-numbers.md  # Intermediate
    scenario-04-need-to-look-more-professional.md    # Intermediate–Advanced
    scenario-05-opening-second-location.md           # Advanced
  rubric/
    scoring-rubric.md                                # Demo2Win-based scoring rubric
  superpowers/
    specs/                                           # Design documentation
    plans/                                           # Implementation plans
CLAUDE.md                                            # AI assistant context file
```

---

## How to Use This for Training

### For Trainers Running a Session

1. **Pick a scenario** — Start with Scenario 1 for new SCs. Use the complexity ratings to match the scenario to the SC's experience level.
2. **Read the Trainer Notes** — Each scenario has a Trainer Notes section at the bottom. Read it before the roleplay. It tells you what good looks like, what mistakes to watch for, and optional objections to introduce.
3. **Give the SC the Business Context** — Share only the Business Context section with the SC before the session. Do not share the Pain Points to Surface or Sample Dialogue — those are for trainer reference.
4. **Run the roleplay** — You play Taylor. Use the Sample Dialogue as a guide for how the conversation should feel, but don't read from it. Respond naturally based on what the SC asks.
5. **Score with the rubric** — Use `docs/rubric/scoring-rubric.md` during or immediately after the session. Fill in scores and written notes.
6. **Debrief** — Follow the Debrief Guide at the bottom of the rubric. Keep it to 10 minutes. Focus on one thing to improve.

### Running All 5 Scenarios as a Full Arc

The scenarios are designed to build on each other. Taylor's situation evolves from Scenario 1 through Scenario 5. Running them in order over multiple sessions simulates a real customer's journey and progressively tests more advanced GoTo Connect features.

### For the SC Being Trained

You'll be given a Business Context for the session. Your job is to have a real conversation with Taylor — ask questions, understand his situation, then demo GoTo Connect in a way that's relevant to what he told you.

**The one rule:** Don't start demoing until you understand his pain. Discovery before demo, every time.

---

## The Customer: Taylor

Taylor owns **Shear Bliss Salon** — a small 6-person salon. He's friendly, practical, and non-technical. He doesn't know phone system terminology. He cares about his clients, his team, and his business.

Use his language:
- "clients" (not customers)
- "bookings" (not leads)
- "my team" or "my stylists" (not employees)

Full persona details are in `docs/scenarios/README.md`.

---

## Scoring

Scoring is based on **Demo2Win methodology** by Peter Cohan. Each session is scored across 13 criteria in 5 sections, with a maximum of 52 points.

---

### Section 1: Discovery & Situation Fluency
*Did the SC listen before showing anything?*

| Criterion | What's Being Evaluated |
|---|---|
| 1A — Asked before telling | Did the SC ask 3+ open questions and hold back the demo until real pain was on the table? |
| 1B — Uncovered specific pain | Did the SC get to a concrete business consequence Taylor named himself — not just the symptom? |
| 1C — Adapted to emotional state | Did the SC read Taylor's mood and match it — urgency with urgency, frustration with empathy? |

---

### Section 2: The "So What?" Test
*Did every feature connect to Taylor's stated problem?*

| Criterion | What's Being Evaluated |
|---|---|
| 2A — Features linked to pain | Was every feature shown tied directly to something Taylor said during discovery? |
| 2B — Taylor's language, not product language | Zero unexplained jargon — did the SC speak in bookings, clients, and stylists, not VoIP terms? |
| 2C — Outcomes, not features | Was each demo point framed as a business result, not just a product walkthrough? |

---

### Section 3: Wow / How / Now Structure
*Did the demo have a clear arc?*

| Criterion | What's Being Evaluated |
|---|---|
| 3A — Created interest (Wow) | Did the SC create a moment of anticipation before each demo point — not just open and click? |
| 3B — Demo was focused (How) | Was the demo tight and relevant, with no rabbit holes or unrequested features? |
| 3C — Prompted next step (Now) | Did the SC check for resonance after each point and end with a clear call to action? |

---

### Section 4: Objection Handling
*Scored only if an objection was introduced — otherwise marked N/A.*

| Criterion | What's Being Evaluated |
|---|---|
| 4A — Acknowledged before responding | Did Taylor feel heard before the SC responded — or did the SC immediately counter? |
| 4B — Business context, not product defense | Did the response connect back to Taylor's situation, or was it a generic product defense? |

---

### Section 5: Presence & Confidence
*Did the SC own the room without dominating it?*

| Criterion | What's Being Evaluated |
|---|---|
| 5A — Owned without dominating | Was it a conversation, not a presentation? Did the SC stay in control without doing all the talking? |
| 5B — Recovered from off-script moments | When Taylor pushed back or went sideways, did the SC stay calm and use it to learn more? |

---

### Performance Bands

| Score (with objection) | Score (without objection) | Band |
|---|---|---|
| 47–52 | 40–44 | **Demo-Ready** — can run live customer demos with light coaching |
| 39–46 | 33–39 | **Developing** — strong foundations; 2–3 areas to sharpen before going live |
| 28–38 | 24–32 | **Building** — needs structured practice; not ready for live demos alone |
| Below 28 | Below 24 | **Foundational** — revisit core Demo2Win principles before continuing |

Full scoring rubric with 4-point behavioral descriptions, score sheets, and debrief guide: [`docs/rubric/scoring-rubric.md`](docs/rubric/scoring-rubric.md)

---

## How to Contribute

### Adding or Updating a Scenario

1. Read the existing scenarios to understand the format before making changes
2. Every scenario must have all required sections — see the format in `CLAUDE.md`
3. Sample dialogue should feel like a real sales conversation, not a script
4. Objections go in the **Optional objections for trainer use** block in Trainer Notes
5. Submit changes as a pull request with a clear description of what changed and why

### Adding a New Scenario

Copy the structure of an existing scenario file. The filename format is:
`scenario-NN-short-description-of-pain.md`

Update `docs/scenarios/README.md` to add the new scenario to the index table.

### Updating the Rubric

The rubric is versioned. If you update scoring criteria:
- Update the version number and date at the bottom of `docs/rubric/scoring-rubric.md`
- Note what changed in your PR description so trainers know to re-calibrate

### Updating the Customer Persona

If Taylor's backstory or characteristics change:
- Update `docs/scenarios/README.md` (Customer Profile section)
- Update `CLAUDE.md` (Customer Persona section)
- Update any scenario files where the change affects the Business Context

### Pull Request Guidelines

- PRs should be small and focused — one scenario or one section at a time
- Include a brief description of the change and the rationale
- If you're updating Sample Dialogue, note whether you tested the new version in a live session

---

## Working with AI Assistance

This repo includes a `CLAUDE.md` file that gives Claude (the AI assistant) full context about the project — the persona, the format, the principles, and what's pending. If you're using Claude Code to work on this repo, it will automatically load that context.

To add a new scenario or make changes with Claude, just describe what you want to change and it will follow the established format and principles without needing to be re-briefed.

---

## Roadmap

- [x] 5 roleplay scenarios (basic to advanced)
- [x] Demo2Win scoring rubric
- [ ] SC self-assessment checklist (pre-session prep)
- [ ] Video example recordings of Scenario 1 (good and bad run)
- [ ] Additional verticals beyond salon (dental, auto shop, law firm)
- [ ] Facilitator certification guide for new trainers

---

## Questions or Feedback

Open an issue in this repo or reach out to the repo owner directly.
