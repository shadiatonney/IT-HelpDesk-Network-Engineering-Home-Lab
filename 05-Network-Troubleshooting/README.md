# Network Troubleshooting Lab

## Overview

This lab demonstrates common network troubleshooting techniques used by IT Support and Help Desk professionals to diagnose and resolve connectivity issues in enterprise environments.

The lab focuses on identifying network problems, analyzing symptoms, determining root causes, and implementing solutions using standard networking tools.

---

## Objectives

* Diagnose network connectivity issues
* Verify TCP/IP configuration
* Test network communication
* Troubleshoot DNS problems
* Troubleshoot DHCP issues
* Identify incorrect gateway settings
* Restore network connectivity

---

## Technologies Used

* Windows 10/11
* Windows Server 2022
* Command Prompt
* DNS
* DHCP
* TCP/IP
* VirtualBox

---

## Troubleshooting Tools

The following tools were used during troubleshooting:

```cmd
ipconfig
ping
tracert
nslookup
arp -a
netstat
```

---

## Scenario 1: No Internet Connectivity

### Problem

User reported that the computer could not access the internet.

### Investigation

Checked network configuration using:

```cmd
ipconfig /all
```

Verified:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server

### Root Cause

Incorrect Default Gateway configuration.

### Resolution

Updated the correct gateway address.

### Result

Internet connectivity restored successfully.

---

## Scenario 2: DNS Resolution Failure

### Problem

User could access websites by IP address but not by hostname.

### Investigation

Performed DNS testing:

```cmd
nslookup google.com
```

### Root Cause

Incorrect DNS server configuration.

### Resolution

Configured the correct DNS server.

### Result

Hostname resolution worked successfully.

---

## Scenario 3: Client Not Receiving IP Address

### Problem

Client computer received an APIPA address:

```text
169.254.x.x
```

### Investigation

Checked DHCP service status and network settings.

### Root Cause

DHCP Server was unavailable.

### Resolution

Restarted DHCP service and renewed lease.

```cmd
ipconfig /release
ipconfig /renew
```

### Result

Client received a valid IP address.

---

## Scenario 4: Unable to Reach Server

### Problem

Client could not connect to the server.

### Investigation

Performed connectivity tests:

```cmd
ping server01
ping 192.168.1.10
```

### Root Cause

Windows Firewall blocked communication.

### Resolution

Updated firewall rules and verified connectivity.

### Result

Successful communication between client and server.

---

## Screenshots

### IP Configuration

(Add screenshot)

### Ping Test

(Add screenshot)

### Traceroute Test

(Add screenshot)

### DNS Troubleshooting

(Add screenshot)

### DHCP Troubleshooting

(Add screenshot)

### Connectivity Restored

(Add screenshot)

---

## Skills Demonstrated

* Network Troubleshooting
* TCP/IP Configuration
* DNS Troubleshooting
* DHCP Troubleshooting
* Connectivity Testing
* Root Cause Analysis
* Problem Resolution
* IT Support Methodology

---

## Real-World Application

Network troubleshooting is one of the most important responsibilities of IT Support and Help Desk professionals. These skills are used daily to diagnose connectivity issues, resolve user-reported incidents, and maintain reliable network operations in enterprise environments.

---

## Lessons Learned

Through this lab, I gained practical experience using troubleshooting methodologies to identify, isolate, and resolve common network issues. Understanding the relationship between DNS, DHCP, TCP/IP, and network infrastructure is essential for effective IT support.
