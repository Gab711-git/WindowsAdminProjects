# 🖥️ Windows Server Administration Homelab

A hands-on Windows Server homelab built using Oracle VirtualBox to demonstrate practical Windows Server administration skills in a simulated enterprise environment.

The lab consists of a Windows Server acting as a Domain Controller and a Windows 11 client joined to the domain. The project focuses on core administrative tasks commonly performed by System Administrators, IT Support Engineers, and Infrastructure Engineers.

All software used in this project is freely available through Microsoft Evaluation editions and Oracle VirtualBox.

---

# Objectives

* Deploy Windows Server in a virtual environment
* Configure Active Directory Domain Services (AD DS)
* Promote the server to a Domain Controller
* Create and manage Organizational Units (OUs)
* Create and manage domain users and security groups
* Implement Identity and Access Management (IAM)
* Configure DNS
* Join a Windows 11 client to the domain
* Configure Group Policy Objects (GPO)
* Create shared folders and configure NTFS permissions
* Automate administrative tasks with PowerShell
* Document each stage of the deployment

---

# Lab Environment

| Component         | Technology                       |
| ----------------- | -------------------------------- |
| Virtualization    | Oracle VirtualBox                |
| Server OS         | Windows Server 2025 Evaluation   |
| Client OS         | Windows 11 Enterprise Evaluation |
| Domain            | InfiniteVoid.local               |
| Domain Controller | DC01                             |
| Client            | PC01                             |
| Scripting         | PowerShell                       |
| Documentation     | Markdown                         |

---

# Repository Structure

```text
Windows-Server-Lab/

├── Documentation/
├── PowerShell/
├── Screenshots/
└── README.md
```

> **Note:** Windows installation ISOs are **not included** in this repository because of Microsoft's licensing restrictions.

---

# Project Roadmap

## Phase 1 – Windows Server Installation

* Install Windows Server
* Configure networking
* Rename the server
* Verify connectivity

---

## Phase 2 – Active Directory

* Install Active Directory Domain Services
* Promote the server to Domain Controller
* Create the `InfiniteVoid.local` domain

---

## Phase 3 – User Administration

* Create Organizational Units
* Create users
* Create security groups
* Configure user permissions

---

## Phase 4 – Windows Client

* Install Windows 11
* Join the client to the domain
* Verify authentication

---

## Phase 5 – Group Policy

Configure common Group Policies, including:

* Password Policy
* Account Lockout Policy
* Desktop Wallpaper
* Disable Control Panel
* Disable USB Storage
* Disable Command Prompt

---

## Phase 6 – File Services

* Configure shared folders
* Configure NTFS permissions
* Test access using different user accounts

---

## Phase 7 – PowerShell Administration

Automate administrative tasks such as:

* Create users
* Reset passwords
* Enable and disable accounts
* Query Active Directory users

---

# Skills Demonstrated

* Windows Server Administration
* Active Directory Domain Services (AD DS)
* Active Directory Users and Computers (ADUC)
* Identity and Access Management (IAM)
* Organizational Unit Administration
* User & Group Management
* DNS Administration
* Group Policy Management
* Windows Authentication
* NTFS Permissions
* Shared Folder Administration
* PowerShell Scripting
* Windows Networking
* Virtualization
* Technical Documentation

---

# Documentation

Each completed phase includes:

* Configuration notes
* Screenshots
* Commands used
* Explanations of administrative decisions

---

# PowerShell

The `PowerShell` directory contains scripts used throughout the project, including:

* User creation
* Password management
* Account administration
* Active Directory queries

---

# Learning Goals

The objective of this project is to gain practical experience with enterprise Windows Server administration while documenting the implementation process in a professional GitHub portfolio.

---

# Future Improvements

Potential future additions include:

* DHCP
* Windows Server Update Services (WSUS)
* Windows Deployment Services (WDS)
* Certificate Services (AD CS)
* DFS
* File Server Resource Manager (FSRM)
* Microsoft Entra ID integration
* Microsoft Intune integration

---

# License

This project is intended for educational and portfolio purposes only.
