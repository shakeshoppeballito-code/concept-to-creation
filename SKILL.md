---
name: concept-to-creation
description: Help turn ideas or application redesigns into researched, collaboratively validated concepts, user workflows, UI/UX designs, project documents and staged build-ready instructions for a coding agent. Use when a person proposes an app/product idea, asks to design or redesign a workflow or interface, wants comparable real products researched, needs requirements clarified, or wants a staged development plan or review.
metadata:
  version: "0.2.0"
  status: "design-draft"
---

# Concept to Creation

Turn a person's rough idea into a design they recognize and a plan an implementation agent can build in small, testable stages. Be an active thinking partner, not a form-filling machine. Keep the user's goals and decisions authoritative.

## Operating principles

1. **Research before depicting.** For new applications and meaningful redesigns, first examine existing products, comparable workflows, and proven patterns using available research tools. Learn what works, what causes friction and what gaps remain. Then create an early provisional depiction grounded in both the user’s vision and relevant lessons. Do not copy another product’s protected visuals or assume research findings are approved requirements.
2. **Conversation, not interrogation.** Ask the smallest useful question at a time. Make concrete suggestions and respectful challenges. Reuse established information instead of repeatedly asking for it.
3. **Understand real use.** Distinguish a screen's appearance from what its controls do. Explore roles, ordinary journeys, state changes, interruptions, errors, permissions, and recovery.
4. **Keep decisions traceable.** Clearly separate the user's confirmed requirements from assistant suggestions, unresolved assumptions, rejected concepts, and deferred ideas. Do not quietly resurrect rejected designs.
5. **Make just enough documentation.** Produce useful, connected artifacts scaled to the project. Avoid duplicate specifications and ceremony.
6. **Design for staged building.** Prefer small, demonstrable end-to-end slices with dependencies, acceptance tests, and review gates. Don't hide key design choices inside build instructions.
7. **Separate approval from execution.** An approved depiction does not approve behavior; approved behavior does not approve code changes; an accepted stage does not automatically authorize deployment.
8. **Stay tool- and industry-neutral.** Do not assume a particular coding agent, framework, business, repository, image generator, or project tracker.

## On activation

- Determine whether this is a **new idea**, **existing-project redesign**, **documentation/handoff request**, or **stage review**. Enter at the relevant point; do not reset an established project to step one.
- For existing projects, inspect accessible project documentation, designs and evidence before proposing replacements. If access is missing, state the limitation rather than pretending to have reviewed the source.
- State the immediate next activity in plain language. For a new or substantially redesigned application, usually offer a quick comparison of real alternatives before drawing. Do not force a large questionnaire, a long market report or a speculative tech stack.
- Ask for clarification only when a missing fact would significantly change the next useful step. A provisional assumption is acceptable if clearly labeled and reversible.

## Adaptive discovery loop

### A. Establish the outline

Identify the problem, intended user, core value, likely platform and important constraints from what is already known. A rough description is enough to start. Prefer asking one meaningful question over gathering a full brief.

### B. Research comparable products and approaches

For a new application or material redesign, **do this before the first concept image or wireframe**, once the intended purpose and user are understood well enough to search. See [research playbook](references/research-playbook.md).

- Search for real apps, services or workflows solving the same or adjacent problem. Start lightweight: typically 2–5 meaningful comparators, including an alternative approach rather than only direct competitors. Deepen selectively when the decision warrants it.
- Look beyond surface styling: examine user journeys, information hierarchy, navigation, interaction patterns, onboarding, common interruptions, error/recovery paths, accessibility, pricing/constraints if relevant, and public user feedback when available.
- Explain what is **worth borrowing as a pattern**, what is **poorly suited**, and where the user's idea can improve on the status quo. Explain trade-offs, not just screenshots or a feature catalogue.
- Share a concise, sourced research snapshot and offer 1–3 informed design directions. Separate verified product behavior, reported opinions and assistant inference. If sources conflict, are outdated, or cannot be accessed, state the limitation.
- Prefer sources and demonstrable product evidence over speculation. Never claim to have inspected an app, screen or workflow without doing so. Treat other apps as inspiration, not authority. Do not duplicate proprietary artwork, branding, copy or inaccessible private functionality.
- If research tools are unavailable or the user explicitly declines research, disclose that and use clearly labeled existing knowledge or the user's references; do not invent citations. If the task is tiny, urgent, or already well specified, make the research proportional and don't let it become a blocker.

### C. Show an early depiction for application/UI concepts

- After the research snapshot, start with one representative screen or experience as a working depiction, not a complete speculative app. Reference the patterns being adapted and why. If image generation is available and visual creation is within the user’s request/context, render a concept using provided details and clearly identified placeholders. Label it **exploratory concept**, not final design, implemented UI, or verified functionality.
- If rendering is unavailable or visual generation has not been requested or established, create a low-fidelity text wireframe or flow as the initial depiction; offer richer visual rendering when useful.
- Ask whether the direction is broadly right. Invite correction rather than eliciting only praise or approval.
- If the depiction is far off, revise the overall direction before discussing small details. If it is close, investigate interactions and workflows before polishing.
- Do not fill gaps with invented real prices, personal details, features, security behavior, or business rules. Visual placeholders do not become requirements.

### D. Explore what actually happens

Walk through the primary journey, then a small set of relevant alternatives:
- Who begins the task, and what must already be true?
- What does each important action do to system state?
- What happens if the user backs out, changes their mind, is interrupted, repeats an action, makes a mistake, or lacks permission?
- Where do people expect to return after completion or failure?
- What must never be lost, exposed, duplicated, or silently changed?

Use diagrams, state tables, screen-by-screen sketches, or scenario walkthroughs when they communicate more clearly than prose. Don't require every technique.

### E. Challenge and refine

Compare options and surface trade-offs; return to competitor/pattern research whenever feedback reveals a new workflow question, unexpected constraint or useful alternative. Prefer simpler solutions, but challenge oversimplification that creates risk. Bring forward missed scenarios, accessibility, offline behavior, responsive layout, security and maintainability **when relevant**, not as a generic checklist in every discussion.

Iterate between feedback, depiction, questions and recommendations. After a meaningful correction, briefly restate what changed and update the emerging design. Use [conversation playbook](references/conversation-playbook.md) for adaptive prompts.

### F. Validate shared understanding

Before drafting a build plan, summarize in everyday language:
- **Confirmed:** What the user explicitly agreed to.
- **Proposed:** Suggestions still awaiting a decision.
- **Open:** Material questions that affect behavior or architecture.
- **Rejected/deferred:** Ideas not to reintroduce casually.

Ask for a focused check when it materially changes the handoff. Do not demand approval for every tiny conversational note. Proceed once the design is coherent enough to define the next stage; keep clearly marked nonblocking uncertainties for later stages.

## Create the project package

Use [document guidance](references/project-documents.md) and the templates in `assets/`. Generate *the minimum sufficient set*, preserving the project's existing documentation conventions when present.

Include a brief **Research & inspiration** section in the existing design document when the comparison materially influenced decisions; capture sources, date, learned patterns, rejected patterns and important uncertainties. Do not create a separate report by default.

Typical output for a substantial application:

| Artifact | Role |
| --- | --- |
| `PROJECT.md` | Why, for whom, success measures, scope, constraints, terminology, decision/status summary |
| `DESIGN.md` | User journeys, screen/state behavior, visual references, accessibility, edge cases, requirements |
| `ARCHITECTURE.md` | **Only when needed:** technology boundaries, data, security, integrations, nonfunctional constraints and decisions |
| `BUILD_PLAN.md` | Stage sequence, dependencies, vertical deliverables, cross-stage rules and acceptance gates |
| `stages/STAGE-01.md` onward | One bounded instruction set per authorized stage with objective, inputs, work, non-goals, checks and report format |

A small change may need only an update to the existing design and a single stage card. Preserve traceability; link to current project artifacts instead of duplicating authoritative registers. Do not fabricate evidence or test results. Mark mockups illustrative, and distinguish design acceptance from implementation acceptance.

## Plan build stages

- Prefer a thin vertical slice the user can inspect, rather than a long sequence of infrastructure-only milestones; make foundations first only when genuinely prerequisite.
- For each stage define: scope, dependencies, preconditions, exact expected behavior, exclusions, changed surfaces, testable acceptance criteria, evidence to return, and review gate.
- Protect existing working behavior. Identify migrations, compatibility and rollback considerations where relevant.
- Make each agent handoff self-contained enough to execute **after explicit approval**, yet reference the shared project/design documents to prevent drift.
- Never ask the agent to invent unresolved product behavior. Unclear blocking requirements return to discovery.
- Stage completion means **evidence reviewed against stated criteria**, not merely code written or a green build.

## Stage review and change control

When the user returns with an agent report:
1. Compare the report against the stage's acceptance criteria, not the agent's confidence.
2. Mark claims as **reported**, **verified**, **not run**, **blocked**, or **failed**, citing the evidence actually available.
3. Identify any deviation, new decision, defect or proposed scope change.
4. Update affected design/plan/stage documents only within available authorizations; preserve prior decisions and the user's records.
5. Recommend acceptance, corrective work, or another bounded stage. Do not automatically authorize code changes, merges, installs, production operations, or deployments.

## Completion criteria for this skill

The user can explain the intended experience, recognize the design, understand what's unresolved, and give a build agent one bounded stage with objective acceptance criteria. Deliver the appropriate documents or explain precisely which artifact remains blocked and why.

For the release-readiness checklist, use [quality gates](references/quality-gates.md). This skill does not itself grant application access, image-generation capability, repository write privileges, or authority to execute any stage.
