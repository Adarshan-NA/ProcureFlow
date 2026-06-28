# ProcureFlow AI – Solution Architecture

## Overview

ProcureFlow AI is an end-to-end Procurement Management System built using Microsoft Power Platform. The solution automates purchase request creation, approval routing, invoice management, and request tracking while providing administrators with a configurable approval engine.

The architecture leverages Microsoft Dataverse as the central data platform, Power Apps for user interfaces, Power Automate for workflow orchestration, and SharePoint for document management.

---

## Solution Architecture

```
                    +----------------------+
                    |  Canvas App          |
                    |  (Requester Portal)  |
                    +----------+-----------+
                               |
                               |
                               ▼
                    +----------------------+
                    |     Dataverse        |
                    | Purchase Requests    |
                    | Categories           |
                    | Line Items           |
                    | Approval Tasks       |
                    | Approval Policies    |
                    | Approval Steps       |
                    +----------+-----------+
                               |
                 +-------------+-------------+
                 |                           |
                 ▼                           ▼
      Power Automate               SharePoint Online
  Approval Workflow Engine        Invoice Repository
                 |                           |
                 ▼                           ▼
      Teams & Outlook             Invoice Status Sync
      Approval Actions                Power Automate
```

---

## Components

### Canvas App

The requester portal allows users to:

- Create purchase requests
- Add multiple line items
- Save drafts
- Submit requests for approval
- Track request and invoice status

---

### Model-Driven App

Provides an administrative interface for:

- Approval Policies
- Approval Steps
- Purchase Requests
- Purchase Request Lines
- Approval Tasks
- Categories

---

### Dataverse

Acts as the centralized data repository storing:

- Purchase Requests
- Purchase Request Lines
- Approval Steps
- Approval Tasks
- Approval Policies
- Categories

---

### Power Automate

Responsible for:

- Dynamic approval routing
- Multi-step approvals
- SharePoint folder creation
- Teams and Outlook approvals
- Request status updates
- Invoice status synchronization

---

### SharePoint

Each purchase request automatically receives a dedicated folder for storing invoices and supporting documentation.

---

## Benefits

- Automated procurement approvals
- Configurable approval policies
- Centralized audit trail
- Real-time request tracking
- Integrated document management