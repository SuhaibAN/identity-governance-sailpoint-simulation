# IGA Flow Diagram

```mermaid
flowchart TD
    A[HR System / Source of Truth] --> B[Identity Source]
    B --> C[Identity Profile]
    C --> D[Business Role Assignment]
    D --> E[Entitlement Mapping]
    E --> F[Provisioning to Applications]

    F --> G[HR Portal]
    F --> H[Finance Portal]
    F --> I[IT Admin Portal]
    F --> J[Contractor Portal]

    K[Access Request] --> L[Manager Approval]
    L --> M[Application Owner Approval]
    M --> N[Security / IAM Review]
    N --> F

    O[Quarterly Access Review] --> P[Reviewer Decision]
    P --> Q{Keep or Revoke?}
    Q -->|Keep| R[Access Retained]
    Q -->|Revoke| S[Remove Entitlement]

    T[Leaver Event] --> U[Disable Identity]
    U --> V[Revoke Access]
    V --> W[Close Remediation Item]
```

## Summary

This diagram shows a simulated IGA workflow:

- HR system provides identity data
- Identity profile drives role assignment
- Roles map to application entitlements
- Access requests require approval
- Access reviews validate continued need
- Revocation removes unnecessary or expired access
