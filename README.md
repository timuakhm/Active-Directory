# Active-Directory

# Objective
The objective of the Active Directory Lab project is to gain hands-on experience through designing and implementing an Active Directory using Server 2019. This involves provisioning, maintenance, and de-provisioning of 1000 user accounts to integrate administrative tasks. This project also aims to set up Remote Access Server (RAS) features to support Network Address Translation (NAT) and Port Addressing Translation (PAT).


# Skills Learned
- Active Directory Administration
- Networking
- Remote Access Configuration

# Tools Used
- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Wi-Fi Router
- Powershell ISE

# Operating Systems Used
- Windows 10 (22H2) ISO
- Windows Server 2019 ISO

# Configuration Steps
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

# Flowchart
![Active Directory Infrastructure](https://github.com/timuakhm/Active-Directory/assets/171197854/1c0b53b4-1e7a-4c3b-b371-c2c8197c388e)
Domain Controller has to have a static private IP Address. Client1 will connect to Domain Controller via the internal VM network. To ensure connectivity we will ping Domain Controller from Client1. Make sure to enable ICMPv4 on the Domain Controller firewall


![Domain Controller Firewall Rules](https://github.com/timuakhm/Active-Directory/assets/171197854/234a21ef-dc1f-4231-85d4-9e4f93159c51)
![client1 cmd](https://github.com/timuakhm/Active-Directory/assets/171197854/f3591107-c0b8-41fd-9cc7-25362369f4e9)

Now we need to get back into Domain Controller to install Active Directory Users and Computers. As well as promote the VM to DC, and setup a new forest "mydomain.com" afterwards, restart and login to the Domain Controller as a user.
![Active Directory Users and Computers](https://github.com/timuakhm/Active-Directory/assets/171197854/70b629b9-9c73-4089-b9ff-38ab1ab17337)
![DC1 Admin](https://github.com/timuakhm/Active-Directory/assets/171197854/59205e9b-ad74-4811-bd63-64be37dd036f) 

As seen above, we have created Organizational Units (OU) _ADMINS_ and _USERS_


Lastly, we will use a PowerShell script to help us generate 1000 users into the domain. We will run the script in Powershell ISE
![DC1 Users](https://github.com/timuakhm/Active-Directory/assets/171197854/554efbdb-d106-4995-ab19-03755814d29c)
![68747470733a2f2f692e696d6775722e636f6d2f457a57473875672e706e67](https://github.com/timuakhm/Active-Directory/assets/171197854/161510e3-5d52-4b54-a456-67aec6563738)



