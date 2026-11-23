# Experience and workflow design — <project>
Status: PROPOSED / FOR USER REVIEW  
Version: <version>

## Design principles
<Speed, clarity, accessibility, safety and project-specific priorities>

## Research and inspiration (where applicable)
| Product / approach | Relevant workflow pattern | Lesson / trade-off | Source/date and evidence level | Adapt / avoid / unresolved |
| --- | --- | --- | --- | --- |
| <reference> | <observed, reported or inferred behavior> | <implication> | <source/date> | <decision> |

## Visual references
| Reference | Fidelity | Status | What it does / does not establish |
| --- | --- | --- | --- |
| <link/attachment> | EXPLORATORY | proposed | <not verified functionality> |

## Primary journey
| Step | Actor and starting state | Action | Resulting state | Alternative/error |
| --- | --- | --- | --- | --- |

## Screens / interaction surfaces
### Screen or surface: <name>
- **Purpose:**
- **Entry/exit:**
- **Visible content (unknown specifics use placeholders):**
- **Actions and state changes:**
- **Empty/loading/error and recovery states:**
- **Permissions and security (only known or proposed):**
- **Responsive/accessibility notes:**
- **Related requirements:** `REQ-...`

## Requirements
The linked canonical decision (`Decision ID`) controls approval status: `confirmed | proposed | open | rejected | deferred`. **Do not create a second requirement status**. Only requirements linked to `confirmed` decisions may define a stage's implementation acceptance tests.

| ID | Behavior / constraint | User-visible acceptance check | Decision ID |
| --- | --- | --- | --- |
| REQ-001 | <behavior> | <observable check> | D-... |

## Decisions (use ONLY if this is the canonical single-document project record)
If there is no `PROJECT.md` or existing authoritative decision register, maintain the *only* ledger here. Otherwise replace this section with a link to the canonical record, **not a copied second ledger**. Allowed statuses: **confirmed**, **proposed**, **open**, **rejected**, **deferred**.

| ID | Topic | Status | Decision or question | Rationale / source / date | Affected artifacts |
| --- | --- | --- | --- | --- | --- |
| D-001 | <topic> | open | <question> | <evidence and date> | <DESIGN / STAGE links> |

### Decision change notes (only if this document holds the ledger)
- `D-001` — <date>: Prior <status/decision> → current <status> because <dated evidence / user decision>.

## Current stage and approval state (single-document projects)
<Stage/status, what user authorized (if anything), any unapproved code changes or deployment boundaries; not implied by design acceptance. If PROJECT.md owns the decision record, link its approval state instead.>

## Edge cases, unknowns and rejected directions
<Reference decision IDs in the one ledger; identify blockers for next stage vs later-stage questions>
