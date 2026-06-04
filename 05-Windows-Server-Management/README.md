# Windows Server Management Lab

## Overview

This lab demonstrates the deployment, configuration, and administration of a Windows Server environment. The project simulates common system administration tasks performed in enterprise environments, including server installation, network configuration, role management, and system monitoring.

---

## Objectives

* Install Windows Server 2022
* Configure a static IP address
* Rename and configure the server
* Install and manage server roles
* Configure DNS and DHCP services
* Monitor server performance
* Perform basic administrative tasks
* Verify network connectivity

---

## Technologies Used

* Windows Server 2022
* Server Manager
* PowerShell
* DNS
* DHCP
* VirtualBox
* Windows Client

---

## Lab Environment

| Device   | Operating System    | Purpose                                     |
| -------- | ------------------- | ------------------------------------------- |
| Server01 | Windows Server 2022 | Domain Controller / Infrastructure Services |
| Client01 | Windows 10/11       | Testing and Administration                  |

---

## Implementation Steps

### Step 1: Install Windows Server

Installed Windows Server 2022 in a virtual machine and completed the initial setup process.

### Step 2: Configure Server Settings

Configured:

* Server Name
* Time Zone
* Network Settings
* Administrator Password

### Step 3: Configure Static IP Address

Assigned a static IP address to ensure reliable server communication.

Example:

```text
IP Address: 192.168.1.10
Subnet Mask: 255.255.255.0
Default Gateway: 192.168.1.1
DNS Server: 192.168.1.10
```

### Step 4: Install Server Roles

Installed the following server roles:

* Active Directory Domain Services
* DNS Server
* DHCP Server

### Step 5: Verify Network Connectivity

Performed connectivity testing using:

```powershell
ping
ipconfig
nslookup
```

### Step 6: Server Monitoring

Reviewed:

* Event Viewer
* Server Manager Dashboard
* Task Manager Performance Metrics

---

## Screenshots

### Windows Server Installation

(Add screenshot)

### Server Manager Dashboard

(Add screenshot)

### Network Configuration

(Add screenshot)

### Installed Roles

(Add screenshot)

### Event Viewer

(Add screenshot)

### Connectivity Testing

(Add screenshot)

---

## Troubleshooting

### Issue

Client machine could not communicate with the server.

### Root Cause

Incorrect DNS server configuration.

### Resolution

Updated the DNS server settings to point to the Windows Server.

### Outcome

Client successfully communicated with the server and resolved hostnames correctly.

---

## Skills Demonstrated

* Windows Server Administration
* Network Configuration
* DNS Management
* DHCP Management
* Server Monitoring
* Infrastructure Support
* IT Troubleshooting
* System Administration

---

## Real-World Application

Windows Server is widely used in enterprise environments to manage users, devices, network services, and infrastructure. The skills demonstrated in this lab are directly applicable to IT Support Officer, Help Desk Technician, Service Desk Analyst, and Junior Systems Administrator roles.
