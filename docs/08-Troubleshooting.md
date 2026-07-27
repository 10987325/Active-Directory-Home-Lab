# Active Directory Troubleshooting

## Overview

Troubleshooting is an essential skill for Identity and Access Management (IAM), System Administration, and Security Operations roles.

During this Active Directory home lab, several configuration and permission issues were encountered and resolved. These challenges provided valuable hands-on experience in diagnosing and correcting common Active Directory problems.

---

# Troubleshooting Scenarios

## 1. DNS Resolution Issue

### Problem

The client computer could not properly locate the Active Directory domain.

### Cause

DNS configuration was incorrect.

### Solution

- Verified DNS Server configuration.
- Confirmed the Domain Controller was acting as the DNS Server.
- Verified name resolution using diagnostic tools.

### Lesson Learned

Active Directory depends heavily on DNS. Incorrect DNS configuration prevents domain services from functioning correctly.

---

## 2. Group Policy Not Applying

### Problem

Expected Group Policy settings were not applied.

### Cause

Possible causes included:

- Missing GPO Link
- Security Filtering
- Inheritance
- Replication delay

### Solution

Executed:

```cmd
gpupdate /force
```

Verified applied policies using:

```cmd
gpresult /r
```

Used the Group Policy Results Wizard for additional verification.

### Lesson Learned

Always verify policy application before assuming the GPO configuration is incorrect.

---

## 3. Delegation of Control Verification

### Problem

The delegated HR administrator initially appeared unable to perform delegated tasks.

### Cause

Testing was performed while logged in as Domain Administrator rather than using the delegated account.

### Solution

Verified delegated permissions using the HR_Admin account and confirmed that delegated permissions applied only within the HR Organizational Unit.

### Lesson Learned

Always test delegated permissions using the delegated user account.

---

## 4. GitHub Documentation Issue

### Problem

Screenshots were not displaying correctly in Markdown.

### Cause

Incorrect folder structure and image paths.

### Solution

- Reorganized repository folders.
- Corrected relative image paths.
- Verified image rendering using GitHub Preview.

### Lesson Learned

Professional documentation requires organized folders and correct relative paths.

---

## Troubleshooting Tools Used

During this project the following tools were used:

- Active Directory Users and Computers (ADUC)
- Group Policy Management Console (GPMC)
- Group Policy Results Wizard
- Group Policy Modeling
- gpupdate /force
- gpresult /r
- Server Manager
- DNS Manager
- Oracle VirtualBox

---

## Key Learning

This project strengthened my ability to:

- Diagnose Active Directory issues.
- Verify Group Policy processing.
- Troubleshoot DNS-related problems.
- Test delegated permissions.
- Document technical issues and their solutions.
- Build structured troubleshooting procedures.

---

## Enterprise Relevance

Troubleshooting is a daily responsibility for Identity and Access Management teams, System Administrators, and Security Operations Center (SOC) analysts. The ability to identify root causes, verify configurations, and resolve issues efficiently helps maintain secure and reliable enterprise environments.
