# File Server Administration Lab

## Overview

This lab demonstrates the deployment and management of a Windows File Server in an enterprise environment. The project focuses on creating shared folders, configuring NTFS permissions, managing access control, and testing file sharing between users and departments.

File servers are commonly used in organizations to centralize data storage, improve collaboration, and control access to business resources.

---

## Objectives

* Configure a Windows File Server
* Create shared folders
* Configure NTFS permissions
* Configure Share permissions
* Create department-based access controls
* Test user access
* Troubleshoot file access issues

---

## Technologies Used

* Windows Server 2022
* Active Directory
* NTFS Permissions
* Shared Folders
* Windows Client
* VirtualBox

---

## Lab Environment

| Device           | Purpose             |
| ---------------- | ------------------- |
| Server01         | File Server         |
| Client01         | User Workstation    |
| Active Directory | User Authentication |

---

## Implementation Steps

### Step 1: Create Shared Folders

Created departmental folders:

```text
Finance
HR
IT
Public
```

Folder structure:

```text
D:\CompanyData\
├── Finance
├── HR
├── IT
└── Public
```

---

### Step 2: Create Security Groups

Created Active Directory security groups:

```text
Finance_Users
HR_Users
IT_Users
```

Assigned users to the appropriate groups.

---

### Step 3: Configure Share Permissions

Configured share permissions:

| Group         | Permission   |
| ------------- | ------------ |
| Finance_Users | Full Control |
| HR_Users      | Full Control |
| IT_Users      | Full Control |
| Everyone      | Read         |

---

### Step 4: Configure NTFS Permissions

Configured folder-level NTFS permissions to ensure only authorized users could access their department folders.

Example:

```text
Finance Folder
- Finance_Users → Modify
- Administrators → Full Control
```

---

### Step 5: Map Network Drives

Mapped shared folders to client computers.

Example:

```text
\\Server01\Finance
\\Server01\HR
\\Server01\IT
```

---

### Step 6: Test User Access

Logged in using different user accounts and verified access permissions.

Verified:

* Authorized users could access their department folders.
* Unauthorized users received access denied messages.

---

## Screenshots

### Shared Folder Configuration

(Add screenshot)

### Share Permissions

(Add screenshot)

### NTFS Permissions

(Add screenshot)

### Security Groups

(Add screenshot)

### Network Drive Mapping

(Add screenshot)

### Access Testing

(Add screenshot)

---

## Troubleshooting

### Issue

User could not access the Finance shared folder.

### Investigation

Verified:

* Group membership
* Share permissions
* NTFS permissions

### Root Cause

User was not a member of the Finance security group.

### Resolution

Added the user to the correct Active Directory group.

### Outcome

User successfully accessed the Finance folder.

---

## Skills Demonstrated

* File Server Administration
* NTFS Permission Management
* Share Permission Configuration
* Active Directory Integration
* Access Control Management
* Network Drive Mapping
* Troubleshooting User Access Issues

---

## Real-World Application

File servers are widely used in enterprise environments to store and manage organizational data securely. IT Support and System Administrators regularly configure file shares, manage permissions, and troubleshoot access issues to ensure users have the correct level of access to business resources.

---

## Lessons Learned

This lab provided practical experience in managing shared resources and implementing access controls. Understanding the interaction between NTFS permissions, share permissions, and Active Directory groups is essential for maintaining secure and efficient file server environments.
