# Group Policy Management

## Overview

Group Policy is one of the most powerful features of Microsoft Active Directory. It enables administrators to centrally manage and enforce security settings, user configurations, and computer configurations across an entire organization.

Instead of configuring every computer individually, administrators create a Group Policy Object (GPO) once and apply it to the required users or computers. This saves time, reduces administrative effort, and ensures consistent security throughout the enterprise.

---

## Why Organizations Use Group Policy

Imagine an organization with 1,000 employees.

Without Group Policy:

- Every computer must be configured manually.
- Security settings may differ from one computer to another.
- Password policies become difficult to enforce.
- Software deployment takes significant time.

With Group Policy:

- Administrators configure settings once.
- Policies are automatically applied.
- Security remains consistent.
- Administration becomes faster and more reliable.

---

## What is a Group Policy Object (GPO)?

A Group Policy Object (GPO) is a collection of rules and configuration settings that control how users and computers behave in an Active Directory environment.

Examples include:

- Password policies
- Windows Firewall settings
- Desktop wallpaper
- USB device restrictions
- Windows Update settings
- Software deployment
- Login scripts

---

## Computer Configuration vs User Configuration

Every GPO contains two main sections.

### Computer Configuration

Computer Configuration applies settings to the computer regardless of who signs in.

Examples include:

- Windows Firewall
- BitLocker
- Windows Update
- Security Options
- Startup Scripts

These settings are processed when the computer starts.

---

### User Configuration

User Configuration applies settings to the user account after the user signs in.

Examples include:

- Desktop wallpaper
- Control Panel restrictions
- Start Menu settings
- Logon scripts
- Folder Redirection

These settings follow the user account.

---

## Real-World Example

Consider a school environment.

Computer Configuration:

- Every computer in the computer lab has the Windows Firewall enabled.
- USB storage devices are blocked.
- Windows Update is configured automatically.

User Configuration:

- Students receive a standard desktop wallpaper.
- The Control Panel is hidden.
- Command Prompt is disabled.

Regardless of which student logs in, the computer settings remain the same, while the user settings apply specifically to the student account.

---

## Applying Policies Immediately

Normally, Group Policy updates automatically every 90–120 minutes on domain-joined computers.

Administrators can force an immediate update by running:

```cmd
gpupdate /force
```

This command refreshes both Computer Configuration and User Configuration without waiting for the automatic refresh interval.

---

## Why Use gpupdate /force?

Administrators commonly use this command after:

- Creating a new GPO
- Modifying an existing GPO
- Troubleshooting policy issues
- Testing new security settings

It ensures the latest policies are applied immediately.

---

## Screenshot

### Group Policy Management Console

<img width="1024" height="768" alt="06-GPO- Management" src="https://github.com/user-attachments/assets/ecc906b4-e5f8-4103-b061-ece4d45c6cea" />

---

## Key Learning

During this lab I learned:

- The purpose of Group Policy in enterprise environments.
- The difference between Computer Configuration and User Configuration.
- How GPOs simplify centralized administration.
- When and why to use `gpupdate /force`.
- How centralized policy management improves security and consistency.

---

## Enterprise Relevance

Group Policy is a core technology in enterprise Windows environments. Organizations rely on it to enforce security standards, maintain compliance, reduce administrative effort, and ensure consistent configurations across thousands of devices.

---

# Linking Group Policy Objects (GPOs)

Creating a Group Policy Object (GPO) does not automatically apply it to users or computers.

A GPO must be linked to an Active Directory container such as a Domain, Organizational Unit (OU), or Site before it becomes effective.

Without a link, the GPO exists but has no impact on the environment.

---

## Where Can a GPO Be Linked?

A Group Policy Object can be linked to:

- Site
- Domain
- Organizational Unit (OU)

The scope of the link determines which users and computers receive the policy.

---

## Domain-Level Link

When a GPO is linked to the domain, every Organizational Unit under that domain inherits the policy unless inheritance is blocked or a conflicting policy exists.

Example:

A Password Policy linked to the domain applies to all users within the Active Directory domain.

---

## Organizational Unit (OU) Link

When a GPO is linked directly to an Organizational Unit, only the users and computers within that OU receive the policy.

Example:

An HR Desktop Wallpaper policy linked to the HR OU applies only to HR users.

---

## Security Filtering

Sometimes administrators do not want every object inside an Organizational Unit to receive the same policy.

Security Filtering allows administrators to apply a GPO only to specific users or security groups.

This provides more granular control without changing the Organizational Unit structure.

Example:

A USB Restriction GPO is linked to the HR OU.

Instead of applying it to every employee, Security Filtering is configured so that only the HR_Admins security group receives the policy.

---

## Real-World Example

Imagine a company with three departments:

- Human Resources
- Finance
- Information Technology

The HR department requires a custom desktop wallpaper.

Rather than applying the wallpaper across the entire organization, the administrator links the GPO only to the HR Organizational Unit.

If only HR managers require an additional restriction, Security Filtering can target the HR_Admins security group while leaving other HR employees unaffected.

---

## Screenshot

### Linked Group Policy Object

<img width="1024" height="768" alt="08-GPO-Linked" src="https://github.com/user-attachments/assets/74a17d93-d0c9-4d0b-9ff3-3d38acd1addf" />

---

## Key Learning

During this lab I learned:

- Creating a GPO does not apply it automatically.
- A GPO must be linked before it becomes effective.
- GPOs can be linked to Sites, Domains, or Organizational Units.
- Security Filtering allows policies to target specific users or security groups.
- Proper GPO linking reduces administrative effort and improves policy management.

---

## Enterprise Relevance

Large organizations often manage hundreds of Group Policy Objects. Proper linking and Security Filtering ensure that policies are applied only where required, reducing security risks and preventing unintended configuration changes.
