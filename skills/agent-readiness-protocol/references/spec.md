# `readiness.yaml` specification

## Schema

```yaml
name: string
version: string
description: string

requirements:
  - what: string
    ready: string
    canonical: string

optional:
  - what: string
    ready: string
    canonical: string
```

## Fields

| Field | Required | Meaning |
|---|---|---|
| `name` | Yes | Kebab-case agent or solution identifier |
| `version` | Yes | Semantic version of the readiness contract |
| `description` | Yes | One-line description for enterprise stakeholders |
| `requirements` | Yes | Blocking enterprise dependencies; at least one |
| `optional` | No | Non-blocking dependencies that improve rollout |
| `what` | Yes | What the agent needs from the enterprise, in plain English |
| `ready` | Yes | The observable outcome proving the dependency is resolved |
| `canonical` | No | Stable dependency identifier for deterministic matching |

## Canonical categories

| Prefix | Scope |
|---|---|
| `integration.*` | CRM, ERP, ticketing, email, analytics, and webhooks |
| `auth.*` | SSO, credentials, service accounts, roles, and permissions |
| `data.*` | Historical exports, samples, mapping, quality, and retention |
| `infra.*` | Test environments, network access, hosting, and observability |
| `stakeholder.*` | Business owners, data owners, security, IT, legal, and sponsors |
| `process.*` | Security, privacy, legal, procurement, training, and change management |

## Validation rules

- Use lowercase kebab-case for `name`.
- Use semantic versioning for `version`.
- Include at least one blocking requirement.
- Give every item non-empty `what` and `ready` fields.
- Write one dependency per item.
- Write `ready` as a specific observable outcome, not “access granted” or “setup complete.”
- Keep contracts free of credentials, private data, and confidential endpoints.
- Do not invent canonical identifiers.

## Design principles

1. Plain English comes first.
2. `what` + `ready` is the atomic unit.
3. Contracts are versioned because rollout dependencies change.
4. Canonical identifiers enable matching but are optional.
5. Technical, data, human, process, and infrastructure dependencies share one format.
