# Implementation Roadmap

This public roadmap is intentionally high-level and omits private infrastructure identities, credentials, and product-specific actions.

## Phase 1 — Local orchestration foundation

Build the local repository, schemas, persistent workflow state, event model, deterministic policy engine, and audit trail.

## Phase 2 — Mock integrations

Exercise workflows against deterministic mocks before connecting real external systems.

## Phase 3 — Approval channel

Introduce a structured human-approval interface for consequential transitions.

## Phase 4 — Read-only integrations

Connect selected external systems in observation-only mode and reconcile authoritative external state.

## Phase 5 — Shadow mode

Allow the Manager to classify and plan work without executing consequential mutations.

## Phase 6 — R0 autonomy

Enable proven read-only / observational automation.

## Phase 7 — Limited R1 writes

Permit selected reversible repository actions under deterministic policy.

## Phase 8 — Development-agent automation

Add bounded implementation workflows with independent review and validation.

## Phase 9 — Qualified low-risk merge automation

Allow narrowly defined merges only after evidence and policy gates are demonstrated reliable.

## Phase 10+ — Human-gated production operations

Add production observation, release preparation, and later explicitly approved deployment actions while retaining mandatory human control over consequential changes.

## Success criteria

The design is successful only if it reduces coordination effort without sacrificing control. Key target properties include:

- no unauthorized consequential action
- no secret leakage
- no stale approval execution
- attributable/auditable autonomous actions
- deterministic policy enforcement
- graceful stop/fail-closed behavior under uncertainty

Implementation status should be updated only when evidence exists; roadmap intent must not be represented as completed capability.
