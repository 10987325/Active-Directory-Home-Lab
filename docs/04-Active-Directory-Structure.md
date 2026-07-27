# Active Directory Structure

## Overview

Active Directory stores and organizes network resources using a logical structure. This structure helps administrators efficiently manage users, computers, groups, and organizational units (OUs).

A well-organized Active Directory environment improves security, simplifies administration, and supports delegation of responsibilities.

---

## Why is Active Directory Organized?

As organizations grow, managing hundreds or thousands of users individually becomes difficult.

Active Directory uses Organizational Units (OUs) and Security Groups to organize resources based on departments, job roles, or business requirements.

This makes administration easier and reduces the risk of human error.

---

## Organizational Units (OUs)

An Organizational Unit (OU) is a logical container used to organize Active Directory objects such as users, computers, and groups.

In this lab, separate OUs were created to represent different departments within an organization.

### Benefits of OUs

- Organize users and computers
- Apply Group Policies (GPOs)
- Delegate administrative permissions
- Simplify Active Directory management

---

## Users

A user account represents an individual who requires access to organizational resources.

Examples created during this lab include:

- HR_Admin
- Sara Ahmed
- Hakim Ali

Each user can be assigned permissions according to their job responsibilities.

---

## Security Groups

Security Groups are used to assign permissions to multiple users at the same time.

Instead of assigning permissions individually, administrators assign permissions to a group and then add users as members.

This approach follows enterprise best practices and simplifies access management.

Example:

- HR_Admins

---

## Screenshots

### Active Directory Users and Computers

<img width="1024" height="768" alt="03-ADUC" src="https://github.com/user-attachments/assets/2e3e4e2d-afa3-4a76-b19a-3231fc901705" />


---

### HR Organizational Unit

<img width="1024" height="768" alt="04-HR-OU" src="https://github.com/user-attachments/assets/700f6d48-5df5-4835-bf13-f1d9fad30f92" />

---

### HR_Admins Security Group

<img width="1024" height="768" alt="05-HR-Admins-Group" src="https://github.com/user-attachments/assets/87acc6e8-4821-454f-93a7-35ef1f1f4334" />

---

## Real-World Example

Imagine a company with separate departments such as Human Resources, Finance, IT, and Sales.

Instead of placing every employee in one location, administrators create separate Organizational Units for each department.

Security Groups are then used to grant department-specific permissions, making administration more secure and easier to manage.

---

## Key Learning

Through this lab, I learned:

- How Organizational Units help organize Active Directory.
- Why Security Groups are preferred over assigning permissions to individual users.
- How users, groups, and OUs work together in an enterprise environment.
- Why a well-structured Active Directory improves security and management.

---

## Skills Demonstrated

- Active Directory Users and Computers (ADUC)
- Organizational Unit (OU) Management
- User Account Management
- Security Group Management
- Enterprise Directory Organization

- 
