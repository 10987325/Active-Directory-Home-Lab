# Delegation of Control

## Overview

Delegation of Control allows organizations to assign specific administrative tasks to users or groups without granting full Domain Administrator privileges.

Instead of giving excessive permissions, administrators delegate only the permissions required to perform a specific job. This approach follows the Principle of Least Privilege (PoLP) and reduces security risks.

---

## Why Delegation is Important

In a large organization, many departments require administrative capabilities.

For example:

- Human Resources resets employee passwords.
- Help Desk unlocks user accounts.
- IT Support joins computers to the domain.
- Finance administrators manage finance department users.

Granting Domain Administrator privileges to all these employees would create unnecessary security risks.

Delegation solves this problem by assigning only the permissions required for each role.

---

## Principle of Least Privilege (PoLP)

The Principle of Least Privilege states that users should receive only the permissions necessary to perform their job responsibilities.

Examples:

- HR administrators can reset passwords for HR users.
- Help Desk can unlock user accounts.
- Finance administrators manage Finance users.

They do not receive full control over the Active Directory domain.

---

## Lab Scenario

In this lab:

- An Organizational Unit named **HR** was created.
- A Security Group named **HR_Admins** was created.
- The user **HR_Admin** was added to the HR_Admins group.
- The Delegation of Control Wizard was used.
- The HR_Admins group was delegated the following permissions:

- Reset user passwords
- Force password change at next logon

The delegation applied only to the HR Organizational Unit.

---

## Why Use Security Groups?

Instead of delegating permissions directly to individual users, permissions were assigned to the HR_Admins Security Group.

This approach provides several advantages:

- Easier administration
- Faster onboarding
- Faster offboarding
- Reduced configuration errors
- Better scalability

When a new HR administrator joins, they only need to be added to the HR_Admins group.

---

## Screenshot

### Delegation of Control Wizard

<img width="1024" height="768" alt="09-Delegation-Wizard" src="https://github.com/user-attachments/assets/d31b2f36-2e6e-4ca3-a8d8-9855dc58ee58" />

---

## Real-World Example

Consider a company with 2,000 employees.

The HR department frequently resets passwords for employees.

Instead of making every HR employee a Domain Administrator, the organization delegates password reset permissions only for the HR Organizational Unit.

This limits administrative access while allowing HR staff to perform their daily responsibilities.

---

## Security Benefits

Delegation of Control improves security by:

- Reducing privileged accounts
- Limiting administrative access
- Following the Principle of Least Privilege
- Reducing the impact of compromised accounts
- Simplifying permission management

---

## Key Learning

Through this lab, I learned:

- Why organizations use Delegation of Control.
- How to delegate administrative permissions safely.
- Why Security Groups are preferred over individual user assignments.
- How the Principle of Least Privilege improves security.
- How delegated permissions differ from Domain Administrator privileges.

---

## Enterprise Relevance

Delegation of Control is widely used in enterprise Active Directory environments to distribute administrative responsibilities securely. It allows organizations to maintain strong security while enabling different departments to manage the resources they are responsible for.
