# Revocation Process

## Objective

The objective of this document is to simulate how access revocation works after an access review, termination, or access expiry event.

## Revocation Triggers

Access can be revoked because of:

- Employee termination
- Department transfer
- Contract end date
- Failed access review
- Expired temporary access
- Policy violation
- Manager or app owner decision

## Revocation Flow

```text
Revocation trigger
→ Identify access to remove
→ Remove role or entitlement
→ Disable account if needed
→ Validate removal
→ Document remediation
→ Close ticket/review item
```

## Example 1: Temporary Access Expiry

Daniel Reed had temporary access to the Finance Portal for 30 days.

After expiry:

```text
Remove Finance_Read entitlement
Remove temporary Finance access
Validate Finance Portal access is removed
```

## Example 2: Leaver Offboarding

Daniel Reed leaves the company.

Expected action:

```text
Disable identity
Remove all active entitlements
Revoke application access
Terminate active sessions
Document completion
```

## Example 3: Access Review Revocation

Reviewer decision:

```text
Revoke Finance_Read
```

Remediation action:

```text
Remove entitlement
Confirm removal
Close access review item
```

## Revocation Validation

After revocation, the IAM/IGA team should validate:

- User can no longer access the application
- Entitlement was removed
- Group membership was removed if applicable
- Review item or ticket was closed
- Audit trail is retained

## Lab Outcome

Simulated access revocation scenarios for temporary access expiry, leaver offboarding, and access review remediation. This demonstrates how IGA processes enforce least privilege and reduce standing access risk.
