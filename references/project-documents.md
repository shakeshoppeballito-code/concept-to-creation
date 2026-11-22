# Project document selection and rules

## Document selection

**Small feature/fix:** Update the project's current document plus one bounded stage card. No new architecture document unless existing behavior or interfaces change materially.

**Moderate application/feature:** `PROJECT.md`, `DESIGN.md`, `BUILD_PLAN.md`, stage cards. Add `ARCHITECTURE.md` if nontrivial interfaces, data, security, storage, deployment or infrastructure choices must be defined.

**Large or regulated system:** Same core documents, with optional decision records, risk analysis, data contracts, accessibility and security plans where required by the project. Link, don't duplicate.

Use existing filenames/task IDs and source-of-truth rules where the user already has a project. Never silently overwrite accepted artifacts or create a competing task register.

## Content rules

- Explicitly distinguish: **confirmed requirement**, **recommendation**, **assumption**, **open question**, **rejected/deferred item**.
- Every significant requirement should have a stable ID (e.g. `REQ-001`); stage acceptance criteria reference the relevant IDs.
- Screen specs must state: purpose, entry points, visible information, allowed actions, state transitions, empty/loading/error states, accessibility and responsive behavior *when relevant*.
- When external research affected design, record source/date, which pattern was adapted or rejected, evidence strength, and user reaction in existing documents; do not create a redundant research report by default.
- Link source visuals and indicate their fidelity; a concept image is neither a functional prototype nor verified source behavior.
- Architecture records must distinguish known existing design from proposed decisions and constraints.
- Stage cards must preserve dependency order, test scope, required evidence and explicit owner/user approval boundaries.
- On revision, identify which requirements, screenshots, interfaces and stage cards are affected. Keep an update note; do not erase a historical decision to make the story seem cleaner.

Templates: `assets/PROJECT.md`, `assets/DESIGN.md`, `assets/ARCHITECTURE.md`, `assets/BUILD_PLAN.md`, `assets/STAGE.md`.
