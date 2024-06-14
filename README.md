# Active-Directory

# Objective
The objective of the Active Directory Lab project is to gain hands-on experience through designing and implementing an Active Directory using Server 2019. This involves provisioning, maintenance, and de-provisioning of 1000 user accounts to integrate administrative tasks. This project also aims to set up Remote Access Server (RAS) features to support Network Address Translation (NAT) and Port Addressing Translation (PAT).


# Skills Learned
- Active Directory Administration
- Networking
- Remote Access Configuration

# Tools Used
- VM Workstation
- Windows 2019 ISO
- Wi-Fi Router
- Powershell ISE

# Steps
If you want to re-create this project yourself, follow the following steps:
- Setup your environment by installing Virtualization Software, in this lab I used Oracle VM VirtualBox
  - Make sure your Virtualization is enabled in your BIOS
  - Download Windows 10 ISO
  - Download Windows Server 2019 ISO and install it on physical / virtual machine
- Install Active Directory Domain Services
  - Create your domain
  - Use Group Policy Management Console to configure Group Policy Objects
- Automate user deployment with PowerShell
  - PowerShell ISE
  - Create a script that will create 1000 users with specific attributes
- Setup Network
  - 2 NICS, 1 for internet, 1 for internal VM
  - Adapter 1: NAT
  - Adapter 2: Internal Network
- Documentation
  - document scripts, procedures to use in the future ( in cased its needed )
- Create Backups
  - Make sure you have created backups of your VM and server configurations

Done!
