# Stage 01 — Filter an existing reading list by category

> **NOT IMPLEMENTATION AUTHORITY.** Example stage only; no execution rights.

Status: EXAMPLE ONLY  
Project: sample existing app with an accepted reading-list screen  
Linked requirements: REQ-004 (category filter)  
Dependencies: existing list and category labels reported present; inspect before implementation

## Objective and boundary
Let readers filter their saved books by an existing category, without losing the selected category when viewing and returning from a book detail screen.

## Changed surfaces
Reading-list screen and list/detail navigation state. Exact source files must be identified by the implementer from the real project.

## Scope and protections
**Do:** Add filter control and preserve its state during ordinary list→detail→back navigation.  
**Do not:** Redesign book details, add categories, change storage schema or user accounts.  
**Preserve:** Book ordering within filtered results, saved-book data and existing navigation permissions.

## Required inputs and preconditions
An illustrative *confirmed* `REQ-004` and linked decision would be required in a real project; source and screenshots must be inspected. Stop if category data or confirmation is absent.

## Expected behavior and state changes
Default is All. Selecting a category filters visible books. Opening a book and returning restores the previous category; resetting to All restores the complete list.

## Compatibility, migration and rollback
No persistent data/schema change expected. Revert the isolated UI/navigation change if acceptance criteria fail.

## Acceptance tests
| ID | Requirement | Test/observation | Exact pass condition | Evidence to return |
| --- | --- | --- | --- | --- |
| A-01 | REQ-004 | Choose a category | Only matching books appear; original order within category preserved | Screenshot + test output |
| A-02 | REQ-004 | Open a book, then return | The same category remains selected | Navigation test output |
| A-03 | REQ-004 | Switch to All | All previously visible books return, with unchanged data | Test output |

## Unknowns and stop conditions
Stop for user decision if categories are not already defined or filter behavior contradicts an accepted requirement.

## Agent report required
Exact changed files, tests and outputs, tests NOT RUN, evidence references, deviations, defects and READY FOR REVIEW / NEEDS CORRECTION / BLOCKED recommendation.

## Approval and review gate
This example does not authorize any coding. In a real project, a human approves execution and separately assesses the results.

## If implementation exposes a design flaw
If the implementation evidence contradicts REQ-004 (for example, categories are not persistent), record the affected decision/requirement and evidence, pause the affected work, preserve the previous stage report, return to design and request a user decision before issuing revised stage instructions. A revised plan is not retroactive permission for code changes.
