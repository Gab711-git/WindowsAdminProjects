# 🖥️ Windows Server Administration Homelab

A hands-on Windows Server homelab built using Oracle VirtualBox to demonstrate practical system administration skills. This project simulates a small enterprise environment where a Windows Server acts as the Domain Controller, managing users, computers, policies, and network services through Active Directory.

The purpose of this lab is to develop and showcase real-world Windows Server administration skills commonly used by System Administrators, IT Support Engineers, and Infrastructure Engineers.

---

#Objectives

* Deploy a Windows Server virtual machine
* Configure Active Directory Domain Services (AD DS)
* Create and manage users and groups
* Implement Identity and Access Management (IAM)
* Configure Organizational Units (OUs)
* Manage passwords and account policies
* Configure Group Policy Objects (GPO)
* Join Windows clients to the domain
* Configure DNS and DHCP
* Manage shared folders and NTFS permissions
* Automate administrative tasks using PowerShell
* Document every stage of the deployment

---

#Lab Environment

| Component         | Technology                                                           |
| ----------------- | -------------------------------------------------------------------- |
| Virtualization    | Oracle VirtualBox                                                    |
| Server OS         | Windows Server 2025 Evaluation
| Client OS         | Windows 11 Enterprise Evaluation                                     |
| Domain            | InfiniteVoid.local                                                       |
| Domain Controller | DC01                                                                 |
| Client Computers  | PC01, PC02                                                           |
| Scripting         | PowerShell                                                           |
| Documentation     | Markdown                                                             |

---

#Repository Structure

```text
Windows-Server-Lab/

│
├── ISO/
│      Windows_Server.iso
│      Windows11.iso
│
├── Screenshots/
│
├── PowerShell/
│
├── Documentation/
│
└── README.md
```

---

#Enterprise Scenario

This lab simulates a fictional company named **InfiniteVoid Ltd.**

Departments include:

* Human Resources
* Finance
* IT
* Sales

The Windows Server infrastructure is responsible for managing users, computers, authentication, permissions, security policies, and network services for the organization.

---

#Lab Roadmap

#Phase 1

* Install Windows Server
* Initial server configuration

#Phase 2

* Install Active Directory Domain Services
* Promote server to Domain Controller

#Phase 3

* Configure DNS
* Create the `InfiniteVoid.local` domain

#Phase 4

* Create Organizational Units (OUs)

#Phase 5

* Create users
* Create security groups
* Configure Identity and Access Management (IAM)

#Phase 6

* Join Windows 11 clients to the domain

#Phase 7

* Configure Group Policy Objects (GPO)

Examples include:

* Password Policy
* Desktop Wallpaper
* Disable Control Panel
* Disable USB Storage
* Disable Command Prompt
* Account Lockout Policy

#Phase 8

* Configure shared folders
* Configure NTFS permissions

#Phase 9

* Install and configure DHCP

#Phase 10

* Configure DNS records

#Phase 11

* PowerShell administration

Examples include:

* Create users
* Reset passwords
* Disable accounts
* Enable accounts
* Retrieve Active Directory users

#Phase 12

* Event Viewer
* Administrative tools
* Backup and recovery

---

#Skills Demonstrated

* Windows Server Administration
* Active Directory
* Active Directory Users and Computers (ADUC)
* Active Directory Domain Services (AD DS)
* Identity and Access Management (IAM)
* Group Policy Management
* DNS Administration
* DHCP Administration
* Organizational Unit Management
* User & Group Administration
* Windows Authentication
* NTFS Permissions
* File Server Administration
* Remote Desktop Services
* PowerShell Scripting
* Windows Networking
* Virtualization
* System Documentation

---

#Documentation

Screenshots of every completed lab are stored inside the **Screenshots** directory.

Each major configuration step is documented in the **Documentation** folder with explanations and implementation details.

---

#PowerShell

Automation scripts are stored in the **PowerShell** directory.

Examples include:

* User creation
* Password reset
* Account management
* Active Directory queries
* Administrative automation

---

#Learning Goals

This project is designed to strengthen practical knowledge of enterprise Windows Server administration by simulating common responsibilities performed by system administrators in production environments.

The project emphasizes both graphical administration tools and PowerShell automation while following industry best practices for documentation and organization.

---

#Future Improvements

* Windows Deployment Services (WDS)
* WSUS
* DFS Namespace
* DFS Replication
* Certificate Services (AD CS)
* Print Server
* File Server Resource Manager
* Failover Clustering
* Hyper-V
* Azure AD / Microsoft Entra ID integration
* Microsoft Intune integration
* Monitoring and logging

---

#License

This repository is intended for educational and portfolio purposes only.
