# Conversation example 01 — From a rough idea to a first decision

> **ILLUSTRATIVE SCRIPT — NOT A RESEARCH REPORT.** The comparator labels below are placeholders, not inspected products or verified claims. In actual work, research real sources first when available, cite them, and disclose inaccessible sources. This example demonstrates **pacing**, not actual market facts.

**User:** "I'm thinking of an app where neighbors can borrow tools from each other."

**Assistant (turn 1):** "The core problem seems to be lending items safely without a lot of messaging. I'll compare a tool-library reservation flow and a peer-to-peer marketplace flow before sketching. Do users borrow from neighbors they already know, or from anyone nearby?"

**User:** "Mostly people in our apartment building."

**Assistant (turn 2 — *sample research format, not real findings*):**

| Comparator to investigate | Workflow question | Evidence required in real use |
| --- | --- | --- |
| Tool-library booking apps | How is item availability reserved? | Current product link and dated documentation or tested UI |
| Community exchange apps | How are handoffs and late returns handled? | Current product link and dated documentation or tested UI |

"I'd adapt simple availability and avoid public marketplace complexity unless you want it. I haven't verified specific services for this example. Does that direction sound right?"

**User:** "Yes, simple is good."

**Assistant (turn 3):** "Exploratory depiction — **text wireframe only**, not a rendered image or functional UI:

```text
TOOLS IN OUR BUILDING
[Search tools...]
[Available] [Borrowed]
[Drill]   [Request]
[Ladder]  [Request]
[My loans]
```

Is this in the ballpark, or should availability take center stage?"

**User:** "Close. I want members to see when a tool must be returned."

**Assistant (turn 4):** "I'd display a due date on each active loan and in My loans. Before deciding what 'overdue' does, does a reminder simply notify the borrower, or should it block another request?"

**User:** "Just a reminder at first."

**Assistant (turn 5 — brief decision recap, still zero-file):**

- **Confirmed:** Building-only scope; show due dates on current loans; reminders only, no blocking.
- **Proposed:** Availability filters and a simple request button.
- **Open:** Who approves a request and how pickup is confirmed.
- **Rejected:** Public marketplace complexity for the first version.

"I won't create documentation yet. The next useful decision is who accepts a borrowing request. Once we agree on the core journey, I can make a `DESIGN.md` and the first testable stage card if you want an agent to build it."

## Why this example matters

- Research is **prior to depiction**; the example explicitly has no actual sources, so it does not claim to have performed real research.
- Questions and visuals **alternate across turns** rather than appearing as an intake questionnaire.
- An early visual establishes direction, **not approval** of permissions, exceptions or coding.
- The decision recap is in chat; files are created only when the user needs persistence or a staged handoff.
