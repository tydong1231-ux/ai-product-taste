# Incumbent Workflow Fit: Wedge, Authority, and Handoff

Read when an AI product competes with mature professional software, sits between existing systems, or risks making users repeat work. Use for **Product Direction** and **Design Assistance**. The example below is hypothetical; it does not establish adoption, capability parity, or any legal requirement.

## 1. Start with the existing workflow—not the AI product

Trace the completed job: **upstream source of record -> preparation / engagement workpapers -> downstream specialist tool -> reviewed outcome**.

For each step, determine:

| Dimension | Question |
| --- | --- |
| Owner and current tool | Who performs it, who pays, who reviews, and who remains accountable? |
| Output and authority | What record or deliverable does it produce? Which version is final? |
| Incumbent capability | Is it supported, partly assisted, automatic in real use, or unknown? |
| Residual labor | Which classifications, document investigations, choices, and reviews still consume time? |
| Handoff | What export/import already exists? Who has to re-enter or reconcile data? |
| Failure and adoption cost | What can be wrong or duplicated? What needs setup, training, or migration? |

A feature list is neither proof of complete automation nor proof of unmet need. Verify a relevant vendor capability, then observe how the practitioner uses it. Do not promise to automate looking up a document or preparing an asset schedule unless the product can actually access the required material.

## 2. Choose the position before the feature set

| Product position | Viable if | Weak if |
| --- | --- | --- |
| **Replace manual workpapers** | A repeatable, material artifact is still built outside the installed software, often in spreadsheets. | The manual task is infrequent, trivial, or depends on inaccessible facts. |
| **Complement a mature incumbent** | A specific exception or investigative job survives, and existing source and output can be reused. | The new app becomes a third system of record or cannot deliver its result back. |
| **Replace the whole incumbent** | The buyer wants to replace its complete job, including reporting, reviews, collaboration, evidence, audit trails, and continuity. | The pitch duplicates one small feature while ignoring the platform's other valuable responsibilities. |
| **Do not add a product** | The current workflow already finishes the job cheaply or safely enough. | A technically impressive demo cannot beat setup and verification costs. |

Define the ICP by **buyer + recurring job + case complexity + installed tool stack + residual human effort + switching behavior**. Firm size, number of small businesses, or exemption from an unrelated professional reporting requirement cannot reliably estimate buyers. A small firm can still require professional engagement tools; a larger specialist team may not.

## 3. Establish a source-of-truth contract

1. **Accountable upstream result.** Identify who finalized the source and its period/version. A successful import confirms format; a human's "final" declaration identifies an accepted source but does not prove independent professional compliance. Final adjusted/reporting balances may differ from earlier transaction exports.
2. **Optional investigative evidence.** Raw ledger detail, receipts, contracts, or event histories explain the character of finalized amounts. They do not silently replace accepted upstream balances. Request detail only where needed and available.
3. **Reporting taxonomy.** Map to an external reporting scheme when required. Correct mapping is not proof of correct underlying accounting or appropriate legal/tax treatment. Test identity, periods, signs, contra accounts, unmapped items and duplicates.
4. **Domain treatment and calculation.** Keep observed facts, model proposals, human choices, rules and calculations distinct. Missing evidence means unknown, not zero or consent. Rule correctness is different from the factual premise on which it runs.
5. **Downstream authority.** A specialist system may already own historic attributes, final schedules, validations, and submission. Reuse them when possible; do not build a competing authoritative copy or claim an export is an accepted filing.

Use separate states where material: **imported -> upstream-finalized -> mapping-reconciled -> domain-reviewed -> downstream-verified**. Trace the responsible actor, rule/version and supporting source at each transition. If source books or master data appear wrong, send a correction to their owner and import the revised final result rather than hiding the error in a downstream adjustment.

## 4. Deliver the smallest usable output

A proposed AI workpaper should contain only what the receiving workflow needs:

- **Baseline:** accepted source identity/version, period, currency, authoritative amounts, existing classification and reconciliation.
- **Reviewable change:** proposed adjustment or decision; affected source items, amount/direction, rule basis, evidence, status and reviewer decision.
- **Unknowns:** precisely what supporting fact is missing, why it matters and who can provide it; avoid invented values.
- **Destination:** tested form/field and version, existing value or explicit UNKNOWN, allowed action **NEW / REPLACE / VERIFY_ONLY / NO_WRITE**, approval and idempotent retry.
- **Outcome:** real import or honest manual handoff, downstream comparison, provenance and readiness state; do not label the result posted/filed/completed without observing that state.

Validate the *actual* external template and field identifiers, import eligibility, overwrite behavior, repeated imports, recalculation, and reconciliation. A syntactically correct spreadsheet, CSV or JSON file alone is not a proven integration.

Avoid asking professionals to maintain mappings, carryforwards and decisions twice. Prefer referencing existing records or reviewing only the **delta** when the incumbent already owns the rest.

## 5. Test the economics before a large refactor

Shadow permissioned, appropriately anonymized **completed real jobs**. Record the incumbent baseline from final source through the downstream reviewer-ready outcome: import, classification, investigation, evidence gathering, human decisions, checking, client requests, handoff, double entry and corrections. Re-run the same case with the proposed agent.

Measure net human minutes, serious errors, false confirmations, missing evidence, reviewer re-investigation, and receipt by the downstream tool. State the unit and denominator. A pilot proves feasibility, not total market size or professional certification.

**Narrow or stop** when the residual job is too small, required source documents are unavailable, checking/re-entry absorbs the time saved, a real handoff is not possible, or correct results cannot be professionally verified. Preserve tested components without continuing to build a full replacement simply because coding is possible.

## 6. Hypothetical professional-services example

A practitioner receives finalized accounts and submits filings through a specialist tool, but still manually prepares certain adjustments in a spreadsheet. An AI tool might replace that manual artifact by accepting the final amounts, investigating selected details only where there is evidence, producing a reviewable adjustment register, and handing the accepted changes to the existing filing tool.

A different practitioner already uses an engagement platform with tax working papers and a direct export to the filing tool. The same AI app risks duplicating the workflow. Only a demonstrably costly unresolved exception, with an inexpensive verified handoff, justifies adding it.

**Portable rule:** Compete to remove a meaningful human step, not to reconstruct a full workflow the customer already trusts.
