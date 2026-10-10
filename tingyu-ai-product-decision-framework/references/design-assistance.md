# Mode 2: Design Assistance

Use to help design a new feature, a reliable AI/agent workflow, a review UX, or a business system. Give concrete choices that the team can implement without unnecessary ceremony.

## Design procedure

1. **Define the deliverable job.** Name one primary persona, trigger, observable outcome, critical data inputs, and explicit non-goals. Confirm the inputs can support the promise before designing the answer.
2. **Map the end-to-end path.** Start with `Trigger -> Authoritative source + optional evidence -> Interpret/plan -> Validate -> Review if needed -> Handoff/authorized action -> Verify the receiving state or recover`. Merge steps for simple flows; show any incumbent step that must remain untouched. Distinguish task-level assistance from full workflow orchestration.
3. **Choose the simplest mechanism.** Default to deterministic code and conventional UI for fixed, structured work. Use AI for ambiguity and agents only when dynamic multi-step context justifies them. Use skills/scripts for repeatable instructions or checks, not as replacements for authoritative state.
4. **Assign authority and design states.** Identify draft, provisional, confirmed, and final *only if needed*. Decide what can auto-complete, what deserves a prepared recommendation, what requires a person's choice, and which missing fact actually blocks progress.
5. **Design the user's decision surface.** Show source evidence, impact, and `Accept / Adjust / Undo` near the decision. Group repetitive items, keep progress visible in the same workflow, and preserve decisions across retries or regeneration.
6. **Test two critical failure paths.** Specify acceptance checks and the smallest coherent MVP. Include the full outcome and verification burden, not only successful model output.

## Allocate work and authority

| Owner | Delegate | Require |
| --- | --- | --- |
| Code / rules | Calculations, invariants, permissions, validation, state transitions, official writes | Reproducible inputs, version/state checks, traceability |
| AI model | Extraction, messy interpretation, classification, explanation, drafting | Grounded sources, structured result, uncertainty and abstention |
| Agent | Bounded investigation and action orchestration across tools | Declared capabilities, budgets, milestones, checkpoints, recoverable failures |
| Person | Missing business context, goals, consequential tradeoffs, approvals, accountability | Clear alternatives, evidence and impact, low-friction correction |

**Do not equate high model confidence with authority.** A source-backed, low-risk mechanical action may be automatic; a material business choice can still require a person despite high confidence.

## Preserve ownership when adding AI to an existing workflow

Define a compact **input and output authority contract** before designing the agent's interface:

- **Finalized upstream result:** Who finalized the value or state used by this workflow? Successful file import proves formatting, not accounting or professional correctness. Finalized balances and raw transactions have different purposes; optional transaction details must not override finalized figures.
- **Reporting classification:** Mapping a record into a reporting taxonomy is not evidence that the upstream accounting or the downstream legal treatment is correct. Record its version, source, reviewer, and unresolved differences.
- **Domain-specific treatment:** Keep sourced facts, AI proposals, explicit business choices, professional approval, and deterministic calculation distinct. A citation points to evidence; it does not independently prove that the cited passage supports the conclusion. If documents are missing, ask for the smallest needed evidence instead of assuming the agent examined it.
- **Correction loop:** If an authoritative source appears incorrect, return a correction request to its owner and use a newly finalized version. Do not hide a book/master-data error inside a downstream domain adjustment.
- **Receiving-system contract:** Define the *smallest useful delta*. For each field: tested destination/version, original value and source, known existing value or explicit UNKNOWN, action NEW / REPLACE / VERIFY_ONLY / NO_WRITE, approval and retry/reversal behavior.

Keep the relevant readiness states separate: **imported -> source-finalized -> mapping-reconciled -> treatment-reviewed -> downstream-verified**. An export should not be called posted, filed, or complete until the receiving tool's state confirms it. Test the actual import template, field IDs, existing-field protection, re-import, and recalculation—not just file generation.

The user interface should surface **exceptions and decisions**, not ask the professional to maintain the entire record in two places. When existing software already owns a number, link to it, validate it, or propose a targeted correction.

## Three practical design details

**1. Capture human context as product data, not only chat.** When a judgment or assumption changes future results, record its meaning, subject/scope, author, date, source, validity period, approval status, and history. Distinguish `observed fact`, `assumption`, `AI recommendation`, and `human choice`. Never silently turn a conjecture into a fact or reuse an expired assumption.

**2. Design checkpoints at action boundaries.** For each meaningful side effect define the authenticated actor, semantic tool, valid input, source evidence, state precondition, idempotency, audit record, result verification, and cancel/reversal or compensation. Prefer existing domain APIs plus narrower agent allowlists. Avoid stacking opaque AI self-checkers as a substitute for explicit validation and evidence.

**3. Optimize for the user's role, not a universal chat screen.** A manager may need `What changed? Why does it matter? What now?`; an operator may need `What is blocked? What needs review? What can I fix?`. Same underlying records, different information priority. Use conventional UI when direct editing is faster than chatting.

## Progressive AI automation

- **First, reliable steps:** make local AI capabilities testable, bounded, and individually recoverable. Encode stable procedures as shared scripts, workflows, or skills where that reduces repeated prompting and handoffs.
- **Then, one complete workflow:** connect those steps through agent orchestration only when the data handoffs, failure handling, and decision gates are workable.
- **Prove the closed loop:** `Accepted source -> Evidence -> Issue -> Recommendation -> Review when needed -> Handoff/action -> Observed downstream outcome`. A dashboard insight, plausible workpaper, or generated import template is not a completed business outcome.
- **Measure net improvement:** baseline manual time minus machine-assisted preparation, new verification, exception resolution, and rework. If total checking dominates, narrow automation or keep the human-first flow.

## Review choices by consequence

- **Auto-complete:** mechanical, sufficiently evidenced, reversible, and within explicit policy; make it visible in history.
- **Prepared recommendation:** show the proposed result and its consequence; person accepts or adjusts a meaningful judgment.
- **Explicit selection/approval:** goals, elections, irreversible or material external effects, or domain-mandated sign-off.
- **Ask for context:** one decisive question when evidence cannot establish a necessary real-world fact; continue unrelated work.

Do not require the same approval or evaluation level for every step. Avoid universal claims that retrofitting agents into legacy systems is impossible; assess whether a narrow API/action surface can be made safe and economical first.

## Illustrative flow

**Task:** Help an operator resolve an ambiguous account item.

`Detect an anomaly -> Gather allowed records -> Code checks consistency -> Agent proposes one action with source references -> Uncertain item enters one review card -> Operator accepts or edits -> Authorized API applies change -> System checks persisted result and provides an undo path.`

Adapt controls to the domain. Prefer a short flow, a few actionable states, and two tested failures over a comprehensive but unshippable platform diagram.

## Deliverable

Return a main user flow, the ownership/review boundary, 1-3 concrete interaction choices, the critical edge cases, and MVP acceptance checks. Avoid huge backlogs unless asked.
