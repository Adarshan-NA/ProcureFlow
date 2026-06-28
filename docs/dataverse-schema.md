# Dataverse Schema

## Category

| Column | Type |
|---------|------|
| Name | Text |
| Code | Text |
| IsActive | Yes/No |

## Purchase Requests

| Column | Type |
|---------|------|
| Request Number | Text |
| Title | Text |
| Category | Lookup |
| Status | Choice |
| Requester Email | Text |
| Total Amount | Currency |
| Current Step | Number |
| Current Approver Email | Text |
| Invoice Folder Link | URL |
| Invoice Status | Choice |

---

## Purchase Request Lines

| Column | Type |
|---------|------|
| Purchase Request | Lookup |
| Line Description | Text |
| Quantity | Number |
| Unit Price | Currency |
| Line Total | Currency |

---

## Approval Policies

| Column | Type |
|---------|------|
| Name | Text |
| Category | Choice |
| Minimum Amount | Currency |
| Maximum Amount | Currency |
| Active | Yes/No |

---

## Approval Steps

| Column | Type |
|---------|------|
| Policy | Lookup |
| Step Order | Number |
| Approver Email | Text |

---

## Approval Tasks

| Column | Type |
|---------|------|
| Purchase Request | Lookup |
| Approval Step | Lookup |
| Approver Email | Text |
| Decision | Choice |
| Decision Date | Date |
| Decision Notes | Multiline Text |