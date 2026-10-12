# AI Agents vs. Business Software: The Production Gap

Read this reference when someone asks whether an AI skill, long prompt, or agent can replace a business application; when an expert-operated prototype is being commercialized; or when a consequential AI workflow needs a trustworthy architecture. This is a decision tool, **not** an argument that every workflow needs new SaaS.

> **Respect the complexity. Automate the routine.**
>
> An agent may replace part of a person's preparation and execution work. The need for valid data, domain constraints, authoritative state, traceability, and accountability does not disappear. Those responsibilities can live in existing software, a thin runtime, or a larger system.

## 1. The hidden operator: why a personal demo works

A capable user running a long prompt + skill + general agent often supplies four missing product functions:

1. **Domain context:** knows the intended outcome, assumptions, and what the source material leaves out.
2. **Orchestration:** knows how to prompt, select tools, retry, and correct the model's path.
3. **Oracle:** can recognize a plausible but wrong conclusion.
4. **Recovery and accountability:** fixes exceptions, approves decisions, and owns the downstream consequence.

This is a legitimate solution for expert-operated, low-stakes, or infrequent tasks. But **the creator being able to make it work is not evidence that a different user can depend on it**. Include the operator's debugging, prompt repair, and review in any measured cost.

**Transfer test:** Hand the same task, with unfamiliar or incomplete inputs, to a second intended user who does not know the prompt history. Observe task completion, error detection, recovery without developer help, and repeatability after a model or data change.

## 2. Choose the smallest responsible product layer

| Situation | Default mechanism | What must still be checked |
| --- | --- | --- |
| One expert, reversible task, few durable records | Prompt, skill, local script, or general-purpose agent | The expert accepts the review and recovery burden |
| Predictable structured task | Deterministic code and conventional UI | Correct inputs, reproducibility, clear errors |
| Variable documents or multi-step investigation | Bounded agent using validated tools | Missing evidence, tool authority, checkpoints and retries |
| Shared, consequential, recurring business workflow | Agent plus an authoritative business runtime | State, permissions, invariants, audit, reversibility and professional decisions |
| Existing mature system already owns the records and final action | Integrate or complement the incumbent narrowly | No duplicated records, approvals or downstream entry |

"AI replaces software" can be true for some **interfaces, repetitive tasks, and lightweight tools**. It is not evidence that persistent business rules, trusted state, or accountability have vanished. A new standalone app is justified only when the remaining job is large enough to pay for it.

## 3. Make the business contract explicit

Keep the runtime as thin as the job allows, but make its critical responsibilities observable:

- **Authority and identity:** which person or system owns each record, its version, period, and finality; separate raw observations from selected authoritative balances.
- **Domain invariants:** typed facts, constraints, versioned rules, deterministic money calculations and valid state transitions.
- **Agency and permissions:** narrow semantic tools, tenant/role/field scope, approval gates, safe writes, idempotency and rollback/compensation.
- **Evidence and truth states:** observed / assumed / proposed / reviewed / committed are not interchangeable; a source citation does not prove the passage supports the proposed treatment. Missing is `UNKNOWN`, not zero.
- **Durability and collaboration:** human corrections, exceptions, overrides, revisions and audit records survive reruns and personnel changes.
- **Integration:** what the downstream system actually accepted, recalculated or posted—not merely a generated CSV, successful API call or green toast.

AI can research, extract, classify, and recommend inside those contracts. High model confidence does not grant authority to write consequential facts.

## 4. Distill professional practice, not just online guidance

In tax, accounting, healthcare, legal or other regulated workflows, public guidance may state a rule without all of the facts, exceptions, client-specific choices and practical interpretation that determine its application. **Practice is evidence to examine, not a universal rule to copy.**

Work with qualified practitioners to capture:

- Required source documents and facts, including facts that **cannot** be inferred from a balance or a heading.
- Rule/version/jurisdiction, eligibility and exceptions; separate settled law/policy from a local practice convention or unresolved opinion.
- Treatment options, materiality, why a case needs human judgment, and what an adequate supporting document looks like.
- Representative accepted cases, counterexamples, disagreement cases and expected abstentions for regression/evaluation.

A strong product pairs **domain authority** with **product/interaction/engineering craft**. The former establishes what a defensible answer requires; the latter makes complicated work understandable, fast to correct, and safe to complete. Neither can substitute for the other. A small cross-functional team can validate a narrow wedge before expanding.

## 5. Make correction a first-class interaction

Static citations and explanations are useful but insufficient when the operator finds a wrong consequential number. Prefer one contextual loop:

`Result / Review finding -> actual calculation/source -> affected treatment -> propose or request correction -> deterministic before/after impact -> appropriate review -> observed downstream tie-out`

- Allow investigation without forcing the reviewer into a parallel transaction-by-transaction workflow.
- If the authoritative source is wrong, ask its owner to correct it; do not mask an upstream error with a downstream adjustment.
- For external calculations, show `External` / `Not independently traced` rather than inventing full lineage.
- Keep the prior approved snapshot intact and invalidate only the affected review/handoff status when data changes.

Human review should inspect **exceptions and consequential decisions**, not redo every mechanical step. For especially consequential outputs, a separate read-only reviewer agent may check original evidence independently; it cannot approve its own findings or replace accountable professional sign-off.

## 6. Productization is a reliability and economics test

A prototype proves one happy path. Product readiness requires risk-proportionate work on:

| Dimension | Ask |
| --- | --- |
| Edge cases | What happens with missing, inconsistent, duplicate, unsupported or unexpected facts? |
| Traceability | Can an operator locate the real source, governing rule, version and prior decision? |
| Correction and recovery | Can they edit/retry/undo without silent overwrite, double count or loss of work? |
| Evaluation | Do expert-accepted cases, negative cases and regressions catch material errors after changes? |
| Stable operation | Do permissions, concurrent actions, model drift, integration failures, monitoring and rollback behave acceptably? |
| UX and adoption | Can a new operator complete the job without the builder translating errors or writing prompts? |

Measure **completed, verified outcomes** and **net human minutes saved after checking, corrections and handoffs** against the installed workflow. A model that produces a plausible draft but forces a reviewer to reconstruct the entire job may have saved nothing. Do not multiply a successful bespoke demo into claims of repeatability, market size or compliance.

## 7. Ask these questions in a review

1. Which indispensable work is the expert currently doing *around* the AI?
2. Is a reusable skill sufficient, or does the job really require authoritative states, collaboration, and controlled side effects?
3. Which domain facts and practices are supported by original sources? Where should the agent abstain?
4. If the answer is wrong, can the user trace it, correct it at the right layer, and verify the downstream result?
5. Can a different intended user repeat the outcome, on a different case, without undocumented heroics?
6. Does the product reduce total professional effort enough to justify another tool?

**Decision principle:** Do not build a platform merely to package a prompt. Do not dismiss a business system because an expert can complete one flow with an agent. Find the smallest trustworthy product boundary that removes meaningful work.
