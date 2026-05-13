# Role and Entitlement Model

## Objective

The objective of this document is to simulate how roles and entitlements are mapped in an IGA environment.

## Key Terms

| Term | Meaning |
|---|---|
| Identity | The user record managed by the IGA platform |
| Role | A business function or job-based access package |
| Entitlement | A specific permission, group, application role, or access right |
| Application | The target system where access is granted |
| Birthright Access | Default access granted automatically based on role or attributes |

## Role Model

| Business Role | Department | Application | Entitlements |
|---|---|---|---|
| HR Specialist | HR | HR Portal | HR_Read, Employee_Profile_View |
| Finance Analyst | Finance | Finance Portal | Finance_Read, Reports_View |
| IT Admin | IT | IT Admin Portal | Admin_Access, User_Admin |
| Contractor | Support | Contractor Portal | Limited_Read |

## Entitlement Risk

| Entitlement | Risk Level | Reason |
|---|---|---|
| HR_Read | Low | Standard HR access |
| Finance_Read | Medium | Access to financial data |
| Reports_View | Medium | Business reporting access |
| Admin_Access | High | Privileged administrative access |
| User_Admin | High | Can manage user access |
| Limited_Read | Low | Restricted contractor access |

## Access Logic

```text
User attributes
→ Business role
→ Application access
→ Entitlements
→ Review and certification
