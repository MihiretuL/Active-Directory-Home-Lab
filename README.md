# Active Directory & IT Support Lab

## Objective
The purpose of this project was to architect and deploy a fully functional on-premises Active Directory environment from scratch. This simulated corporate network serves as a hands-on environment to practice System Administration, Identity & Access Management (IAM), and Help Desk troubleshooting.

## Tools & Technologies Used
* **Hypervisor:** Oracle VirtualBox
* **Server OS:** Windows Server 2022 (Desktop Experience)
* **Client OS:** Windows 10 Enterprise
* **Core Services:** Active Directory Domain Services (AD DS), DNS, DHCP
* **Network Protocol:** IPv4, ICMP, NAT Networking

---

##  Phase 1: Network Architecture & Server Deployment
In this phase, I established the foundation of the corporate network.
* Configured an isolated virtual NAT Network to ensure secure communication between virtual machines.
* Deployed a Windows Server 2022 instance and configured a static IPv4 address (`192.168.10.1`) and loopback DNS (`127.0.0.1`).
* Renamed the server to `DC-01` to adhere to standard enterprise naming conventions.

![server manager dashboard](/iamges/server-manager.png)

---

##  Phase 2: Active Directory Forest Creation
With the server networked, I elevated it to act as the central authority for the environment.
* Installed the **Active Directory Domain Services (AD DS)** role via Server Manager.
* Promoted the server to a Domain Controller and established the root forest/domain: `hq.corp`.
* Verified local DNS resolution to ensure client machines could locate the Domain Controller.

![domain controller created](/images/hq.corp-domain.png)

---

## 💻 Phase 3: Client Integration & Connectivity
This phase demonstrated the actual onboarding of a corporate workstation.
* Deployed a Windows 10 client virtual machine.
* Performed ping tests (ICMP) to verify network connectivity between the client and the Domain Controller, adjusting Windows Defender Firewall rules as necessary.
* Renamed the workstation to `WIN10-CLIENT` and successfully joined it to the `hq.corp` domain.

![client creation UI screenshot](/images/client-added.png)

---

##  Phase 4: User Management & Group Policy (In Progress)
*(Currently taking a masterclass to implement the following features:)*
* Provisioning standard and administrator user accounts.
* Creating Organizational Units (OUs) for department isolation (e.g., HR, IT, Finance).
* Pushing Group Policy Objects (GPOs) for password complexity, screen lockouts, and mapped network drives.