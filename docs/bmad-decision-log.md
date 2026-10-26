---
type: deliverable
class: MIS 430
title: BMAD Decision Log — New College Course Navigator
deliverable: 9
status: running log — append as we go
started: 2026-10-26
---
# BMAD Decision Log

Deliverable 9. A running record of where we changed, overrode, or rejected BMAD's
output and why.

**How to use this file.** Append an entry at the time the decision is made, not in a
reconstruction at the end. Each entry should be liftable into that week's status
report with no rewriting. If a decision was later reversed, append a new entry rather
than editing the old one — the reversal is itself the finding.

**Standing context behind most overrides:** our final deliverable is an *interactive
mockup*, not a running system. BMAD's workflows assume you are shipping software, so
its defaults pull toward architecture, infrastructure, and non-functional
requirements. Divergence from those defaults is expected and is the main thing this
log records.

---

## Entry 1 — 2026-10-26 — Which `init` to run

**Category:** Tooling / disambiguation (not an override of generated content)

**BMAD's output:** The plugin exposes two initialization commands with near-identical
names, `/bmad:init` and `/bmad:bmad-init`, and no guidance distinguishing them.

**What we did:** Ran `/bmad:init`.

**Why:** Reading the plugin source showed these are not variants of one command, they
are two different systems. `/bmad:init` writes `bmad/config.yaml` plus
`planning-artifacts/`, which is what the user-invocable project workflows
(`create-prd`, `status`, `research`, `brainstorming`) actually read.
`/bmad:bmad-init` writes `_bmad/{module}/config.yaml` through a Python script and
serves the *BMad Builder* module — tooling for authoring new BMAD agents and modules,
which is not what we are doing. Running it would have produced a second, incompatible
config tree.

**Consequence:** None yet. Recorded because the ambiguity cost real time to resolve
and will recur for anyone picking the repo up.

---

## Entry 2 — 2026-10-26 — Rejected the Product Brief workflow

**Category:** Workflow step rejected

**BMAD's output:** BMAD's prescribed sequence for a Level 2 project is
Product Brief → PRD → Architecture → Epics/Stories. `/bmad:init` recommended
`/bmad:product-brief` as the next step.

**What we did:** Skipped the product brief entirely. Marked
`analysis.product-brief: not-applicable` in `workflow-status.yaml`. The PRD will be
seeded from the existing SOW instead.

**Why:** The SOW (deliverable 2) already does the brief's job — purpose, problem,
scope, prioritized requirements, risks — and unlike a BMAD brief it is a *graded*
artifact on a required course template. Generating a brief would have produced a
second document asserting the same things in different words, and the PRD would then
have descended from the duplicate rather than from the document we are actually
marked on. Two drifting sources of truth, no added information.

**Consequence:** The PRD inherits the SOW's known gaps rather than silently papering
over them: no "Won't have (this time)" row in the MoSCoW table, no advisor-side user
story despite advisors appearing in §3's *Who*, and risk likelihood ratings with no
evidence behind them. These are tracked as PRD open questions rather than quietly
resolved.

---

## Entry 3 — 2026-10-26 — Overrode the Level 2 architecture requirement

**Category:** Default overridden

**BMAD's output:** At project Level 2, BMAD marks `solutioning.architecture` as
**required** and will route to `/bmad:create-architecture` after the PRD.

**What we did:** Set `architecture: not-applicable` in `workflow-status.yaml` and
added `delivery_target: interactive-mockup` / `build_infrastructure: false` to
`bmad/config.yaml`.

**Why:** Deliverable 10 is a clickable mockup demonstrating the core feature. The
assignment states outright that building working AI is not required. An architecture
document would specify a retrieval pipeline, a data store, and a hosting model that
nobody will build and that feeds none of the 11 deliverables. BMAD cannot know this
constraint, so it has to be imposed from outside.

**Consequence:** We give up BMAD's architecture-to-story traceability. Accepted —
deliverable 5 grades stories on MoSCoW ranking, estimation reasoning, and acceptance
criteria, none of which depend on an architecture doc. Note that deliverable 4 (data
model, ER-style) still needs doing; it is a *course* artifact on a course format and
will be built directly, not derived from a BMAD architecture run.

---

## Entry 4 — 2026-10-26 — Project level set to 2 despite imperfect fit

**Category:** Judgment call on a BMAD input

**BMAD's output:** BMAD asks for a project level 0–4 and derives which artifacts are
required from it. Level 1 = 1–10 stories; Level 2 = 5–15 stories.

**What we did:** Chose Level 2.

**Why:** Neither level fits cleanly. Level 1 would have correctly made architecture
optional, but it also marks the PRD *optional* and a tech-spec *required* — and a
tech-spec is precisely the infrastructure-flavored artifact that is out of scope.
Level 2 gets the two important flags right (PRD required, tech-spec optional) and
gets exactly one flag wrong (architecture), which we overrode directly in Entry 3.
Fewer overrides, and the override we kept is explicit rather than buried in a level
number.

**Consequence:** Anyone reading `workflow-status.yaml` sees a Level 2 project with
architecture switched off, which looks inconsistent until they read this entry. That
is the intended tradeoff: visible and explained beats tidy and implicit.

---
