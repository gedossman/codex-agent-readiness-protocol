## Inspiration

AI agents are powerful, but enterprise rollouts often stall on missing system access, SSO, data, security reviews, unclear ownership, and internal approvals. We wanted vendors and enterprises to agree on readiness before deployment begins.

## What it does

Agent Readiness Protocol creates a `readiness.yaml` contract defining what an AI agent needs from an enterprise. Every dependency includes what is required and a verifiable criterion showing when it is ready.

## How we built it

We used OpenAI Codex to create three installable skills: one drafts the readiness contract, one previews rollout at a specific enterprise, and one provides the protocol specification and dependency categories.

## Challenges we ran into

The main challenge was making enterprise requirements simple but verifiable. We solved this with clear `what` and `ready` pairs covering integrations, authentication, data, infrastructure, stakeholders, and approval processes.

## Accomplishments that we're proud of

We created a small, standalone protocol that teams can understand quickly and use before deployment. It produces clear requirements, likely stakeholders, rollout risks, parallel workstreams, and a critical path.

## What we learned

Successful agent deployment is a coordination problem as much as a technical problem. Making dependencies explicit early lets security, IT, data, legal, and business teams work in parallel.

## What's next for Agent Readiness Protocol

Next we will add a JSON Schema, a lightweight validator, reusable industry profiles, and a GitHub Action that checks readiness contracts when agent requirements change.
