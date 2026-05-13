# Access Request Workflow

## Objective

The objective of this document is to simulate an access request workflow in an IGA environment based on SailPoint concepts.

## Scenario

Daniel Reed works in HR but needs temporary access to the Finance Portal for a reporting project.

Because this access is outside his standard role, it must go through approval.

## Access Request Flow

```text
User submits access request
→ Manager reviews business justification
→ Application owner reviews risk
→ IGA platform provisions access
→ Access is reviewed
→ Access is removed after expiry
```

## Request Details

| Field | Value |
|---|---|
| Requester | Daniel Reed |
| Current Department | HR |
| Requested Application | Finance Portal |
| Requested Entitlement | Finance_Read |
| Access Type | Temporary exception access |
| Duration | 30 days |
| Business Justification | Support finance reporting project |

## Approval Workflow

| Approval Step | Approver | Decision |
|---|---|---|
| Manager Approval | HR Manager | Approved |
| Application Owner Approval | Finance App Owner | Approved |
| Security Review | IAM/Security Team | Approved with expiry |

## Provisioning Action

After approval, the user receives temporary access.

```text
Daniel Reed
→ Temporary Finance Access
→ Finance Portal
→ Finance_Read
```

## Access Control Requirements

- Business justification required
- Manager approval required
- Application owner approval required
- Temporary access only
- Expiry date required
- Access review required before extension
- Access removed after expiry

## Lab Outcome

Simulated an access request workflow showing how exception access should be requested, approved, provisioned, reviewed, and removed. This demonstrates approval-based access governance and least privilege control.
