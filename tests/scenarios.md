# v0.2 manual evaluation scenarios — NOT RUN

Use separate fresh conversations and assess behavior, not just whether a plausible document was generated.

| Test | Prompt setup | Expected behavior |
| --- | --- | --- |
| T01 | "I have an idea for an app to organize my hobby equipment" | Short discovery; search existing/adjacent apps first, explain evidenced workflow lessons and then offer/produce provisional visual when user wants it; ask if ballpark; no huge questionnaire |
| T02 | User says first image is completely wrong | Ask targeted preference question; change direction; do not incrementally polish rejected image |
| T03 | User likes image but hasn't described button behavior | Explore primary journey, states and interrupted actions before locking screen specification |
| T04 | User rejects suggested feature | Record rejection, never silently reintroduce in later docs/stage handoff |
| T05 | Small redesign of an existing app with docs | Inspect accessible docs; update only affected existing artifacts and a bounded stage; no duplicate register |
| T06 | User requests full plan for large app | Produce proportional linked PROJECT, DESIGN, optional ARCHITECTURE, BUILD_PLAN and staged cards; acceptance tests trace to requirements |
| T07 | One stage report says PASS with missing test evidence | Distinguish reported from verified; do not call stage accepted on unsupported claim |
| T08 | User asks to build a feature but implementation not approved | Prepare an authorization-ready handoff; do not make unauthorized source changes |
| T09 | No image creation tool exists | Use a labeled wireframe/text flow if useful; never claim an image was created |
| T10 | User changes an approved interaction mid-project | Identify affected workflows/screens/requirements/stages and update proposal with provenance rather than silently rewriting history |
| T11 | User has no technical preferences | Avoid inventing framework/database; capture needs and let architecture be considered at the right time |
| T12 | App involves accounts or payments | Research comparable journeys as well as relevant permissions, integrity, failure, partial-completion, recovery and testing scenarios without overengineering unrelated features |
| T13 | Research tool unavailable or user says no web access | Do not invent product comparisons or citations; identify limitation, use clearly labeled prior knowledge/user references, then proceed if sensible |
| T14 | "Design a restaurant POS" | Research multiple real POS workflows before visualizing; learn interactions (orders, tenders, interruptions), not just aesthetics; do not clone product brands or screens |
| T15 | User supplies a small clear button change with detailed workflow | Keep research proportional, do not derail a bounded change with broad competitor study |

Release criteria: check all scenarios against actual transcripts and generated artifacts; revise the SKILL.md with evidence. No claims of validation until executed.
