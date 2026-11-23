# Project documentation selection and maintenance

## Pacing: zero files first, structure when it earns its place

| Situation | Default deliverable |
| --- | --- |
| Casual idea/early exploration | **Zero files**. Natural discussion, appropriate research, optional early depiction and short in-chat decisions recap. |
| Small UI/workflow redesign before handoff | **One existing design document**, or `DESIGN.md` with `## Decisions` if no canonical project register exists. |
| Small redesign ready for an agent | Update design and add **one** `assets/STAGE.md`-based stage card; do not invent `ARCHITECTURE.md` when technical contracts don't change. |
| New application needing a multi-stage build | `PROJECT.md`, `DESIGN.md`, `BUILD_PLAN.md`; add `ARCHITECTURE.md` only for consequential new technical boundaries, and draft stage cards as each stage nears execution. |
| Large or regulated system | Above with focused extra evidence, data, risk, security and accessibility contracts **only where justified**. |

Do not create files simply because templates exist. Preserve the user's existing project filenames, task IDs and authoritative sources; link instead of duplicating. Documentation is not permission to implement.

## One canonical decision ledger

- From the first meaningful decision, maintain `confirmed / proposed / open / rejected / deferred` in chat; at persistence time write them to **one** document.
- `PROJECT.md` is the preferred durable ledger; if an existing project register is authoritative, use that. For a single-doc small change without `PROJECT.md`, use `DESIGN.md`'s `## Decisions` table with the same columns.
- **Exact columns:** `ID | Topic | Status | Decision or question | Rationale / source / date | Affected artifacts`.
- On a changed decision, retain the ID and a dated history of its prior status/rationale; update the current status to `open` or `proposed` when new evidence challenges it. Do not silently delete rejection or rewrite a previously confirmed decision as if it never existed.
- If a project later grows a `PROJECT.md`, migrate/link the ledger; do **not** maintain competing copies. Other document summaries are views referencing `D-###`.

## Consistency

- Requirements receive stable `REQ-###` IDs and a link to the canonical `D-###` decision. Their approval status is **derived from that decision**, not stored independently in `DESIGN.md`. Only `confirmed` requirements can anchor implementation acceptance tests.
- Central journeys identify user, start state, action, result and relevant error/empty/cancellation/recovery behavior; deepen only when it affects current decisions.
- Research impacting design records a source/date and whether behavior was observed, third-party reported, or inferred. A visual concept alone is not evidence of runtime behavior.
- Technical documents distinguish inspected existing behavior, user reports, proposed design and unresolved choices.
- Stage cards **follow `assets/STAGE.md`**, including prerequisites, changed surfaces, exclusions, compatibility/rollback, evidence, approval and stop conditions.
- A mid-stage failure that invalidates earlier design sends the work back to discovery; update affected requirements and *future/proposed* stages, retain the original stage evidence and require user review of revised scope.

## Delivery

- **Authorized existing workspace/repository:** Write files in the established docs structure and make changes reviewable. Preserve accepted documents and avoid unsolicited publication.
- **No workspace write permission:** Deliver clearly named downloadable files when tooling supports them, otherwise complete ready-to-save Markdown. Be accurate about what was saved.
- **Still exploring:** Keep the working understanding in chat; offer to persist it only when it helps resumption or a handoff.

Templates: `assets/PROJECT.md`, `assets/DESIGN.md`, `assets/ARCHITECTURE.md`, `assets/BUILD_PLAN.md`, `assets/STAGE.md`.
