# Governed Agentic Engineering

A public-safe architecture and implementation showcase for a supervisory agentic system designed to automate low-risk software-engineering work while preserving deterministic policy controls, auditability, and explicit human authority over consequential actions.

> **Current status:** architecture and implementation preparation are established; staged implementation is beginning. This repository intentionally does not claim a fully deployed autonomous engineering platform.

## At a glance

| Area | Design direction |
| --- | --- |
| Orchestration | Event-driven supervisory manager with specialist-agent capabilities |
| Governance | Deterministic policy and approval engines constrain AI-proposed actions |
| Execution | Tool gateways execute only actions that pass authority and policy checks |
| Risk | Actions are classified from observational/low-risk through consequential/high-impact |
| Evidence | Workflow state changes are tied to explicit validation and audit evidence |
| Human control | Production deployment, secrets, migrations, destructive actions, and other consequential operations require approval |
| Reliability | Cost controls, idempotency, locks, recovery logic, and kill switches are part of the design |

## What I am building

The project explores a practical alternative to unrestricted software agents. Instead of giving an AI model broad authority, the system separates **reasoning, authorization, execution, and evidence**.

```text
AI specialist proposes work
        |
        v
Deterministic policy / authority evaluation
        |
        v
Approved tool gateway execution
        |
        v
Independent review + validation evidence
        |
        v
Workflow state transition
        |
        +----> human approval whenever the boundary is consequential
```

## What this demonstrates

- agentic system architecture
- specialist-agent orchestration
- deterministic policy and approval boundaries
- human-in-the-loop governance
- risk-based action classification
- tool-gateway and least-authority design
- workflow state machines
- independent review / QA separation
- auditability and evidence-driven transitions
- idempotency, locking, cost controls, and kill-switch thinking
- progressive autonomy rather than unrestricted automation

## Specialist capabilities

The planned system separates logical specialist roles such as:

- planning / product reasoning;
- bounded development;
- independent review;
- QA / test interpretation;
- release/deployment preparation;
- maintenance and incident analysis;
- support drafting;
- feedback and product-intelligence analysis.

These specialists are invoked only when a bounded workflow needs them; they are not treated as permanently autonomous processes.

## Risk and authority model

The design uses progressively stronger controls as impact rises:

- **R0 — observational:** repository state, logs, health, documentation reads;
- **R1 — low-risk / reversible:** bounded development branches, tests, routine documentation;
- **R2 — meaningful / controlled:** larger changes, dependency work, release preparation;
- **R3 — consequential:** production deployment, secrets, migrations, destructive operations, financial actions, major permission changes.

AI may propose risk, but deterministic policy can retain or raise it. Consequential actions remain human-controlled.

## Implementation path

1. local orchestration and state model;
2. deterministic mock integrations;
3. approval/communication integration;
4. read-only external integrations;
5. shadow mode;
6. observational autonomy;
7. limited reversible writes;
8. bounded development automation;
9. qualified low-risk merge automation;
10. human-gated production operations.

## Public-safe workflow example

See [`examples/workflow-state-example.md`](examples/workflow-state-example.md) for a fictional task showing how a work item can move from creation through risk assessment, authorization, execution, review, validation, and approval without exposing any private repository or production details.

## Repository scope

This repository is a **sanitized technical showcase**. It intentionally excludes:

- private product names and private repository identifiers;
- credentials, secrets, production endpoints, and operational channel IDs;
- internal authorization records;
- customer/merchant data;
- exact production policies and deployment targets;
- private infrastructure details that could broaden operational access.

## Current limitations

The architecture is significantly more mature than the current implementation. The public repository therefore distinguishes clearly between **designed**, **being implemented**, and **operationally qualified** capabilities rather than presenting planned autonomy as already deployed.

## Additional notes

- [`docs/risk-and-approval-model.md`](docs/risk-and-approval-model.md) — authority boundaries
- [`docs/implementation-roadmap.md`](docs/implementation-roadmap.md) — staged rollout direction
- [`docs/agent-contract-example.md`](docs/agent-contract-example.md) — public-safe specialist contract pattern

---

**Why this repository exists:** to demonstrate how agentic AI can be engineered as a governed software system with explicit authority, evidence, and human control rather than unrestricted model autonomy.