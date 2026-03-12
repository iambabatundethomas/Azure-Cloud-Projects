# Azure Project 1 – Deploying Windows and Linux Virtual Machines

## Project Overview

This project demonstrates the deployment of cloud infrastructure in Microsoft Azure, including Windows and Linux virtual machines communicating inside a private virtual network.

The goal of this lab was to understand Azure infrastructure fundamentals including networking, VM deployment, remote access, and cost control.

---

## Architecture

Resources created in Azure:

- Resource Group
- Virtual Network (VNet)
- Subnet
- Windows Virtual Machine
- Ubuntu Linux Virtual Machine
- Network Interfaces
- Public IP Addresses

Both virtual machines were deployed inside the same Virtual Network to allow private communication.

---

## Deployment Steps

### 1. Resource Group Creation

Created a resource group to organize all infrastructure resources.

### 2. Virtual Network Deployment

Configured:

- Address space
- Subnet
- Private network communication

### 3. Windows Virtual Machine Deployment

A Windows Server VM was deployed and accessed using:

RDP (Remote Desktop Protocol)

---

### 4. Linux Virtual Machine Deployment

An Ubuntu Server VM was deployed and accessed using:

SSH via PowerShell

---

### 5. Private Network Communication Test

The Windows VM successfully pinged the private IP address of the Linux VM, confirming internal VNet communication.

---

### 6. Internet Connectivity Test

Inside the Linux VM the following command confirmed internet access:

```
ping google.com
```

---

### 7. Linux Network Inspection

Checked the private IP configuration using:

```
ip a
```

---

### 8. Cost Management Configuration

Implemented cost monitoring using:

- Azure Budget (£6 limit)
- Logic App automation to automatically shut down VMs

---

## Skills Demonstrated

- Azure Virtual Machine deployment
- Azure Virtual Networking
- Linux command-line basics
- SSH remote server access
- Windows RDP administration
- Private IP communication
- Azure cost management
- Cloud infrastructure organisation

---

## What I Learned

This project helped reinforce:

- Azure resource architecture
- Virtual networking concepts
- Remote server administration
- Cloud cost control strategies
- Linux network commands

---

## Next Project

Secure a Virtual Machine with Network Security Groups
