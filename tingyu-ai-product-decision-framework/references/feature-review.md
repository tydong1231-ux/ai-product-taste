# Mode 1: Feature Review

Use for a requirement, PRD, workflow, prototype, shipped feature, UI, system design, or supplied implementation. Evaluate what works and what should change, not whether it matches a preferred AI pattern.

## Review procedure

1. **Reconstruct the job.** Identify the user, trigger, current workaround, desired final state, and consequences of an incorrect result. Ask whether the promise is within the product's actual data and context.
2. **Trace the real flow.** Compare claimed behavior with code, screens, states, and tests actually provided. Identify who acts, what data they see, when a record becomes final, and how they recover.
3. **Check end-to-end value.** Is this a useful isolated improvement or does a handoff/review bottleneck erase the benefit? For automation-heavy workflows, sample the material steps: baseline effort, needed context, whether AI can help, verification effort, and remaining human/physical constraint.
4. **Stress the relevant boundaries.** Choose only the lenses below. A harmless UI tweak does not need the controls of a financial transaction.
5. **Rank 3-5 actionable findings.** State the observed failure or design risk, why it matters, the smallest viable fix, and how to verify it.

## Review lenses

| Lens | Ask |
| --- | --- |
| User outcome | Does it finish the important job, or merely expose features and impressive answers? |
| Data ceiling | Are required inputs reliable, current, correctly scoped, and complete? Are unsupported insights withheld? |
| Authority | Which actions are deterministic, inferred, provisional, approved, or posted? Can a model silently bypass a rule? |
| End-to-end workflow | Is effort saved at this step lost to downstream handoffs, reviews, or missing integrations? |
| Human experience | Does each role see what matters, why, and the next action? Does the reviewer repeat the work? |
| Risk and recovery | What happens on wrong match, duplicate, stale source, permission denial, timeout, retry, partial success, or reversal? |
| Economics | Does total work avoided exceed new checking and support? Is the denominator for success clear? |

## Evidence and severity

- **P0:** A concrete path to unauthorized or irreversible action, false authoritative data, material harm, or a broken core outcome. Describe the mechanism; do not call a hypothetical risk a proven bug.
- **P1:** Material user confusion, avoidable rework, poor recovery, unsupported promise, or automation whose verification cost undermines value.
- **P2:** Worthwhile simplification, navigation, terminology, or secondary polish.
- Label significant claims **Observed**, **Reported**, **Design risk**, or **Needs verification**. Do not invent test results.

## Extra checks for implemented features

- Inspect the visible code path, state transition, validation, permission check, and failure path when available. A PRD is intent, not proof.
- Walk one normal and two high-consequence edge paths; check persisted state, not only a success toast or chat response.
- Check whether source imports, regeneration, or re-runs preserve prior human decisions and correct invalidated ones.
- For agent changes, validate actual tool authority, bounded output, error propagation, and user-facing action evidence.
- Prefer targeted fixes and acceptance tests to a full rewrite.

## Concise example

**Verdict:** Keep the matching flow; block confirmation when supporting evidence is absent.

**P0 - A plausible match can become final.** Same amount is not proof of identity. Require reference/counterparty evidence or leave unmatched; test that no authoritative record changes.

**P1 - Human review recreates the work.** Show the relevant source comparison and `Accept / Change / No match` in one review surface.

**Verify:** Track falsely accepted matches, justified abstentions, and actual reviewer minutes, not match coverage alone.
