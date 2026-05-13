# Access Review Certification

## Objective

The objective of this document is to simulate an access review certification process in an IGA environment.

## Scenario

A quarterly access review is performed to validate whether users still need their current access.

Managers and application owners review access and decide whether to keep, revoke, or modify access.

## Access Review Matrix

| User | Department | Application | Entitlement | Risk Level | Reviewer | Decision |
|---|---|---|---|---|---|---|
| Omar Hassan | HR | HR Portal | HR_Read | Low | HR Manager | Keep |
| Sarah Miller | Finance | Finance Portal | Finance_Read | Medium | Finance Manager | Keep |
| Alex Chen | IT | IT Admin Portal | Admin_Access | High | IT Manager | Keep with review |
| Mark Wilson | Contractor | Contractor Portal | Limited_Read | Medium | App Owner | Remove at contract end |
| Daniel Reed | HR | Finance Portal | Finance_Read | Medium | Finance App Owner | Revoke after expiry |

## Review Decisions

| Decision | Meaning |
|---|---|
| Keep | Access is still required |
| Revoke | Access is no longer required |
| Modify | Access should be changed |
| Escalate | Reviewer needs more information |

## High-Risk Access

Privileged access should receive stricter review.

Example:

```text
Alex Chen → IT Admin Portal → Admin_Access
```

Required controls:

- Manager approval
- Application owner approval
- MFA enforcement
- Quarterly review
- Justification required

## Contractor Access

Contractor access should be time-bound.

Example:

```text
Mark Wilson → Contractor Portal → Limited_Read
```

Required controls:

- Contract end date
- Limited entitlement
- Regular review
- Automatic removal after contract ends

## Remediation

If access is rejected during review, the IGA team should create a remediation action.

Example:

```text
Reviewer decision = Revoke
→ Remove entitlement
→ Validate removal
→ Close review item
```

## Lab Outcome

Simulated an access review certification process covering standard users, privileged users, contractors, and temporary exception access. This demonstrates how IGA platforms support compliance, least privilege, and periodic access validation.
