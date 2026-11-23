# Concept to Creation

**v0.5.0 · Public test candidate**

An Agent Skills-format workflow for researching an app idea, exploring its design, and preparing one testable coding-agent stage at a time.

## Try it and share feedback

1. In a separate test workspace, put the skill folder at `.agents/skills/concept-to-creation/` for Codex. Copy this repository's files into that folder so `SKILL.md` sits directly inside it. For another compatible agent, use its documented local skill location.
2. Open a fresh session in that workspace. Run one of the [12 priority smoke tests](tests/scenarios.md#suggested-first-smoke-pass-12-cases) with a fictional project. For activation tests, paste the prompt without naming the skill.
3. [Open a GitHub issue](https://github.com/shakeshoppeballito-code/concept-to-creation/issues/new) with the test ID or prompt, agent and version, expected and actual behavior, and how you observed the skill load if your host exposes that information. Remove personal and project details from excerpts.

## What has been tested

The initial v0.5 candidate passed 10 of 12 priority cases in one Windows Codex CLI environment. This candidate includes two follow-up fixes. It asks for current screen context before offering product-specific advice and puts sourced comparisons before the initial depiction. Both targeted reruns met their assertions. The other 43 scenarios and testing on additional hosts are still pending.

A full fictional project walkthrough reached a staged handoff. The first draft required a follow-up to restore the stage authority banner and limit acceptance tests to confirmed decisions. Reports on those safeguards and on skill activation are especially welcome.

## What it contains

| Path | Role |
| --- | --- |
| `SKILL.md` | Discovery/activation guidance, progressive conversation, research, depiction, documents, staged handoff and report review |
| `references/research-playbook.md` | Dated, evidence-qualified comparable-product reconnaissance |
| `references/conversation-playbook.md` | Gradual questioning, critique, decision resumption and mid-stage pivots |
| `references/project-documents.md` | **Zero-file / single-doc / multi-doc** selection and single ledger rules |
| `references/quality-gates.md` | Proportionate design, handoff and evidence checks |
| `assets/PROJECT.md` | Durable project brief and canonical decision ledger |
| `assets/DESIGN.md` | User journeys, interactions, requirements; single-ledger fallback for small changes |
| `assets/ARCHITECTURE.md` | Optional technical boundaries |
| `assets/BUILD_PLAN.md` | Optional multi-stage roadmap |
| `assets/STAGE.md` | **Authoritative** coding-agent stage-card template |
| `examples/conversation-01.md` | Illustrative multi-turn loop; **not** a verified research example |
| `examples/STAGE-01.example.md` | Generic filled-in stage example, not execution authority |
| `tests/scenarios.md` | Positive and negative activation checks and behavioral scenarios |

## Changes in v0.5 — independent review convergence

- Tightened description and routed cosmetic/copy-only requests as **mis-activations**, not discovery cases.
- Kept the four separate approval boundaries, reversible assumptions, placeholder data, research-first threshold, and multi-turn pacing.
- Removed duplicate requirement `Status` from `DESIGN.md`; a requirement's status is inherited from its linked canonical decision.
- Blocked an implementation stage whenever a stage-defining requirement remains `proposed` or `open`; assumptions cannot approve acceptance tests.
- Fixed the broken behavioral-test table, added ambiguous near-miss activation tests and a **12-case smoke suite**.
- Added a hypothetical, explicitly **not-researched** conversation example and clarified actual visual fidelity disclosures.
- Strengthened the stage-card authority banner and the small-design document's stage authorization section.

## Package status

This is a development candidate for feedback. It follows the [Agent Skills format](https://agentskills.io/specification). A licence is pending.
