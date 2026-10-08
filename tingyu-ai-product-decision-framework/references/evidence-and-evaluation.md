# Shared Lens: Evidence, Evaluation, and Launch Decisions

Read only when correctness, AI autonomy, claims, product readiness, or measurement materially affects the user's decision.

## Separate evidence states

- **Observed:** Supplied code, running behavior, primary records, or directly inspected test outputs.
- **Reported:** A user or stakeholder assertion not independently verified.
- **Inferred:** An interpretation or plausible risk, labeled as such.
- **Proposed:** An untested change, design, or plan.
- **Unknown:** Missing or inaccessible evidence. Never convert unknown to zero, safe, complete, or false.

Keep a human business assumption or judgment distinct from source facts. If reused over time, specify its author, scope, time, and validity; re-evaluate it when inputs change. Cite supplied evidence when available without exposing sensitive details.

## Evaluate outcome, not just model accuracy

| Signal | Question |
| --- | --- |
| Correctness | Correct unit, ground truth, population, and denominator? |
| Critical error | How costly is a wrong accepted action relative to an abstention? |
| Automation coverage | Of eligible cases, which finished safely without human intervention? |
| End-to-end completion | Did the entire job finish correctly, including the final state and downstream handoffs? |
| Human verification | How long did checking, exception handling, correcting, and redoing take? |
| Context readiness | Were the necessary sources, assumptions, permissions, and integration states available? |
| Agent authority | Did all actions stay within authorized tools and verify the persisted result? |
| Recovery | Can a retry, stale version, duplicate, partial completion, or reversal be handled safely? |
| Commercial impact | Was the outcome valuable enough to repeat, switch for, or pay for? |

**Net work saved** = baseline work avoided - added verification - exception resolution - rework. This is a decision aid, not a financial reporting equation. Consider total product cost separately. Never trade a low-frequency catastrophic error for superficial coverage gains without stating the risk.

## Place assurance at the right boundaries

Test normal, incomplete, ambiguous, stale, conflicting, duplicate, unsupported, and high-consequence cases. Use deterministic invariant checks and source-based verification whenever possible; reserve human review for unresolved decisions. Do not assume one high-level model evaluator guarantees the correctness of every downstream action. Negative answers such as `unknown`, `no match`, or `needs review` can be correct outcomes.

## Call experiments by their real names

- **Offline regression:** Compare versions on the same saved cases.
- **Shadow evaluation:** Observe new logic on live-shaped data without user-visible effects.
- **Pilot:** Limited real use, not necessarily randomized.
- **Canary:** Limited release with monitoring and rollback.
- **Randomized A/B test:** Allocate actual users or traffic to variants for causal comparison.

A prompt replay is not an A/B test. Do not present a claimed accuracy rate without its evaluation unit, denominator, distribution, and human involvement.

## Launch gate

Specify only the risk-proportionate checks: authoritative rules intact, no known unauthorized action paths, missing evidence surfaced, material choices reviewed, recorded result verifiable, recovery workable, and total user effort meaningfully improved. A low-stakes creative feature needs fewer controls than a financial posting operation.
