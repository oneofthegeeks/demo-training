# GitHub Pages Site Implementation Plan

> **For agentic workers:** REQUIRED: Use superpowers:subagent-driven-development (if subagents available) or superpowers:executing-plans to implement this plan. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a single `index.html` at the repo root that renders all training content as a navigable GitHub Pages site.

**Architecture:** Single HTML file with embedded CSS and JS. Hash-based routing (`#home`, `#scenario-1`, etc.) swaps page content without reloads. All scenario and rubric content is embedded directly as JS data — no Markdown parsing, no build tools, no external dependencies beyond Google Fonts.

**Tech Stack:** Vanilla HTML/CSS/JS, Google Fonts (Nunito Sans), GitHub Pages (main branch root)

---

## Chunk 1: Shell, Routing, and Sidebar

### Task 1: Create index.html with brand styles and layout shell

**Files:**
- Create: `index.html`

- [ ] Create `index.html` with the following:
  - `<head>`: Nunito Sans from Google Fonts, GoTo brand CSS variables (`--purple: #6633CC`, `--teal: #00C8CB`), base reset, layout styles
  - Two-column layout: fixed left sidebar (240px) + scrollable main content area
  - Sidebar: GoTo logo text "Shear Bliss Training", nav links for Home, 5 Scenarios, Scoring Rubric
  - Mobile responsive: sidebar collapses to top nav on small screens
  - Empty `<main id="content">` div where router injects pages

- [ ] Open `index.html` in browser, verify:
  - Sidebar renders with purple background
  - GoTo teal accent on active/hover nav items
  - Main area is blank but layout is correct
  - No console errors

- [ ] Commit:
  ```bash
  git add index.html
  git commit -m "feat: add index.html shell with GoTo brand styles and sidebar"
  ```

### Task 2: Add hash-based router

**Files:**
- Modify: `index.html`

- [ ] Add JS router to `index.html`:
  - `const routes = { 'home': renderHome, 'scenario-1': ..., ... }`
  - `function navigate(hash)` — reads `location.hash`, calls matching render function, injects into `#content`
  - Listen on `hashchange` and `DOMContentLoaded`
  - Default route: `#home`
  - `setActiveNav(hash)` — adds `.active` class to correct sidebar link

- [ ] Verify routing works:
  - Visit `#home`, `#scenario-1`, `#rubric` in browser
  - Each renders a placeholder `<h1>` with the route name
  - Active nav item highlights correctly
  - Browser back/forward buttons work

- [ ] Commit:
  ```bash
  git add index.html
  git commit -m "feat: add hash-based JS router with sidebar active state"
  ```

---

## Chunk 2: Home Page and Scenario Page Components

### Task 3: Build reusable scenario page renderer

**Files:**
- Modify: `index.html`

- [ ] Add CSS for scenario page components:
  - `.complexity-badge` — pill badge, color-coded: Basic=gray, Basic–Intermediate=blue, Intermediate=teal, Intermediate–Advanced=orange, Advanced=purple
  - `.customer-profile` — two-column table with subtle border
  - `.pain-points-callout` — yellow/amber left-border callout box with "Trainer: Surface these through questions" label
  - `.dialogue` — chat bubble container
  - `.bubble.sc` — left-aligned bubble, light gray background, "SC" label
  - `.bubble.taylor` — right-aligned bubble, GoTo purple background, white text, "Taylor" label
  - `.features-list` — clean bulleted list with teal checkmarks
  - `.trainer-notes` — light gray section
  - `.objection` — collapsible `<details>`/`<summary>` element, styled with teal border

- [ ] Add `function renderScenarioPage(scenario)` that takes a scenario data object and returns an HTML string using all the above components

- [ ] Verify with a hardcoded test scenario object in browser — all components render correctly

- [ ] Commit:
  ```bash
  git add index.html
  git commit -m "feat: add scenario page renderer and CSS components"
  ```

### Task 4: Add Home page

**Files:**
- Modify: `index.html`

- [ ] Add `function renderHome()`:
  - Heading: "GoTo Connect Demo Training"
  - Subheading: "Solution Consultant Roleplay Scenarios"
  - Brief description: what this site is and how to use it
  - Scenario overview table: Name | Complexity | Features Practiced (5 rows)
  - Link/note about the Scoring Rubric

- [ ] Navigate to `#home`, verify layout looks clean and on-brand

- [ ] Commit:
  ```bash
  git add index.html
  git commit -m "feat: add home page with scenario overview table"
  ```

---

## Chunk 3: All 5 Scenario Pages

### Task 5: Embed Scenario 1 data and page

**Files:**
- Modify: `index.html`

- [ ] Add `const scenario1 = { ... }` data object with all fields:
  - `title`, `complexity`, `features` (array)
  - `businessContext` (string)
  - `customerProfile` (array of `[label, value]` pairs)
  - `painPoints` (array of strings)
  - `dialogue` (array of `{ speaker: 'SC'|'Taylor', text: string }`)
  - `featuresDemo` (array of `{ name, description }`)
  - `trainerNotes` (object: `whatGood`, `mistakes`, `objections` array)

- [ ] Wire `routes['scenario-1']` to call `renderScenarioPage(scenario1)`

- [ ] Navigate to `#scenario-1`, verify all sections render:
  - "Basic" badge in gray
  - Customer profile table
  - Pain points callout box
  - Alternating SC/Taylor chat bubbles
  - Features demoed list
  - Trainer notes + 3 collapsible objections

- [ ] Commit:
  ```bash
  git add index.html
  git commit -m "feat: embed scenario 1 content"
  ```

### Task 6: Embed Scenarios 2–5

**Files:**
- Modify: `index.html`

- [ ] Add `scenario2`, `scenario3`, `scenario4`, `scenario5` data objects following the same structure as `scenario1`
- [ ] **Fix Jenna pronoun error in scenario5 dialogue:** The line "When he's at Westside, he's in the Westside queue. When he's back at the original location, she flips it." should read "When she's at Westside, she's in the Westside queue. When she's back at the original location, she flips it."
- [ ] Wire routes `scenario-2` through `scenario-5`
- [ ] Verify each page in browser:
  - Correct complexity badge and color for each
  - S2: "Basic–Intermediate" badge
  - S3: "Intermediate" badge
  - S4: "Intermediate–Advanced" badge
  - S5: "Advanced" badge in purple
  - All dialogue, objections, and trainer notes render

- [ ] Commit:
  ```bash
  git add index.html
  git commit -m "feat: embed scenarios 2-5 content, fix Jenna pronoun in S5"
  ```

---

## Chunk 4: Scoring Rubric Page and Final Polish

### Task 7: Embed Scoring Rubric page

**Files:**
- Modify: `index.html`

- [ ] Add `function renderRubric()`:
  - Page title: "GoTo Connect Demo Scoring Rubric"
  - Subheading: "Based on Demo2Win Methodology by Peter Cohan"
  - Scoring scale table (1–4 definitions)
  - All 5 sections with criteria, behavior tables, and score fields
  - Scoring Summary table
  - Performance Bands (with and without objection)
  - Debrief Guide for Taylor
  - CSS for rubric: `.rubric-section`, `.criteria-table`, `.score-field`

- [ ] Navigate to `#rubric`, verify:
  - All 13 criteria render with behavior tables
  - Performance bands table is clear and readable
  - Debrief guide section is present

- [ ] Commit:
  ```bash
  git add index.html
  git commit -m "feat: embed scoring rubric page"
  ```

### Task 8: Final polish and mobile check

**Files:**
- Modify: `index.html`

- [ ] Visual polish pass:
  - Verify page titles use the right heading hierarchy
  - Check that all chat bubbles have consistent padding and max-width
  - Confirm complexity badge colors are visually distinct
  - Verify collapsible objections have a visible expand indicator (▶)
  - Add `<title>Shear Bliss Demo Training</title>` and favicon emoji via `<link rel="icon">`

- [ ] Mobile check (resize browser to 375px width):
  - Sidebar collapses cleanly
  - Content is readable without horizontal scroll
  - Chat bubbles don't overflow

- [ ] Commit:
  ```bash
  git add index.html
  git commit -m "chore: final polish and mobile layout fixes"
  ```

### Task 9: Push to GitHub and activate Pages

**Files:**
- None (git operations only)

- [ ] Push to main:
  ```bash
  git push origin main
  ```

- [ ] Verify GitHub Pages activation instructions:
  - Go to repo Settings → Pages → Source: Deploy from branch → Branch: main → Folder: / (root) → Save
  - Live URL: `https://oneofthegeeks.github.io/demo-training`

- [ ] After ~60 seconds, visit the live URL and verify site loads
