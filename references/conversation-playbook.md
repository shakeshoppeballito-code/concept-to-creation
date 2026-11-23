# Conversational discovery playbook

This is a *menu of prompts*, not a questionnaire or a required per-turn script. Use the pacing and research threshold in `SKILL.md`.

## Start small and progress across turns

- First response: reflect the user's objective, add one useful insight, and ask **at most the next consequential question** (or offer a researched comparison if that will help more).
- Follow-up turns: test one significant assumption or show one relevant visual. Don't ask the user to answer an exhaustive list of states, permissions and errors.
- If a fact doesn't affect the next move, proceed on a **labeled, reversible assumption** and invite correction. If it affects safety, permissions, money, or irreversible behavior in the *next stage*, clarify before handoff.
- Don't create project documents in a casual exploration unless the user wants a durable record or development handoff. A short chat recap is sufficient at first.

## Opening a new idea

- Identify the intended user and key task in plain language.
- For a **new app, new screen, or changed user journey/interaction**, follow `SKILL.md`'s research-first default unless an explicit skip condition applies.
- Share specific strengths/weaknesses of comparable solutions and invite reaction; consider adjacent industries when the same underlying workflow exists.
- Then create one representative exploratory concept with the best available medium when a depiction helps. Ask "Which parts are close, and what feels wrong?"

## After a positive reaction to a depiction

Explore the next relevant behavior instead of simply polishing appearance. Example prompts to use selectively:

- "When someone taps this, what happens next?"
- "What is shown when there is nothing to display?"
- "Who is allowed to do this?"
- "What if someone changes their mind partway through?"
- "What if this action fails or happens twice?"
- "Which steps could be removed without creating risk?"

Check the key actor, starting state, state transition and outcome as the design matures. Do not ask every example prompt in one turn.

## Challenge constructively

- Offer one or two specific alternatives with practical trade-offs.
- Check the user's actual workflow, not what a polished picture seems to promise.
- Before presenting a revised visual, ensure it shows the requested experience and doesn't resurrect rejected choices or invent data.

## Single decision history and resumption

- Begin at the **first meaningful decision**: keep `confirmed / proposed / open / rejected / deferred` notes in conversation until the user requests persistent documentation.
- Once documents exist, use the **single canonical** decision table in `PROJECT.md` (or existing register). For a one-document change, use `DESIGN.md`'s `## Decisions` table if there is no `PROJECT.md`.
- Use the exact column names and status vocabulary in `assets/PROJECT.md`. Summaries are *views*, not a second register. Retain rejected options and change history with provenance.
- For a returning conversation, inspect the current decisions and stage first; do not ask the user to restate known outcomes.

## Pivot when implementation contradicts design

- Record the report or test evidence and the affected `D-###` and `REQ-###` identifiers.
- Pause only affected stage activity. Preserve previous accepted evidence and the original confirmed decision as history.
- Mark the current decision `open` or `proposed` with the date and reason; return to targeted discovery/research or workflow design.
- Revise downstream requirements and proposed stages after a user decision; do not quietly alter an accepted stage or imply new implementation authorization.

## When to stop discovery

Prepare a stage handoff when the **next stage's** behavior, boundaries, prerequisites, and tests are defined. Leave clearly identified nonblocking choices for later stages. Don't continue asking questions just to eliminate every possible unknown.
