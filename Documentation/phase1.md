PHASE 1 - Windows Server 2025 Evaluation Installation

    # This project uses Microsoft Evaluation editions.

    # Windows Server 2025 Evaluation -Download from Microsoft's Evaluation Center
    # Windows 11 Enterprise Evaluation - Download from Micosoft's Evaluation Center
    # Oracle VirtualBox - Download from Oracle

STEP 1:  Download the Prerequisites

    # Download Windows Server 2025 Evaluation
    # Download Windows 11 Enterprise Evaluation
    # Download Oracle VirtualBox

STEP 2: Install and configure the Virtual Machines

    # Credentials for Windows Server Evaluation
    Username: Administrator
    Password: WindowsLab2026!

    # Credentials for Windows 11 Evaluation
    Username: Admin
    Password: WindowsLab2026$

STEP 5: Rename the server to DC01

    # Open Server Manager, then head to Local Server, click on the Server's Name,
    in this case 'WIN-M3TE09BT9RP' change it to 'DC01' by clicking on Change button,
    beside the label "To rename this computer or change its domain or workgroup, click Change." 
    Then perform a system restart to apply changes.

STEP 6: Configure the VirtualBox Network

    # Before we begin our connection, we first need to know what connectivity best fits our scenario,
    in this case, we will use a NAT Network, because we want our system to access the internet, 
    as well as download updates and install additional tools. While also giving us a 'private network' 
    which contains my virtual system from interfering with my home LAN.
    Why not use Bridged Adapter? Because we do not want our virtual system to be accessed and 
    known to other people on the LAN, and that we are doing this safely in a private-controlled environment.

    # We shut down the server first, open our Virtual Machine, click on settings, then head to Network, 
    and change it to NAT Network. 
    
    # Repeat for all Machines participating in the lab, 
    in this case, the "Windows 11 Enterprise Evaluation" Machine.

    # The DC01 Server and Windows 11 Enterprise is already configured to NAT Network.

Step 7: Configure a static IP address


Step 8: Verify Connectivity



