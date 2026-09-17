# Governed Agentic Engineering

A sanitized technical showcase of an in-development supervisory agentic system intended to automate low-risk software-engineering workflows while preserving deterministic controls, auditability, and explicit human approval for consequential actions.

> **Status:** Architecture complete enough for implementation preparation; staged implementation is beginning. This repository does not claim a fully deployed autonomous engineering system.

## What this project demonstrates

- Agentic system architecture
- Specialist-agent orchestration
- Deterministic policy and approval boundaries
- Human-in-the-loop governance
- Risk-based action classification
- Tool-gateway design
- Auditability and evidence-driven workflow state
- Cost controls and bounded automation
- Separation between reasoning, authorization, and execution

## Core operating principle

```text
AI agents reason and propose
        |
        v
Deterministic services evaluate policy / authority
        |
        v
Tool gateways execute only authorized actions
        |
        v
Evidence updates workflow state
        |
        v
Human approval remains mandatory at consequential boundaries
```

## High-level architecture

The planned system uses a supervisory manager with deterministic shared services and a specialist-agent pool.

### Deterministic services

- workflow/state engine
- policy engine
- approval engine
- cost controller
- audit service
- notification service
- tool gateway
- scheduler / next-work selector
- lock and idempotency controls

### Specialist capabilities

- planning / product reasoning
- development
- independent review
- QA / test interpretation
- release / deployment preparation
- maintenance / incident analysis
- support drafting
- feedback / product intelligence

Specialists are invoked only when a bounded workflow needs them; they are not treated as unrestricted autonomous processes.

## Risk model

The design distinguishes low-impact observation from higher-impact actions. Read-only inspection may be automatic, while consequential actions such as production deployment, secret changes, database migrations, permission changes, destructive operations, or material financial actions require explicit human approval.

## Implementation philosophy

The system is intended to earn autonomy progressively:

1. local orchestration skeleton
2. deterministic mocks
3. communication / approval integration
4. read-only external integrations
5. shadow mode
6. observational autonomy
7. limited low-risk writes
8. bounded development automation
9. qualified low-risk merge automation
10. human-gated production operations

## Repository scope

This repository is a **public-facing architecture and engineering showcase**. It intentionally excludes:

- private product names and internal project identifiers
- production credentials and infrastructure secrets
- exact private repository structure
- customer or merchant data
- internal authorization records
- operational channel identifiers
- sensitive deployment targets and environment values

## Why this public version exists

The goal is to demonstrate how agentic AI can be engineered as a governed software system rather than treated as unrestricted model autonomy.

## Next additions

Planned public-safe additions include:

- risk-model documentation
- human-approval design
- specialist-agent contract examples
- state-machine examples
- implementation notes as the private system progresses
