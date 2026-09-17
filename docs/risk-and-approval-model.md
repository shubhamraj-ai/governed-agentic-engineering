# Risk and Approval Model

## Purpose

The system separates *what an AI recommends* from *what the system is allowed to do*.

AI components may assist with planning, diagnosis, implementation, review, or prioritization, but authority is enforced by deterministic services and explicit policy.

## Risk classes

A simplified public model uses four levels:

### R0 — Observational

Examples:

- read repository state
- inspect logs
- read test results
- perform health checks
- read documentation

Default posture: automatic.

### R1 — Low-risk and reversible

Examples:

- create an approved development branch
- make bounded implementation changes
- run relevant tests
- update documentation
- prepare a pull request

Default posture: automation may proceed when policy conditions are satisfied.

### R2 — Meaningful / controlled

Examples:

- larger feature work
- selected dependency updates
- non-trivial maintenance
- release preparation

Default posture: automation is possible, but transitions depend on stronger evidence and policy checks.

### R3 — Consequential

Examples:

- production deployment
- environment-secret changes
- database migration
- permission or scope changes
- destructive data actions
- billing/refund actions
- DNS/domain changes
- material financial actions

Default posture: explicit human approval required.

## Policy precedence

AI may suggest a risk level, but deterministic policy may keep or increase it. Policy must not silently lower a risk classification merely because an agent is confident.

On disagreement between model output and deterministic policy, deterministic policy wins.

## Approval properties

A consequential approval should be:

- specific to one workflow/run
- bound to the intended target
- time-bounded
- single-use
- invalidated if relevant state changes
- auditable

The objective is not maximum autonomy. The objective is **useful automation with clear authority boundaries**.
