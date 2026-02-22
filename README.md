# Active-Directory-Home-Lab
##Title: Active Directory & IT Support Lab Environment
Objective: To build a simulated enterprise network environment to practice system administration, identity management, and help desk troubleshooting.

#Tools & Technologies:

Oracle VirtualBox (Hypervisor)

Windows Server 2022 (Domain Controller)

Windows 10 Enterprise (Client Workstation)

PowerShell (Automation & Configuration)

#Phase 1: Network & Server Configuration

Description: Configured a NAT Network to isolate the lab environment. Deployed Windows Server 2022 Core and assigned a static IP (192.168.10.1) and loopback DNS (127.0.0.1) via PowerShell.



#Phase 2: Active Directory Deployment

Description: Installed Active Directory Domain Services (AD DS) and promoted the server to a Domain Controller for the home.lab domain.



Phase 3: Client Integration & Identity Management

Description: Joined a Windows 10 client workstation to the home.lab domain. Utilized PowerShell to securely provision a new standard user account (jdoe) without utilizing the GUI.

