# Mode 2: Design Assistance

Use to design AI-native features, non-chat products, agent workflows, review UX, and reliable execution. Give the smallest implementable design that completes a user job.

## Design in six steps

1. **Define the outcome.** Identify the user, trigger, existing workflow, trustworthy input, intended receiving state, and non-goals. Check that the evidence can support the promise.
2. **Map authority, then capabilities.** Identify who owns each source fact, rule, business decision, persisted record, and downstream action. Do not turn a proposed interpretation into an authoritative fact.
3. **Choose the least complex mechanism.** Prefer code and conventional UI for fixed work, AI for ambiguous interpretation, agents for justified multi-step execution, and the incumbent system for records it already owns. Use a new governed runtime only for responsibilities that actually need one.
4. **Set action-specific autonomy.** Distinguish observe, propose, stage, and commit. Define the evidence, authorization, verification, consequences, and recovery required for each meaningful state change.
5. **Design the decision surface.** Show progress and exceptions in the user's business workflow. Put source, rationale, effect, and `Accept / Correct / Undo` by consequential decisions; do not make the user redo machine-verifiable work.
6. **Prove the closed loop.** Test the normal case, one missing/conflicting-evidence case, and one failed/retried action. Measure the real downstream result and the remaining human effort.

## Who owns what?

| Role | Primary responsibility | Boundary |
| --- | --- | --- |
| **Source / external authority** | Original evidence, governing rules, upstream records, downstream calculations or commitments | Do not overwrite, infer, or duplicate its authority without an explicit contract |
| **Platform + deterministic code** | Typed state, validations, permissions, versioning, audit, authorized writes, downstream verification, recovery | Verifies what can be checked; does not transform unsupported assumptions into facts |
| **AI model** | Extract, interpret, classify, explain, draft | Ground uncertain outputs; preserve unknowns and abstain when evidence is insufficient |
| **Agent** | Plan and execute bounded multi-step work through semantic tools | May only exercise explicitly delegated capabilities; must not self-grant approval |
| **Person** | Set goals and delegation policy, provide missing context, resolve material choices, own required sign-off | Intervene where judgment or accountability matters, not at every mechanical step |

These are **responsibilities, not mandatory product components**. One system may serve multiple roles. A low-stakes one-off task may need only a script or a general agent; a consequential recurring workflow may need durable governance.

## Authority before autonomy: the action test

For every action that changes state, decide:

1. **Permission:** Who authorized this actor, tool, object, scope, and level of effect?
2. **Evidence:** Are the required facts established, or is an inference being mistaken for a fact?
3. **Verification:** Can the result be checked against independent evidence, deterministic rules, or the receiving system? A second model's agreement alone is not proof.
4. **Consequence:** What happens if this action is wrong? Does law, policy, or material judgment require approval?
5. **Recovery:** Can it be undone or compensated? Are retries idempotent, versions checked, and partial success detectable?

| Appropriate delegation | Product behavior |
| --- | --- |
| **Observe / propose** | Read allowed data; present grounded drafts without changing authoritative state |
| **Prepare / stage** | Validate and save reviewable, reversible work; route unresolved judgments to people |
| **Policy-bounded commit** | Automatically execute only with explicit permission, adequate evidence/checks, acceptable risk, and verifiable recovery |
| **Consequential commit** | Require the necessary human decision or formal authorization before external effects; verify the outcome afterward |

A model's confidence score does not increase its permission. Nor does safety require blanket approval for each low-risk, objectively verifiable action. Delegation can expand with evidence and evaluation, or contract when the context becomes riskier.

## Design state and UX around the job

- Keep `observed / assumed / proposed / reviewed / committed / verified` distinct **where material**. A partial output is not a completed outcome; missing is `UNKNOWN`, not consent or zero.
- Preserve human choices, provenance, version, and scope across reruns. Invalidate only affected approvals when inputs change.
- Center the UI on business objects, status, exceptions, and next decisions. Use chat for exploration, not as a compulsory interface to structured records or simple edits.
- Make correction contextual: `Result -> evidence / assumption -> affected action -> fix at owner -> recompute -> appropriate approval -> verify downstream`. If lineage is unavailable, say so; do not invent it.
- For side effects use authenticated semantic tools, narrow allowlists, preconditions, idempotency, audit, and read-back. On failure, expose the partial state and a safe next step; never show success merely because a tool call returned.
- Avoid duplicate entry beside mature software. When the source or target is wrong, send a correction to its owner rather than concealing the problem in a parallel workspace. See [incumbent workflow boundaries](incumbent-workflow-boundaries.md) for detailed integration contracts.

## Illustrative pattern

For an ambiguous transaction match:

`Evidence collected -> deterministic candidate checks -> agent proposes match or abstains -> policy permits a proven unique low-risk match OR routes an ambiguous match to review -> authorized write -> persisted result verified -> correction/retry available.`

Do not automate solely because similarity or model confidence is high. Equally, do not force an operator to inspect every unique, policy-compliant match if sound checks and authorization make automatic completion appropriate.

## Deliverable

Give **one main flow**, the minimal authority/delegation map, 1-3 specific interaction choices, critical failure paths, and MVP acceptance checks. Optimize **verified outcome value minus human verification and recovery cost**, with hard safety requirements independent of that calculation.
