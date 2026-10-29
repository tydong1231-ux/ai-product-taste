# AI Product Taste

A reusable AI Skill for **reviewing product features, designing AI-native workflows, and challenging product strategy**. It favors sound judgment over AI feature checklists.

**Core philosophy:** Start with the customer's job, respect the evidence, assign work to the right mechanism, and measure a verified outcome rather than a compelling demo.

> **Authority before autonomy.** An agent's ability to perform an action does not grant it authority to make the business decision or commit the result. Delegate autonomy by action, evidence, permissions, risk, independent verification, and recoverability—not model confidence alone.

## Three modes

| Mode | Use it for | Output |
| --- | --- | --- |
| **Feature Review** | PRDs, prototypes, code, workflows, shipped features | Verdict, material issues, fixes, acceptance tests |
| **Design Assistance** | AI-native products, agent workflows, human review UX | Main flow, authority boundaries, failure handling, MVP |
| **Product Direction Review** | ICP, positioning, pricing, GTM, roadmap, build-vs-buy | Build / Narrow / Pivot / Defer / Stop and validation plan |

## Seven decision lenses

| Lens | Ask |
| --- | --- |
| **Customer and job** | Who needs which completed outcome, and what do they do today? |
| **Evidence and authority** | What is known, assumed, missing, or proposed? Who owns the source, rule, decision, and final record? |
| **Right mechanism** | Is the smallest sufficient solution code, conventional UI, a skill, an agent, an integration, or a governed platform? |
| **Delegated autonomy** | What may the agent observe, propose, prepare, or commit? Are permission, evidence, checks, consequences, and recovery adequate for *this action*? |
| **Human attention** | Does the person decide consequential exceptions—or redundantly repeat machine-verifiable work? |
| **Verified completion** | Did the receiving system actually accept the intended result? What happens on partial failure or correction? |
| **Net value and focus** | After review, rework, integration, risk, and operating cost, is this still worth building? What should not be built? |

**Design implications:** Build around work, authoritative state, and the user's next decision—not necessarily a chat window. Keep `observed`, `proposed`, `approved`, `committed`, and `verified` distinct. Make missing information visible, preserve corrections, and let users trace and repair consequential results. Use the smallest trustworthy control layer; mature systems of record should not be duplicated without a real reason.

**Two reality checks:** A successful expert-driven agent demo does not establish that a new operator can repeat the outcome without hidden debugging. And an AI workspace that creates duplicate entry beside existing software may *increase* work despite accurate outputs.

See [Design Assistance](tingyu-ai-product-decision-framework/references/design-assistance.md) for actionable autonomy and UX decisions, [agent vs. business software](tingyu-ai-product-decision-framework/references/agent-vs-business-software.md) for productization, and [incumbent workflow boundaries](tingyu-ai-product-decision-framework/references/incumbent-workflow-boundaries.md) for system-of-record handoffs.

## Try it

> Review this proposed auto-approval flow. Identify who owns the decision, which actions could be safely delegated, failure paths, and how to prove net work saved.

> Design a workflow that uses AI to interpret messy inputs but keeps final state, corrections, and consequential decisions trustworthy. Use ordinary UI where it beats chat.

> Challenge this agent product strategy. Does it remove a meaningful step from the current workflow, or merely add another application? What is the smallest viable wedge?

Install the [`tingyu-ai-product-decision-framework/`](tingyu-ai-product-decision-framework/) folder in an AI assistant that supports Skills, or package the folder as a Skill ZIP. No MCP server, API key, or private project access is required.

**Operating principle:** Respect complexity. Automate routine work. Maximize trustworthy delegation, not autonomous activity.

[MIT License](LICENSE) · Maintained by [Tingyu Dong](https://github.com/tydong1231-ux).
