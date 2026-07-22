---
name: preview-agent-rollout
description: Preview an AI agent's rollout at a specific enterprise from readiness.yaml. Use when a vendor wants likely timelines, stakeholders, dependency order, parallel workstreams, blockers, and risks for an enterprise deployment.
---

# Preview agent rollout

Turn a readiness contract into an evidence-bounded enterprise rollout preview.

## Workflow

1. Read `readiness.yaml`; if it does not exist, use `draft-agent-readiness` first.
2. Load `../agent-readiness-protocol/references/spec.md`.
3. Build a cautious company profile from user-provided or well-sourced public facts: sector, scale, known systems, and regulatory environment.
4. For each requirement, identify likely stakeholders, prerequisites, complexity, risks, and evidence gaps.
5. Order requirements by dependency, identify the critical path, and group work that can run in parallel.
6. Present the preview with assumptions clearly separated from verified facts.

## Output

- Requirement-by-requirement resolution approach
- Likely stakeholders and owners
- Complexity and risks
- Dependency order and critical path
- Parallel workstreams
- Unknowns requiring enterprise confirmation

Do not claim a company uses a system, has approved access, or satisfies a requirement without evidence.
