# Workflow State Example

This fictional example illustrates the governance pattern used by the private design. It contains no private repository names, credentials, production endpoints, or real authorization data.

## Example work item

**Task:** update documentation for a low-risk internal feature description.

```text
CREATED
  -> STATE_CAPTURED
  -> CLASSIFIED
  -> RISK_ASSESSED (R1)
  -> PLAN_CREATED
  -> POLICY_AUTHORIZED
  -> BRANCH_CREATED
  -> EXECUTING
  -> REVIEWING
  -> VALIDATING
  -> MERGE_ELIGIBLE
  -> COMPLETED
```

## Example authority decisions

```yaml
risk: R1
reversible: true
production_change: false
secret_access: false
database_migration: false
human_approval_required: false
auto_merge_eligible: only_if_policy_and_validation_pass
```

## Consequential variant

If the same workflow later requested a production deployment:

```yaml
risk: R3
human_approval_required: true
automatic_execution: false
required_evidence:
  - reviewed_commit
  - validation_pass
  - expected_target_unchanged
  - approval_not_expired
```

The key design principle is that an AI agent may propose the next step, but it does not self-authorize a consequential action.