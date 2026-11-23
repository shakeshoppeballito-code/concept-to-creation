# Stage <NN> — <specific demonstrable outcome>

> **NOT IMPLEMENTATION AUTHORITY.** This card is a proposed plan; only explicit approval for this stage permits execution. No approval here permits the next stage or deployment.

Status: PROPOSED  
Project: <links to available PROJECT/DESIGN/ARCHITECTURE/BUILD_PLAN or existing sources>  
Linked requirements: <REQ-...>  
Dependencies: <accepted prerequisites or N/A>

## Objective and boundary
<One independently demonstrable result; stage is NOT authorized by generating this card>

## Changed surfaces
<Exact screens, files/components/interfaces likely affected; mark exact paths UNKNOWN until inspected>

## Scope and protections
**Do:** <bounded work>  
**Do not:** <excluded work>  
**Preserve:** <accepted behavior, data, privacy, security and evidence>

## Required inputs and preconditions
<Approved behavior, source versions, access/tools/fixtures; stop if absent>

## Expected behavior and state changes
<Actor, starting state, action, resulting state, alternative/cancel/retry and recovery>

## Compatibility, migration and rollback
<Potential compatibility or data impact, migration plan, reversible path, or explicit N/A with reason>

## Acceptance tests
Every acceptance criterion must trace to a `confirmed` decision/requirement. If stage-defining behavior is `proposed` or `open`, mark the stage **BLOCKED FOR DESIGN**; do not hand off implementation.

| ID | Requirement | Test / observation | Exact pass condition | Evidence to return |
| --- | --- | --- | --- | --- |
| A-01 | REQ-001 | <scenario> | <observable expected result> | <log/screenshot/test output> |

## Unknowns and stop conditions
<Blocking decisions; do not ask the agent to invent product behavior>

## Agent report required
- Exact changed source surfaces and references, deviations from scope
- Tests executed with results/evidence and all **NOT RUN** tests with reasons
- Artifacts and provenance; a screenshot cannot establish unshown runtime behavior
- Defects, blocked items, risks and changed assumptions
- Proposed result **READY FOR REVIEW / NEEDS CORRECTION / BLOCKED**; never auto-accepted

## Approval and review gate
<Who authorizes this stage's execution? Who reviews and accepts evidence? Acceptance of this stage does NOT authorize the next stage, merge, installation or deployment.>

## If implementation exposes a design flaw
<Identify affected decision and requirement IDs, preserve stage/history, pause affected implementation, reopen discovery and request user decision before revised instructions>
