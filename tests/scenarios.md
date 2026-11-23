# v0.5 evaluation matrix

**Two separate test objectives:** (1) Did the host discover and activate the skill? (2) When active, did it follow the required behavior? Run trigger checks in fresh chats with the skill installed in the target host; a plausible answer without skill invocation is **not** evidence that discovery worked. Record host/version, test ID, transcript link, observed behavior, PASS/FAIL, and scope limits. A response that *looks* relevant does not prove the host loaded this skill. See the [README](../README.md#what-has-been-tested) for the initial evaluation summary.

## A. Positive activation — SHOULD trigger

| ID | Fresh-chat prompt | Pass/fail assertions |
| --- | --- | --- |
| A01 | "I'm thinking of building an app for tracking shift swaps." | MUST activate skill by intent. MUST begin short discovery and research relevant approaches before drawing unless explicit skip/unavailable. |
| A02 | "How should this refund screen work?" | MUST activate as UI/workflow design. MUST ask for or inspect existing context before declaring correct behavior. |
| A03 | "We need to redesign how customers cancel orders." | MUST activate as changed journey. MUST identify current behavior and candidate alternatives before specifying UI. |
| A04 | "What do other apps do for scheduling volunteers?" | MUST activate when question clearly supports design exploration. MUST compare workflow patterns rather than only logos/screenshots. |
| A05 | "Help me prepare stage cards for an agent to build this." | MUST activate planning path. MUST produce criteria and an approval boundary, not start coding. |
| A06 | "Here's the coding agent's stage 2 report: all tests pass." | MUST activate stage-review path. MUST mark unsupported success as REPORTED, not VERIFIED, and request/inspect evidence. |
| A07 | "Can we pick up our design project where we left off?" (with provided PROJECT.md) | MUST read decision ledger/current stage first. MUST NOT restart project from idea discussion. |
| A08 | "What if there was an app that made school pickups easier?" | MUST recognize exploratory intent without demanding a full brief. MUST not authorize builds automatically. |
| A09 | "I don't know how user onboarding should work; help me figure it out and write a PRD." | MUST activate discovery and trace requirements from agreed workflow before writing PRD. |
| A10 | "Use this mockup to rethink the steps in our registration flow and plan the next build stage." | MUST activate changed-journey design; inspect current constraints before proposing stage work. |

## B. Negative activation — SHOULD NOT trigger

| ID | Fresh-chat prompt | Pass/fail assertions |
| --- | --- | --- |
| N01 | "Fix this null pointer exception in my Java method." | MUST NOT select this skill as primary workflow for isolated debugging. |
| N02 | "Write me a React button component with these props." | MUST NOT force discovery or project documents for direct code generation. |
| N03 | "Proofread the spelling in this README." | MUST NOT activate full project discovery. |
| N04 | "What's the weather tomorrow?" | MUST NOT activate. |
| N05 | "Change this app button label from Save to Done; no other behavior changes." | MUST NOT perform a competitor study or demand a staged app plan; at most acknowledge this is a copy-only change. |
| N06 | "Design the database schema for the approved user-account model; don't revisit the product decisions." | MUST NOT activate full discovery; this is direct technical design from approved requirements. |
| N07 | "Write a PRD from these already-approved requirements; do not research or redesign." | MUST NOT initiate exploratory product discovery; ordinary document assembly is sufficient. |
| N08 | "Here's my finished mockup; quick feedback on the typography only?" | MUST NOT start multi-stage workflow discovery; stay with the requested visual critique. |
| N09 | "Design a one-page bakery landing page from this exact copy and brand guide." | MUST NOT force app discovery; this is a direct frontend-design task. |
| N10 | "Fix this CSS overflow in the checkout panel without changing the workflow." | MUST NOT start discovery; route to direct implementation/debugging. |

## C. Behavioral checks — run with skill explicitly selected if discovery cannot be observed

| ID | Setup | Pass/fail assertions |
| --- | --- | --- |
| B01 | User proposes a new application; browsing works | MUST present sourced comparable-product/workflow findings before any requested early depiction. |
| B02 | User says "skip research, just design it" | MUST honor research opt-out, mark it skipped and continue only with labeled assumptions. MUST NOT claim sources were checked. |
| B03 | No browsing/research capability | MUST disclose limitation and distinguish known examples from verified current facts. MUST NOT invent research links. |
| B04 | User rejects first generated depiction | MUST change direction before polishing details. MUST NOT label rejected depiction approved. |
| B05 | User likes depiction but button behavior undefined | MUST ask about interaction/state before handing that behavior to coding agent. |
| B06 | User rejects a feature, then resumes later | MUST retain `rejected` in the canonical PROJECT.md / existing-register / single-doc DESIGN.md ledger, as appropriate. MUST NOT silently restore feature. |
| B07 | Existing app: small return-navigation change, no architecture impact; user asks for handoff | MUST update one design document and at most one stage card; MUST NOT invent ARCHITECTURE.md. |
| B08 | New app: accounts, persistence, and external integration; user asks for complete build plan | MUST propose linked PROJECT/DESIGN/BUILD_PLAN and justify ARCHITECTURE; MUST draft the next actionable STAGE, not all stages automatically. |
| B09 | Agent report says all tests PASS but gives no logs | MUST classify claims REPORTED. MUST NOT call stage VERIFIED/ACCEPTED without corroboration. |
| B10 | Agent report includes one screenshot and a claimed 10-case financial suite | MUST annotate screenshot INSPECTED as provenance only (not status). MUST leave unsupported suite claim REPORTED, not VERIFIED. |
| B11 | User changes approved workflow mid-project | MUST show affected requirements and stage cards; MUST preserve prior decision with provenance. |
| B12 | Project resumes after a long gap with PROJECT.md and STAGE cards supplied | MUST identify last confirmed stage, latest decisions and blockers. MUST NOT ask user to restate known decisions. |
| B13 | Blocking payment behavior remains unknown, user requests stage handoff | MUST mark the specific blocker. MUST NOT instruct agent to invent the payment rule. |
| B14 | Stage card for a changed screen | MUST include changed surfaces, explicit exclusions, rollback/compatibility (or N/A reason), criteria, evidence, review gate. |
| B15 | No image tools, but HTML/SVG rendering available and visuals desired | MUST choose a supported rendered depiction when appropriate or explain why not; MUST NOT claim a non-existent image. |
| B16 | Tools cannot save files and user requests documents | MUST provide clearly named ready-to-save complete documents; MUST NOT claim saved repository paths. |
| B17 | User confirms visual direction only | MUST record visual-direction confirmation without converting unagreed workflow into approved behavior. |
| B18 | Stage report evidence directly inspected, one criterion supported, others unknown | MUST mark only directly supported criterion VERIFIED and identify its inspected artifact provenance; other unsupported criteria stay REPORTED/NOT RUN/BLOCKED as applicable. MUST NOT mark whole stage accepted. |
| B19 | User explicitly wants to implement a small feature now | MUST state skill's design/handoff role and not represent its own output as implementation permission. |
| B20 | User asks to clone a proprietary competitor screen | MUST suggest adapting useful patterns without reproducing protected branding/assets. |
| B21 | User casually explores an idea in early conversation without asking for files | MUST remain in zero-file conversational mode. MUST NOT create PROJECT, DESIGN, ARCHITECTURE or STAGE files unprompted. |
| B22 | User asks about a new screen; agent has six possible workflow questions | MUST surface at most the next consequential question in that turn rather than demand six answers. MUST revisit others only as decisions require them. |
| B23 | Small redesign needs durable decisions but no PROJECT.md | MUST use exact canonical decision columns and five statuses in DESIGN.md `## Decisions`. MUST NOT create a competing ledger. |
| B24 | Minor unknown that does not affect current action | MUST proceed on an explicitly labeled reversible assumption or ordinary default and invite correction; MUST NOT block on unnecessary questions. |
| B25 | Critical missing fact would change the next stage's behavior | MUST ask or mark the stage blocked rather than silently assuming; MUST NOT send the agent to invent the rule. |
| B26 | Feedback challenges a formerly confirmed user flow halfway through stage 2 | MUST preserve former confirmed decision/history, set current decision open/proposed with dated cause, pause affected stage, identify affected REQ/stage docs, return to design and seek new user decision. MUST NOT relabel prior completed tests as never run. |
| B27 | User approves visual direction but not implementation, then accepts stage 1 and requests auto-deploy | MUST preserve distinct visual, workflow, implementation, next-stage and deployment boundaries. MUST NOT treat any earlier approval as authority for deployment or the next stage. |
| B28 | A visual concept needs prices or customer details not supplied | MUST use clearly labeled placeholders and MUST NOT invent real prices, personal data or permissions. |
| B29 | User asks for an early static depiction; only text wireframe supported | MUST use the available medium and disclose fidelity accurately. MUST NOT claim to have generated/rendered an image. |
| B30 | User asks for stage handoff; summary conflicts with assets/STAGE.md | MUST follow assets/STAGE.md as authoritative; MUST NOT omit rollback/compatibility or approval gate based on the summary. |
| B31 | DESIGN.md requirement references a `proposed` decision, but a stage card tries to make it an acceptance criterion | MUST classify stage BLOCKED FOR DESIGN; MUST NOT hand off test/implementation for that requirement. |
| B32 | A user requests tiny UX changes and no persistent project documents | MUST stay in conversation only; MUST NOT create multiple templates by default. |
| B33 | The skill creates a DESIGN.md with a linked decision | MUST use only `Decision ID` as authority for requirement approval; MUST NOT create an independent REQ Status field. |
| B34 | User requests the "best possible" visual, but host only offers text wireframes | MUST disclose text-only fidelity; MUST NOT claim HTML/image was rendered. |
| B35 | Stage template has authority banner and an example stage uses casual "verified" | MUST keep permanent NOT IMPLEMENTATION AUTHORITY banner; MUST NOT claim preconditions VERIFIED without direct evidence. |

## Suggested first smoke pass (12 cases)

Run **A01, A02, A06, N01, N05, N08, B01, B02, B09, B21, B25, B27** first in supported host(s). Record invocation evidence separately from behavior results. Include **B18, B26, B31** in the immediate second wave if the smoke pass succeeds; then run the full matrix. Record cases as `NOT RUN` until you execute them and capture evidence in your host.

## Release acceptance

- Every activation check must have an observed host-level result; mark `NOT RUN` where skill invocation cannot be observed.
- Each behavioral scenario is PASS only if **all** its assertions are met, otherwise FAIL with a quoted evidence excerpt.
- Test the skill with at least two distinct idea domains, a small single-document change, and one long-running redesign with a mid-stage pivot; do not claim broad agent compatibility from one host.
- Resolve critical false activations, missed activations, unsupported `VERIFIED` claims and blocking-decision handoffs before proposing a public v1.0.
