# PHASE 1

STEP 1:  Download the Prerequisites

    # This project uses Microsoft Evaluation editions

    # Download Windows Server 2022 Evaluation
    # Download Windows 11 Enterprise Evaluation
    # Download Oracle VirtualBox

STEP 2: Install and configure the Virtual Machines

    # Credentials for Windows Server Evaluation
    Username: Administrator
    Password: WindowsLab2026!

    # Credentials for Windows 11 Evaluation
    Username: Admin
    Password: WindowsLab2026$

STEP 3: Rename the server to DC01

    # Open Server Manager, then head to Local Server, click on the Server's Name,
    in this case 'WIN-M3TE09BT9RP' change it to 'DC01' by clicking on Change button,
    beside the label "To rename this computer or change its domain or workgroup, click Change." 
    Then perform a system restart to apply changes.

STEP 4: Configure the VirtualBox Network

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

Step 5: Configure a static IP address

    # Why do we need to configure our Domain Controller's IP address?
    because we do not want DHCP to set it automatically for us, 
    a Domain Controller needs to have a fixed, predictable IP address.

    # Open Command Prompt by pressing 
    Win + R or Win + S, type cmd and hit enter, we first verify the ip addresses, 
    our virtual machines begin with 10.x.x.x and our host machine begins with 192.x.x.x, therefore
    , we have successfully created a subnet on our last step. Now, let us open our Control Panel.

Step 6: Verify Connectivity

    # I opened the cmd terminal and typed 'ipconfig /all' on both machines, I tried to verify the connection 
    between the DC01 machine to our PC01 machine by pinging them, however I recieved a request timed out response. 
    I went back to the VirtualBox network settings to check the issue, maybe it was because I set the network name
    or maybe the network type wrong, in which I did not, I performed 'ipconfig /all' command again on both machines
    and carefully analyzed the issue, I then found out that I can ping the default gateway and recieve responses on 
    both machine, so why can't I ping the other machine? The answer was simple, a firewall was blocking the ping
    or icmp request from one machine to the other. So to test it, I temporarily opened both machine's inbound rule
    and pinged them together, as a result, they started communicating with each other,
    and I found out that the issue was in the firewall itself and have fixed the issue.

# PHASE 1 Complete 