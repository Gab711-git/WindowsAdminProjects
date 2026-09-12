# 🖥️ Windows Server Administration Homelab

A hands-on Windows Server homelab built using Oracle VirtualBox to practice administration in a simulated enterprise environment.

The lab uses DC01 as the domain controller for `InfiniteVoid.local` and PC01 as a Windows 11 client. This project is in progress. The notes currently cover installation, Active Directory deployment, users and groups, and initial Group Policy configuration.

**Start here:** [Prerequisites](Documentation/Prerequisites.md) → [Phase 1](Documentation/phase1.md) → [Phase 2](Documentation/phase2.md) → [Phase 3](Documentation/phase3.md)

## Contents

* [Lab environment](#lab-environment)
* [Documentation and roadmap](#documentation-and-roadmap)
* [Repository structure](#repository-structure)
* [Skills practiced so far](#skills-practiced-so-far)
* [Documentation gaps to resolve](#documentation-gaps-to-resolve)
* [Future improvements](#future-improvements)

## Lab Environment

| Component | Technology / configuration |
| --- | --- |
| Virtualization | Oracle VirtualBox |
| Server OS | Windows Server 2025 Evaluation |
| Client OS | Windows 11 Enterprise Evaluation |
| Domain | `InfiniteVoid.local` |
| Domain controller | `DC01` |
| Client | `PC01` |
| Network | NAT Network |
| DC01 IP / preferred DNS | `10.0.3.10` |
| Subnet mask | `255.255.255.0` |
| Default gateway | `10.0.3.1` |

The Server 2025 download is confirmed by the saved Phase 1 screenshot and matches the prerequisites and Phase 2 notes.

## Documentation and Roadmap

Phases 1–3 are recorded as complete. Phase 3 includes evidence of effective domain policy, password reset acceptance/rejection, and actual test-account lockout. Client setup and Group Policy work overlap phases, as noted below.

| Phase | Scope | Status / documentation |
| --- | --- | --- |
| 1 | VM installation, networking, and connectivity | [Complete](Documentation/phase1.md) |
| 2 | AD DS, domain controller promotion, and DNS installation | [Complete](Documentation/phase2.md) |
| 3 | OUs, users, groups, and initial Group Policy validation | [Complete](Documentation/phase3.md) |
| 4 | Client naming, DNS setup, domain join, and authentication | Walkthrough pending |
| 5 | Additional Group Policy and validation | Planned |
| 6 | Shared folders, share/NTFS permissions, and access testing | Planned |
| 7 | PowerShell user and account automation | Planned |

Client installation is covered in Phase 1, and Phase 3 already includes domain-user testing and PC01 organization. Phase 4 will fill in the missing rename and domain-join procedure. Phase 5 will build on the password and lockout settings with validation and planned wallpaper, Control Panel, USB storage, and Command Prompt restrictions.

Download resources are listed in [Prerequisites](Documentation/Prerequisites.md). Screenshots are stored by phase in [Screenshots](Screenshots/).

## Repository Structure

```text
WindowsAdminProjects/
├── Documentation/
│   ├── Prerequisites.md
│   ├── phase1.md
│   ├── phase2.md
│   └── phase3.md
├── Powershell/
│   └── cmd1                 # Empty placeholder
├── Screenshots/
│   ├── phase1/
│   ├── phase2/
│   └── phase3/
└── READme.md
```

Windows installation ISOs are not included in this repository.

## Skills Practiced So Far

* Virtual machine setup and Windows networking
* Windows Server installation and administration
* Active Directory Domain Services deployment with DNS
* Active Directory Users and Computers (ADUC)
* Organizational unit, user, and security group administration
* Initial Group Policy configuration
* PowerShell commands for Active Directory verification
* Technical documentation and troubleshooting

Shared folder administration, NTFS permissions, and reusable PowerShell automation remain learning objectives for later phases. The `Powershell/cmd1` file is currently empty; the existing verification commands are documented in Phase 3.

## Documentation Gaps to Resolve

* Add VM hardware allocations and the NAT Network name and DHCP range to Phase 1.
* Add the PC01 domain-join walkthrough so readers can reproduce the setup used in Phase 3.
* Document the historical client rename sequence in Phase 4. Phase 3 now confirms the current Windows hostname is `PC01`.

## Future Improvements

Potential additions after the core roadmap include DHCP, WSUS, WDS, AD CS, DFS, File Server Resource Manager, Microsoft Entra ID integration, and Microsoft Intune integration.

## Purpose

This project is intended for educational and portfolio purposes, with the goal of building practical Windows Server administration experience and documenting the implementation as it progresses.
