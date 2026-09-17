# Specialist Agent Contract Example

A governed agent should receive a bounded contract rather than broad permission to "do whatever is needed."

## Example contract

```yaml
agent_role: development_specialist
objective: implement one bounded, approved change
allowed_scope:
  - approved_branch
  - approved_files
  - approved_tests
forbidden:
  - production_deploy
  - secret_changes
  - database_migration
  - permission_expansion
  - protected_reference_changes
  - self_approval
required_outputs:
  - implementation_summary
  - changed_files
  - tests_run
  - residual_risks
  - handoff_for_independent_review
```

## Separation of duties

The development specialist does not decide that its own work is safe to merge. A separate review/QA capability evaluates:

- scope compliance;
- correctness;
- security and privacy implications;
- regression risk;
- test adequacy;
- merge eligibility.

## Why contracts matter

This architecture treats model output as a proposal inside a larger software-control system. Deterministic policy, scoped credentials, independent review, and explicit state transitions limit what any individual agent can do.