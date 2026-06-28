# Power Automate Flows

## 1. Purchase Request Approval Engine

### Purpose

Automates the procurement approval lifecycle.

### Workflow

1. Purchase Request Submitted
2. Determine Approval Policy
3. Retrieve Approval Steps
4. Create Approval Task
5. Create SharePoint Invoice Folder
6. Send Teams & Outlook Approval
7. Process Decision
8. Route to Next Step (if applicable)
9. Update Purchase Request Status
10. Notify Requester

---

## Features

- Dynamic policy routing
- Multi-step approvals
- Teams integration
- Outlook integration
- Approval audit trail

---

## 2. Invoice Status Synchronization

### Purpose

Updates invoice status after documents are uploaded.

### Workflow

1. Detect file upload
2. Identify request folder
3. Retrieve Purchase Request
4. Update Invoice Status

---

## Notifications

Requester receives notifications for:

- Submission
- Approval
- Rejection

Approvers receive:

- Teams Approval Card
- Outlook Approval Email