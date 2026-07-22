# Agent Readiness Protocol

This repository is a standalone, documentation-first skill pack for enterprise agent rollouts.

Install it with:

```bash
npx skills add gedossman/codex-agent-readiness-protocol
```

Keep every readiness requirement in plain English with a specific `what` + `ready` pair. Describe only dependencies the enterprise must resolve before an AI agent can deploy successfully. Never invent company systems, access, regulatory obligations, stakeholders, or approvals.

Validate every changed skill with:

```bash
python3 "$HOME/.codex/skills/.system/skill-creator/scripts/quick_validate.py" skills/<skill-name>
```

## Skills

| Skill | Purpose |
|---|---|
| `draft-agent-readiness` | Draft an enterprise rollout contract |
| `preview-agent-rollout` | Preview rollout at a specific enterprise |
| `agent-readiness-protocol` | Protocol specification and dependency categories |
