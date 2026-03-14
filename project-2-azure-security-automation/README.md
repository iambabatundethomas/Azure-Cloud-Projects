Azure Project 2 – Network Security & Automated Cost Control
Project Overview
This project focuses on securing cloud infrastructure using Network Security Groups (NSGs) and implementing a serverless "Kill Switch" using Azure Logic Apps.
The goal was twofold:
Security: Ensure the Virtual Machines are only accessible via secure ports (RDP/SSH) while blocking all other traffic.
Governance: Prevent unexpected billing by automatically deallocating all VMs once a specific budget threshold (£2) is reached.
Architecture & Components
Network Security Group (NSG): Acting as a virtual firewall for the subnet.
Inbound Security Rules:
Port 3389 (RDP): Allowed for Windows VM access.
Port 22 (SSH): Allowed for Linux VM access.
Deny All: A "Least Privilege" rule to block unauthorized traffic.
Azure Logic App: A serverless workflow triggered by an HTTP request from a Budget Alert.
Managed Identity: Used for secure, password-less authentication between the Logic App and Azure resources.
Azure Budget Alert: Set at a £2 threshold to trigger the automated shutdown.
Key Steps Taken
Part 1: Securing the Network (NSG)
Created a Network Security Group (NSG) and associated it with the VM's subnet.
Defined Inbound Rules: Configured high-priority rules to allow RDP and SSH traffic from specific IP addresses.
Hardened the Environment: Verified that all other non-essential ports were blocked to reduce the attack surface.
Part 2: The Automated "Kill Switch" (Logic App)
Enabled Managed Identity: Provided the Logic App with its own identity to bypass authentication errors.
Role Assignments (IAM): Granted the Logic App Virtual Machine Contributor permissions to the target VMs.
Built the Workflow: Designed a Logic App to deallocate multiple VMs sequentially upon receiving an alert.
Linked to Budget: Created a £2 budget alert that triggers an Action Group, which in turn calls the Logic App.
Skills Learned
Network Security: Understanding Inbound vs. Outbound rules and rule priority.
Least Privilege Access: Only opening necessary ports to maintain a secure posture.
Cloud Governance: Using automation to manage cloud spend and prevent "bill shock."
Serverless Automation: Working with Azure Logic Apps and HTTP triggers.
Identity Management: Implementing System-Assigned Managed Identities for secure resource communication.
