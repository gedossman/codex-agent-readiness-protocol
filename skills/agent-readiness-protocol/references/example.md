# Example enterprise agent contract

```yaml
name: support-agent
version: 0.1.0
description: Resolves tier-one customer support requests

requirements:
  - what: Read access to the customer support knowledge base
    ready: The agent retrieves approved answers for 20 representative test questions
    canonical: data.knowledge-base.read

  - what: Ticketing access to read tickets and add internal notes
    ready: The agent reads a test ticket, adds a note, and updates its status in staging
    canonical: integration.ticketing.api

  - what: Enterprise SSO for support operators
    ready: A test support user signs in and sees only tickets allowed by their role
    canonical: auth.sso.saml

  - what: A support owner to approve escalation rules and tone
    ready: The owner approves the escalation matrix and response guidelines
    canonical: stakeholder.business-owner

  - what: Security and privacy review
    ready: Both reviews are complete and the agent is approved for the intended customer data
    canonical: process.security-review

optional:
  - what: Real-time customer sentiment signals
    ready: The agent receives a test sentiment score during a support session
    canonical: integration.analytics.api
```
