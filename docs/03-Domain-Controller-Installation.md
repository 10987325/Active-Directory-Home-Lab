# Domain Controller Installation

## Overview

The first step in building an Active Directory environment is installing a Windows Server and promoting it to a Domain Controller.

A Domain Controller (DC) is the central server responsible for authenticating users, managing computer accounts, enforcing Group Policies, and maintaining the Active Directory database.

Without a Domain Controller, Active Directory cannot function.

---

## Lab Configuration

| Component | Value |
|-----------|-------|
| Operating System | Windows Server 2022 |
| Server Role | Domain Controller |
| Domain Name | corp.local |
| Services Installed | Active Directory Domain Services (AD DS), DNS |

---

## Installation Process

The following steps were completed during the lab:

1. Installed Windows Server 2022.
2. Opened **Server Manager**.
3. Added the **Active Directory Domain Services (AD DS)** role.
4. Installed the **DNS Server** role.
5. Promoted the server to a Domain Controller.
6. Created a new forest named **corp.local**.
7. Restarted the server to complete the installation.
8. Verified that Active Directory was successfully installed.

---

## Why is a Domain Controller Important?

A Domain Controller provides centralized identity and access management for an organization.

Instead of creating separate user accounts on every computer, administrators can manage all users, groups, passwords, and security policies from one central location.

This improves security, simplifies administration, and supports enterprise-scale environments.

---

## Screenshot

The following screenshot shows the Windows Server environment used to install and manage Active Directory.

<img width="1024" height="768" alt="02-Server-Manager" src="https://github.com/user-attachments/assets/f538072d-d698-4bd9-b56d-6001c16adaed" />


---

## Key Learning

Through this lab, I learned:

- The role of a Domain Controller in an enterprise environment.
- How to install Active Directory Domain Services (AD DS).
- How to promote a Windows Server to a Domain Controller.
- Why DNS is required for Active Directory.
- How centralized identity management improves security and administration.
