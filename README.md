# Agent Readiness Protocol

**An open standard for defining and verifying what AI agents need from enterprise environments before rollout.**

Agent deployments rarely stall because of the model. They stall on hidden dependencies: system access, SSO, data, security review, test environments, internal owners, and approval processes.

Agent Readiness Protocol turns those dependencies into a portable `readiness.yaml` contract.

## Five-minute demo

Install the skills:

```bash
npx skills add gedossman/codex-agent-readiness-protocol
```

Then tell Codex:

```text
Draft a readiness contract for this agent and preview its rollout at BlackRock.
```

## The contract

Every dependency is a plain-English `what` + `ready` pair: what the agent needs from the enterprise, and the observable condition that proves it is available.

```yaml
name: crm-automation-agent
version: 0.1.0
description: Automates CRM data entry and follow-up scheduling

requirements:
  - what: Read/write access to CRM contacts and opportunities
    ready: The agent creates a test contact and reads a test opportunity in staging
    canonical: integration.crm.api

  - what: Enterprise SSO for agent operators
    ready: A test user signs in through enterprise SSO and sees only authorized data
    canonical: auth.sso.saml

  - what: Security review and approval for the agent integration
    ready: Security review is complete and the integration is approved for production
    canonical: process.security-review

  - what: A data owner to map custom CRM fields
    ready: The field mapping is reviewed and approved by both teams
    canonical: stakeholder.data-owner

optional:
  - what: Webhook access for real-time CRM updates
    ready: The agent receives a test event within five seconds of a CRM update
    canonical: integration.webhook.outbound
```

## Skills

| Skill | Purpose |
|---|---|
| `draft-agent-readiness` | Scan an agent project and draft `readiness.yaml` |
| `preview-agent-rollout` | Preview rollout at a specific enterprise—timeline, stakeholders, blockers, and risks |
| `agent-readiness-protocol` | Load the protocol format, categories, and design rules |

## Dependency categories

| Category | Covers |
|---|---|
| `integration.*` | CRM, ERP, ticketing, email, analytics, and webhooks |
| `auth.*` | SSO, API credentials, service accounts, and permissions |
| `data.*` | Historical exports, sample data, field mapping, and data quality |
| `infra.*` | Test environments, network access, hosting, and observability |
| `stakeholder.*` | Business owners, security, IT, legal, and executive sponsors |
| `process.*` | Security, privacy, legal, procurement, training, and change management |

## How it works

1. **Draft** — The vendor uses Codex to identify every enterprise dependency.
2. **Deliver** — The vendor shares the versioned `readiness.yaml` contract with the enterprise.
3. **Resolve** — Both teams work through requirements in dependency order.
4. **Verify** — Each item closes only when its `ready` criterion is demonstrably true.

The repository is standalone and has no runtime, hosted-service, registry, or proprietary platform dependency.

## OpenAI Build Week

Agent Readiness Protocol was packaged and published with OpenAI Codex during OpenAI Build Week on July 21, 2026.

The copy-ready submission story is in [PROJECT_STORY.md](PROJECT_STORY.md).

## License

MIT — Agent Readiness Protocol contributors
