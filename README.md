# AI Product Taste

A reusable AI Skill for reviewing product features, designing AI-native workflows, and evaluating product direction.

The framework weighs user value, technical feasibility, agent autonomy, trust, and business economics, rather than treating AI as a feature checklist.

Use it with an AI assistant to **review existing features, design AI-native workflows, or challenge product strategy**. It prioritizes clear reasoning, real user value, trustworthy AI/agent boundaries, and concise, actionable recommendations.

## Three modes

| Mode | Use it for | Output |
| --- | --- | --- |
| **Feature Review** | PRDs, prototypes, workflows, shipped features, code | Verdict, key issues, fixes, acceptance checks |
| **Design Assistance** | Product flows, AI/agent actions, human-in-the-loop UX | Practical design, role boundaries, edge cases, MVP |
| **Product Direction Review** | ICP, business ideas, positioning, GTM, pricing, roadmaps | Build / Narrow / Pivot / Defer / Stop, with a validation plan |

**Core ideas:** Start with the customer and the job. Promise only what the data supports. Use code for deterministic truth, AI for ambiguity, agents for bounded execution, and people for consequential judgment. Measure the complete outcome **minus the cost of verification**. Explicitly decide what *not* to build.

## Decision framework

| Lens | Question to answer |
| --- | --- |
| Customer and job | Who is the buyer, and which recurring task is painful enough to solve? |
| Data readiness | What evidence is available, what is missing, and what cannot be inferred? |
| Right mechanism | Should this be code, UI, a model, a bounded agent, or a human decision? |
| Consequential actions | What needs validation, explicit permission, review, and recovery? |
| Business outcome | Does the complete workflow save time **after** verification and exceptions? |
| Strategic choice | What should we build, narrow, defer, pivot, or stop—and why? |

The Skill is deliberately opinionated about **scope and evidence**, not about always adding more AI. A model's plausible answer is not a verified business result.

## Try a concrete product review

Use this **illustrative** scenario with the Feature Review mode:

> We want an AI agent to automatically approve bank-transaction matches whenever model confidence is high. Review the product decision, identify the most important failure modes, propose a safer first version, and tell us how to measure real time saved after accounting for review and corrections.

A useful review should address false accepted matches, required supporting evidence, authoritative accounting APIs, exception handling, and a measurable release criterion. It should not merely suggest a higher confidence threshold or say to keep a human in every loop.

You can also try Design Assistance for the end-to-end review UX, or Product Direction Review to decide whether the feature is the best next investment.

## Use

Install the [`tingyu-ai-product-decision-framework/`](tingyu-ai-product-decision-framework/) folder in an AI assistant that supports custom Skills, or zip that folder for clients that accept Skill ZIP uploads. Installation options vary by client. **No MCP server, API key, or private project access is required.**

Try:

> Review this PRD with AI Product Taste. Identify the three most important risks, recommend the smallest useful changes, and tell me how to verify them.

> Help me design this agent workflow. Show what code, AI, the agent, and the human should each own.

> Challenge our product direction. Choose a narrow ICP, a paid outcome, what not to build, and the fastest test.

This Skill does not access private projects or employer systems. [MIT License](LICENSE).

Maintained by [Tingyu Dong](https://github.com/tydong1231-ux).
