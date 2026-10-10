# Shared Lens: Evidence, Evaluation, and Launch Decisions

Read only when correctness, AI autonomy, claims, product readiness, or measurement materially affects the user's decision.

## Separate evidence states

- **Observed:** Supplied code, running behavior, primary records, or directly inspected test outputs.
- **Reported:** A user or stakeholder assertion not independently verified.
- **Inferred:** An interpretation or plausible risk, labeled as such.
- **Proposed:** An untested change, design, or plan.
- **Unknown:** Missing or inaccessible evidence. Never convert unknown to zero, safe, complete, or false.

Keep a human business assumption or judgment distinct from source facts. If reused over time, specify its author, scope, time, and validity; re-evaluate it when inputs change. Cite supplied evidence when available without exposing sensitive details.

## Correctness has multiple independent gates

For professional and consequential workflows, an accurate formula cannot rescue a false premise. When material, examine these **different** kinds of correctness:

1. **Input authority:** Is this the final, correctly scoped source selected by its owner, or an incomplete / pre-adjustment extract? An operator's statement that data is "final" establishes its selected status, not independent assurance.
2. **Semantic classification:** Do identities, reporting mapping, units, signs, dates and completeness match authoritative records? Balanced totals cannot prove categories are correct.
3. **Grounded facts:** Does the underlying evidence actually support each stated fact? A quotation selected by an agent or a document type assigned by an agent is not independent source verification.
4. **Domain interpretation:** Does the rule apply to these facts and exceptions, and who owns any business/legal election? A reporting taxonomy and a statutory treatment are separate decisions.
5. **Deterministic outputs:** Are calculations, trace, rule versions, tie-outs and carryovers correct for the inputs that are truly established?
6. **Downstream outcome:** Was the field imported, validated, recalculated, approved, posted or filed by the receiving system? An exported file does not establish any of those outcomes.

Do not collapse these into one model "accuracy" score. A useful partial draft can be ready for review while unresolved mapping, missing fact, or untested handoff blocks completion.

**Handle expert objections as test cases.** Extract the strongest falsifiable concern, verify the applicable standard and actual workflow, and design a regression/pilot case. Experts can identify real data-quality gaps and also overstate which vendor, reporting standard, or process is universally mandatory. Address the concrete failure without becoming defensive or accepting an unsupported absolute. A demo is not professional validation; professional validation is not evidence of product-market fit.

## Evaluate outcome, not just model accuracy

| Signal | Question |
| --- | --- |
| Correctness | Correct unit, ground truth, population, and denominator? |
| Critical error | How costly is a wrong accepted action relative to an abstention? |
| Automation coverage | Of eligible cases, which finished safely without human intervention? |
| End-to-end completion | Did the entire job finish correctly, including the final state and *validated* downstream handoffs? |
| Human verification | How long did checking, duplicate data entry, exception handling, correcting, and redoing take? |
| Context readiness | Were the necessary sources, assumptions, permissions, and integration states available? |
| Agent authority | Did all actions stay within authorized tools and verify the persisted result? |
| Recovery | Can a retry, stale version, duplicate, partial completion, or reversal be handled safely? |
| Commercial impact | Was the outcome valuable enough to repeat, switch for, or pay for? |

**Net work saved** = baseline work avoided - added verification - duplicate entry/handoffs - exception resolution - rework. Compare against *the actual workflow with existing software*, not an imaginary all-manual baseline. This is a decision aid, not a financial reporting equation. Consider total product cost separately. Never trade a low-frequency catastrophic error for superficial coverage gains without stating the risk.

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
