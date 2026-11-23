# Quality and readiness gates

These are checkpoints at the **appropriate maturity**, not a checklist to dump into an opening conversation.

## Gate 0 — Research (SKILL.md threshold)
- A new app, new screen, or changed user journey/interaction receives a targeted comparison **before** early depiction, unless research was legitimately reused, skipped by the user, unavailable, narrow/urgent or already satisfactorily completed. Record the reason for a skip.
- Research examines workflow behavior where evidence allows, not merely visual styles; source claims are dated and qualified.
- Inspiration is adapted without copying protected artwork, branding, or product text.

## Gate 1 — Exploration and visual direction
- The user can identify what fits or doesn't fit; an early depiction is labeled `EXPLORATORY` and is not assumed approved.
- All unprovided real-world particulars (including prices, names, personal information, permissions, financial rules) are placeholders, not invented facts.
- **Zero-file mode** remains valid until the user needs durable files or an implementation handoff.

## Gate 2 — Workflow readiness for the next handoff
- The **stage-relevant** journeys have actor/start state/action/result and consequential exceptions, permissions and recovery.
- Unanswered *nonblocking* questions may remain labeled open; material conflicts and blockers cannot be silently delegated to a coding agent.
- Visual approval is **not** workflow approval.

## Gate 3 — Documentation coherence
- One canonical ledger exists **when documents are necessary**: `PROJECT.md`, authorized existing register, or `DESIGN.md` for small single-document changes. Significant decisions had been tracked in chat before persistence.
- Design and optional technical/build files reference stable decision/requirement IDs, preserve history and do not contradict each other.
- Document choice is proportional; saved locations and unsaved draft limits are accurately reported.

## Gate 4 — Stage ready for coding agent
- `assets/STAGE.md` governs the card and includes changed surfaces, dependencies, exclusions/protections, compatibility/rollback, measurable tests, evidence, unknowns/stop conditions and approval gate.
- **Hard readiness rule:** Every acceptance criterion traces to `confirmed` requirements/decisions. A stage-defining `proposed` or `open` behavior/dependency means **BLOCKED FOR DESIGN**, not a handoff. Reversible assumptions are allowed while exploring, never as a substitute for confirmed behavior in coding-stage acceptance tests. See `SKILL.md` and `assets/STAGE.md`.
- Respect the approval chain: visual ≠ workflow; workflow ≠ code authorization; stage acceptance ≠ next stage authorization or deployment.

## Gate 5 — Report review and pivots
- Summary-only claims default to **`REPORTED`**; **`INSPECTED`** is an artifact provenance note, not an acceptance status. **`VERIFIED`** requires evidence directly supporting the specific criterion.
- Explicitly distinguish **`NOT RUN`**, **`BLOCKED`**, and **`FAILED`**; a passing build does not prove the stage is accepted.
- If a failed test invalidates a confirmed design, preserve history, mark the current decision open/proposed, pause affected work, revise dependent specs/stages after user review, and do not silently restart, deploy or override completed work.
