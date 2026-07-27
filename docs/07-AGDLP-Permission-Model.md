# AGDLP Permission Model

## Overview

AGDLP is a Microsoft-recommended best practice for assigning permissions in an Active Directory environment.

Instead of assigning permissions directly to individual users, AGDLP organizes access through groups. This approach simplifies administration, improves security, and reduces configuration errors.

AGDLP stands for:

- **A** – Accounts
- **G** – Global Groups
- **DL** – Domain Local Groups
- **P** – Permissions

---

## Why Organizations Use AGDLP

In large organizations, hundreds or thousands of employees require access to shared resources.

Assigning permissions directly to each user would be:

- Time-consuming
- Difficult to manage
- More likely to result in configuration errors

AGDLP provides a structured method for managing permissions efficiently.

---

## Understanding Each Component

### Accounts (A)

Accounts represent individual users.

Examples:

- Sara Ahmed
- Hakim Ali
- HR_Admin

Users are never assigned permissions directly.

Instead, they become members of Global Groups.

---

### Global Groups (G)

Global Groups organize users who have similar job roles.

Examples:

- HR_Admins
- Finance_Admins
- IT_Admins

Global Groups make it easier to manage users within a department.

---

### Domain Local Groups (DL)

Domain Local Groups represent access to a specific resource.

Examples:

- HR Shared Folder Access
- Finance Shared Folder Access
- IT File Server Access

Permissions are assigned to Domain Local Groups rather than directly to users.

---

### Permissions (P)

Permissions define what actions users can perform on a resource.

Examples:

- Read
- Write
- Modify
- Full Control

Permissions are granted to the Domain Local Group.

---

## AGDLP Workflow

The permission assignment process follows this sequence:

```
User Account
      │
      ▼
Global Group
      │
      ▼
Domain Local Group
      │
      ▼
Shared Resource
```

Example:

Sara Ahmed

↓

HR_Admins (Global Group)

↓

HR_Share_RW (Domain Local Group)

↓

HR Shared Folder (Modify Permission)

---

## Why AGDLP is Better

Instead of changing permissions every time an employee joins or leaves a department:

- Add new employees to the Global Group.
- Remove departing employees from the Global Group.

No changes are required on the shared folder permissions.

This reduces administrative effort and improves consistency.

---

## Real-World Example

A new Finance Administrator joins the company.

Instead of assigning permissions directly:

1. Add the user to the Finance_Admins Global Group.
2. Finance_Admins is already a member of Finance_Share_RW.
3. Finance_Share_RW already has Modify permission on the Finance Shared Folder.

The new employee immediately receives the correct access without changing folder permissions.

---

## Security Benefits

AGDLP provides:

- Simplified administration
- Reduced human error
- Better scalability
- Role-Based Access Control (RBAC)
- Easier auditing
- Stronger security management

---

## Key Learning

During this lab I learned:

- The meaning of AGDLP.
- Why Microsoft recommends AGDLP.
- How Global Groups simplify user management.
- Why permissions should be assigned through Domain Local Groups.
- How AGDLP improves enterprise security and scalability.

---

## Enterprise Relevance

AGDLP is widely used in enterprise Active Directory environments because it separates user management from resource permissions. This approach supports scalable identity and access management while reducing administrative complexity and security risks.
