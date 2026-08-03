# PHASE 2

STEP 1: Install Active Directory Domain Services Role

    # Why do we need Active Directory? 

    #We need Active Directory Domain Services because we need to store information about the users, computers,
    and other end devices on our enterprise network. 
    Active Directory also helps administrators enforce policies and facilitate resource sharing and 
    collaboration between employees within an organization.

    # First we open 'Server Manager' on our DC01 machine, we then head to 'Manage' then to 'Add Roles and Features'.

    # We then get taken to the Wizard tab, choose Role-based or feature-based installation and click next.

    # In Server Selection part, we will see DC01, our server name, we leave it selected, then we click next

    # In Server Roles, we leave Active Directory Domain Services checked, then Windows will ask us 
    'Add features that are required?' we then leave 'Add Features' checked.

    # In Features, we just click next.

    # In Active Directory Domain Services Information part, it basically explains Active Directory.

    # In Confirmation, we set all to default, we can also leave 'Restart the destination server automatically if required' 
    part checked. But in this lab, we did not select this option, and then we hit 'Install'. 
    We then wait for the installation process, it is important to not close the Server Manager, 
    when it is finished, do not restart manually, after installation is complete, we will recieve a yellow notification flag
     on the top right part of Server Manager, do not click it yet.

STEP 2: Promote DC01 to a Domain Controller

    # After installation finishes, we will promote DC01 to a Domain Controller, we click 'Promote this server to a domain controller'

    # In Deployment Configuration, we will see 3 choices, 'choose Add a new forest':

        # Add a domain controller to an existing domain
        # Add a new domain to an existing forest
        # Add a new forest

    # Now for the Root domain name, we will name it: InfiniteVoid.local, we then click next.

    # In Domain Controller Options, we will use the following configurations:

        # Forest Functional Level: Windows Server 2025
        # Domain Functional Level: Windows Server 2025
        # DNS Server : Checked
        # Global Catalog : Checked
        # Read-Only Domain Controller(RODC) : Unchecked
    
    # Directory Service Restore Mode(DSRM) : Password

        # Do not use Administrative Password, they are not the same, and is important to not use the same password as is.
        It is a recovery password, if ever we need to resore or perform a backup on our Active Directory. 
        It is also important to also use a strong password we can remember, or use a password manager.

    # Password for Directory Services Restore Mode (DSRM): WindowsLabRecover!, we then click next.

    # In DNS options, we will recieve a warning, 'A delegation, for this DNS server cannot be created.' 
    Do not panic, and just ignore the message, as this was expected because it is our first domain controller. We then click next.

    # In Additional options, we should see 'NetBIOS domain name: INFINITEVOID', leave it as is and click next.

    # In Paths, we will see:

        # Database folder
        # Log files folder
        # SYSVOL folder

    # Leave the default locations

        # C:\Windows\NTDS
        # C:\Windows\NTDS
        # C:\Windows\SYSVOL
    
    # In Review Options, it is just a summary of our configuration choices, and then proceed with next.

    # In Prerequisites Check, Windows will perform various checks, might see some warnings, but as long as there 
    are no errors we are good to proceed and hit 'Install', and wait for installation.

    # After all this, the server will Install Active Directory, DNS, configure the domain based on our trim, and reboot automatically.

    # We will notice a few changes, firstly, our login screen changes to 'INFINITEVOID\Administrator', 
    we use our default password, not the DSRM password to login, and hit 'enter'. 

STEP 3: Verify

    # Verify the domain and hostname

    # Open Command prompt, type in 'echo %USERDOMAIN%' and hit 'enter'. We are expecting 'INFINITEVOID' output. 
    then type 'hostname' and hit 'enter'. We are expecting 'DC01'

    # Verify the Active Directory

    # Open Server Manager, then head to Tools, we should be able to see new tools such as the following:

        # Active Directory Users and Computers
        # Active Directory Administrative Center
        # Active Directory Domains and Trusts
        # Active Directory Sites and Services
        # DNS
        # Group Policy Management
    
    # Again on Server Manager, head to Tools. head to Active Directory Users and Computers, 
    on the left-hand side, expand 'InfiniteVoid.local'.

    # We should be able to see containers such as Builtin, Computers, Domain Controllers, and Users. 
    This is our Active Directory database.

# PHASE 2 Complete