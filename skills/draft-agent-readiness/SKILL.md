---
name: draft-agent-readiness
description: Scan an AI-agent project and draft a readiness.yaml contract declaring what it needs from an enterprise before rollout. Use when a vendor wants to prepare agent onboarding, expose deployment blockers, or define verifiable enterprise requirements.
---

# Draft agent readiness

Create the smallest complete `readiness.yaml` contract for the agent's enterprise rollout.

## Workflow

1. Read product, setup, architecture, integration, authentication, data, deployment, security, and operations documentation.
2. Load `../agent-readiness-protocol/references/spec.md` and follow its schema.
3. Identify enterprise dependencies across integrations, authentication, data, infrastructure, stakeholders, and processes.
4. Separate blocking requirements from optional improvements.
5. Write one plain-English `what` + `ready` pair per dependency.
6. Add a canonical identifier only when it matches a defined category and meaning.
7. Write `readiness.yaml` and summarize the likely critical blockers.

## Rules

- Describe what the enterprise must provide or complete, not internal vendor tasks.
- Include human owners and approval processes when they can block rollout.
- Make every `ready` criterion specific and observable.
- Do not combine multiple dependencies into one item.
- Do not invent enterprise systems, regulatory obligations, access, or approvals.
- Do not include secret values, private data, or confidential endpoints.
