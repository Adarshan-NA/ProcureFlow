# Setup Guide

## Prerequisites

- Microsoft Power Apps
- Microsoft Dataverse
- Power Automate
- SharePoint Online
- Microsoft Teams
- Outlook

---

## Solution Import

1. Open Power Apps Maker Portal.
2. Navigate to Solutions.
3. Import ProcureFlow AI Solution.
4. Publish all customizations.

---

## Configure SharePoint

Create a document library named:

```
ProcureFlowInvoices
```

---

## Configure Environment Variables

Update:

- SharePoint Site URL
- Invoice Library Name

---

## Approval Policies

Create approval policies for each procurement category.

Example:

| Category | Amount Range | Approver           |
|----------|--------------|--------------------|
| IT       | 0–10,000     | Manager            |
| IT       | >10,000      | Manager → Director |

---

## Power Automate

Enable:

- Purchase Request Approval Flow
- Invoice Status Synchronization Flow

---

## Test

Create a purchase request and verify:

- Approval task creation
- Teams approval
- SharePoint folder creation
- Invoice status synchronization