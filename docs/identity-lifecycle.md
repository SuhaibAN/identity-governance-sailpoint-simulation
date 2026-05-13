# Identity Lifecycle

## Objective

The objective of this document is to simulate identity lifecycle management in an IGA environment based on SailPoint concepts.

## Lifecycle Flow

```text
HR System
→ Identity Source
→ Identity Profile
→ Role Assignment
→ Entitlement Assignment
→ Provisioning
→ Access Review
→ Revocation
```

## Source of Truth

In a real IGA environment, the HR system is usually the source of truth for workforce identity data.

Example HR systems:

- Workday
- SAP SuccessFactors
- Oracle HCM

The HR system provides attributes such as:

- First name
- Last name
- Employee ID
- Department
- Job title
- Manager
- Employment type
- Start date
- Termination date

## Joiner Scenario

A new employee joins the company.

Example:

| Attribute | Value |
|---|---|
| Name | Daniel Reed |
| Department | Finance |
| Job Title | Finance Analyst |
| Manager | Sarah Miller |
| Employment Type | Full-time |

Expected IGA action:

```text
Create identity
Assign Finance role
Grant finance-related entitlements
Trigger approval if access is sensitive
```

## Mover Scenario

An employee changes department or role.

Example:

```text
Daniel Reed moves from Finance to HR
```

Expected IGA action:

```text
Remove Finance role
Revoke Finance entitlements
Assign HR role
Grant HR entitlements
Trigger review for any retained access
```

## Leaver Scenario

An employee leaves the company.

Expected IGA action:

```text
Disable identity
Remove application access
Revoke entitlements
Terminate sessions
Trigger manager review for ownership transfer
```

## Lab Outcome

Simulated the identity lifecycle process using HR-driven user attributes, role changes, entitlement assignment, and offboarding logic. This demonstrates how IGA platforms manage access across joiner, mover, and leaver events.
