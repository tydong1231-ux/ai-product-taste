# Reusable Product Patterns (Generalized)

Use at most one or two when they genuinely clarify a recommendation. These are portable patterns, not claims about the implementation, users, or results of any named private project.

## 1. Matching: precision before coverage

For high-risk matches, amount similarity alone is insufficient. Narrow candidates with deterministic filters; let AI interpret messy references; allow `no match`. Track false accepted matches and reviewer time, not match percentage alone. Use weaker thresholds only where the cost of mistakes is low and reversibility is high.

## 2. Document intake: draft, validate, advance

Extract into constrained fields, run deterministic consistency and completeness checks, then advance supported states. Keep unsupported or missing evidence visible. On re-import, preserve prior human corrections unless new source evidence invalidates them.

## 3. Deterministic engines: facts do not come from the model

Compute monetary values, policy eligibility, and other reproducible rules in code with versioned inputs. Agents may interpret documents, draft scenarios, and explain results, but should not invent the numbers or silently fill unknown values. Trace consequential outputs back to evidence and explicit assumptions.

## 4. Review: focus on judgment, not rows

Group similar cases, present a defensible recommendation, show its impact and evidence, and let the reviewer accept or correct only meaningful differences. Store the human choice and its scope so later AI runs cannot overwrite it silently.

## 5. Governed agent tools: reusable capability, narrower authority

Use semantic tools with authenticated scope, declared inputs, validation, traceable outcome, and recovery. Agent-specific permissions may be stricter than the web user's permissions. Keep the system of record authoritative; do not expose broad database or arbitrary HTTP writes.

## 6. Multi-step agent: stage-by-stage verification

Use a planner for the overall job and bounded executors for observable milestones. Each stage has success criteria, limited authority, and evidence of effect. If needed context is absent, return `needs guidance` rather than guessing. Orchestrate full workflows only after the local steps can reliably complete.

## 7. Truthful readiness: verify the actual artifact

A `Downloaded`, `Completed`, or `Ready` label should correspond to persisted, usable state, not a successful API response alone. Reopen offline or after a retry and verify. Test the final user outcome, not merely intermediary events.

## 8. Data ceiling: sell the answer you can support

A product with payments and invoices may reliably explain historical cash movement while lacking the plans and operational dimensions required to advise on expansion. State what the product knows, what it infers, and what must be supplied by a person. Record important assumptions as structured, expiring context.

## 9. Workflow wedge before broad agent vision

Start with a narrow repeatable paid job; expand across adjacent steps only after credible data, approvals, and a recovery path exist. A conversational assistant or a dashboard with many answers is not proof that any important work is complete.

## 10. Role-specific surface over agent-first everything

A business owner may want `What changed / Why / What now?`; an expert operator may need `What is blocked / What needs review / How do I fix it?`. Prioritize information by role while preserving the same underlying system of record. For direct edits, traditional UI may be faster than chat.

## 11. Enterprise integration and reuse

Before promising to replace a mature system, pilot one measurable cross-system workflow. Document handoffs, required mappings, review labor, and implementation cost. The second customer's reuse is the test for scalable software, not the first customer's successful custom deployment.

 
## 12. The third-system trap: find the residual job first

A buyer already uses a ledger or CRM, professional workpaper software, and a specialist execution or filing tool. Ask what each **actually automates** and what still needs human investigation. An AI product requiring the user to export, re-code, and re-enter facts may increase work even when it computes the right result. Prefer replacing a truly manual artifact or a measurable exception job; otherwise integrate narrowly with the incumbent or do not build.

## 13. Final record for amounts, raw detail for investigation

A professionally finalized balance or state is the selected source of record; raw transactions may omit later adjustments. Use transaction-level data to understand how to treat a finalized amount, not to silently override it. If sources disagree, flag the discrepancy or ask the upstream owner for a corrected version. Keep reporting classification, domain-specific treatment, deterministic arithmetic, and professional approval as separate gates.

## 14. Review-ready delta, not a second full system

Produce the specific decision or adjustment needed downstream: amount, direction, explanation, grounded source, review state, tested target, and NEW / REPLACE / VERIFY_ONLY / NO_WRITE action. Existing target values must be inspected or explicitly marked unknown. Reuse already-owned mappings, opening balances, and choices rather than asking the user to maintain them in two products. An untested export is not an integration.

## 15. Expert objections: isolate warning from overclaim

An experienced practitioner says a prototype skipped basic input normalization. Treat that as a potential serious correctness gap and test it. Do not automatically accept an additional sweeping claim that every customer must use one named vendor or accounting basis. Find a concrete failing case, clarify who owns the underlying record, and test with qualified users. Avoid treating either a plausible demo or expert approval as market validation.
