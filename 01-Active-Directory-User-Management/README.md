# Active Directory User Management Lab

## Overview

This lab demonstrates the deployment and management of Active Directory in a Windows Server environment.

The lab simulates a real-world business environment where users, groups, and computers are centrally managed through Active Directory Domain Services (AD DS).

---

## Objectives

- Install Active Directory Domain Services
- Configure a Domain Controller
- Create Organizational Units (OUs)
- Create User Accounts
- Create Security Groups
- Join Client Computers to the Domain
- Test Domain Authentication

---

## Technologies Used

- Windows Server 2022
- Active Directory Domain Services (AD DS)
- DNS
- Windows 10/11 Client
- VirtualBox

---

## Network Information

| Device | IP Address |
|----------|----------|
| Domain Controller | 192.168.1.10 |
| Client PC | 192.168.1.20 |

---

## Lab Steps

### Step 1: Install Windows Server

Installed Windows Server 2022 and configured a static IP address.

### Step 2: Install Active Directory Domain Services

Installed the AD DS role using Server Manager.

### Step 3: Promote Server to Domain Controller

Created a new domain:

```text
shadialab.local
```

### Step 4: Create Organizational Units

Created the following OUs:

```text
IT
HR
Finance
Computers
```

### Step 5: Create Users

Created test user accounts for the organisation.

### Step 6: Create Security Groups

Created security groups to manage access permissions.

### Step 7: Join Client Computer to Domain

Joined a Windows client machine to the domain.

### Step 8: Verify Login

Successfully logged in using a domain user account.

---

## Screenshots

### Domain Controller

(Add screenshot here)

### Active Directory Users and Computers

(Add screenshot here)

### Organisational Units

(Add screenshot here)

### Security Groups

(Add screenshot here)

### Client Joined to Domain

(Add screenshot here)

---

## Skills Demonstrated

- Active Directory Administration
- User Account Management
- Group Management
- DNS Configuration
- Domain Joining
- Windows Server Administration
- IT Support Troubleshooting

---

## Real World Application

Active Directory is widely used in enterprise environments. These skills are commonly required for IT Support Officer, Service Desk Analyst, and Help Desk Technician roles.
