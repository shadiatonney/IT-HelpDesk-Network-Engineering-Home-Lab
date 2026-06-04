# DNS and DHCP Configuration Lab

## Overview

This lab demonstrates the configuration and management of DNS (Domain Name System) and DHCP (Dynamic Host Configuration Protocol) services in a Windows Server environment.

DNS and DHCP are essential network services used in enterprise environments to automate IP address allocation and hostname resolution.

---

## Objectives

* Install DNS Server Role
* Install DHCP Server Role
* Create a DNS Forward Lookup Zone
* Configure DHCP Scope
* Configure DHCP Reservations
* Verify Name Resolution
* Test Client IP Assignment

---

## Technologies Used

* Windows Server 2022
* DNS Server
* DHCP Server
* Windows Client
* VirtualBox

---

## Lab Environment

| Device   | IP Address   | Role               |
| -------- | ------------ | ------------------ |
| Server01 | 192.168.1.10 | DNS & DHCP Server  |
| Client01 | Dynamic IP   | Client Workstation |

---

## Implementation Steps

### Step 1: Install DNS Server Role

Installed the DNS Server role using Server Manager.

Verified the DNS service was running successfully.

---

### Step 2: Create Forward Lookup Zone

Created a new Forward Lookup Zone.

Example:

```text
shadialab.local
```

Configured DNS records for network devices and servers.

---

### Step 3: Install DHCP Server Role

Installed the DHCP Server role and completed post-installation configuration.

Authorized the DHCP server within Active Directory.

---

### Step 4: Configure DHCP Scope

Created a DHCP Scope.

Example Configuration:

```text
Scope Name: Office Network

Start IP: 192.168.1.100
End IP: 192.168.1.200

Subnet Mask:
255.255.255.0

Default Gateway:
192.168.1.1

DNS Server:
192.168.1.10
```

---

### Step 5: Configure DHCP Reservation

Created a DHCP Reservation for a client device.

Example:

```text
Device: Printer01

Reserved IP:
192.168.1.50
```

---

### Step 6: Test DHCP Lease

On the client machine:

```cmd
ipconfig /release
ipconfig /renew
```

Verified the client received an IP address from the DHCP scope.

---

### Step 7: Test DNS Resolution

Performed DNS testing using:

```cmd
nslookup server01
ping server01
```

Successfully resolved hostnames and verified network connectivity.

---

## Screenshots

### DNS Server Installation

(Add screenshot)

### Forward Lookup Zone

(Add screenshot)

### DNS Records

(Add screenshot)

### DHCP Scope Configuration

(Add screenshot)

### DHCP Lease Assignment

(Add screenshot)

### DHCP Reservation

(Add screenshot)

### Client IP Configuration

(Add screenshot)

### DNS Testing

(Add screenshot)

---

## Troubleshooting

### Issue

Client computer was unable to resolve hostnames.

### Root Cause

Incorrect DNS server address configured on the client.

### Resolution

Updated the client DNS settings to point to the Windows Server DNS service.

### Outcome

Hostname resolution was successful and network connectivity was restored.

---

## Skills Demonstrated

* DNS Administration
* DHCP Administration
* IP Address Management
* Network Configuration
* Windows Server Administration
* Troubleshooting Network Services
* Client Connectivity Testing

---

## Real-World Application

DNS and DHCP services are critical components of enterprise networks. IT Support and Systems Administration professionals use these services daily to manage network connectivity, troubleshoot client issues, and maintain reliable communication between devices and servers.
