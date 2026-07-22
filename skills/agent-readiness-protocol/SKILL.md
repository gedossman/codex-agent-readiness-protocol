---
name: agent-readiness-protocol
description: Define and interpret the Agent Readiness Protocol for enterprise AI-agent rollouts. Use when Codex needs the readiness.yaml format, dependency categories, design rules, or examples for declaring what an agent needs from an enterprise before deployment.
---

# Agent Readiness Protocol

Treat `readiness.yaml` as a versioned contract between an agent vendor and an enterprise.

## Apply the protocol

1. Read [references/spec.md](references/spec.md) before creating or interpreting a contract.
2. Read [references/example.md](references/example.md) when a concrete enterprise rollout example would improve accuracy.
3. Require a plain-English `what` + `ready` pair for every dependency.
4. Treat every item in `requirements` as blocking and every item in `optional` as non-blocking.
5. Use canonical identifiers when the dependency fits a known category; otherwise keep the plain-English requirement without inventing an ID.
6. Describe observable enterprise outcomes, not vendor implementation tasks.

## Preserve evidence boundaries

- Never claim an enterprise uses a system without evidence.
- Never infer access, approval, compliance, or stakeholder commitment from public information alone.
- Never include credentials, private data, or confidential infrastructure details.
- Keep uncertainty explicit in rollout previews.
