#  Windows-Server-2025-Windows-11-Enterprise-Lab

This IT and cybersecurity home lab project was built to simulate a small enterprise Windows environment using Oracle VirtualBox, Windows Server 2025, and Windows 11 Pro.

## 🏗️ Lab Architecture

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/d616fa5705bf4e811b901e743f2fdd1af102daf1/Windows%20Server%2025%20%26%20Win%2011%20Enterprise%20Lab%20Architecture%201.png">

## 📥 Step 1 | Download Windows ISO Files

Downloaded:
✅ Windows Server 2025 Evaluation ISO
✅ Windows 11 Pro ISO

Source:
Microsoft Evaluation Center

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/445cc667880f57c668475ec1b0109a3539169f55/Windows%20Server%202022/Select%20Windows%20Server%202025%20Download%20.png">



## 🖥️ Step 2 | Create Windows Server 2025 Virtual Machine

Created a new virtual machine in Oracle VirtualBox.

Configuration:

🛠️ Operating System:
Microsoft Windows

🛠️ Version:
Windows 2022 (64 bit)

🛠️ VM Name:
WinServer25

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/a930b6e0e35736c0fc96b2f7d25150acdc5be909/Windows%20Server%202022/Step%202%20Installing%20Winserver%2025%20on%20VM.png">



## ⚙️ Step 3 | Configure Hardware Resources

Allocated system resources for the virtual machine.

Hardware Configuration:

💾 Memory:
5120 MB RAM

🧠 Processors:
4 CPUs

🖥️ EFI Enabled:
Optional depending on setup

This step ensured the virtual machine had enough resources to run enterprise services efficiently.


<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/76a4f944c5b61046062a1fbb48fb8a87a1951c8c/Windows%20Server%202022/Step%203%20Set%20up%20Hardaware.png">



##

## 💽 Step 4 | Configure Virtual Disk

Created and expanded the virtual hard disk.

Disk Configuration:

📦 Disk Type:
VDI (VirtualBox Disk Image)

💾 Disk Size:
100 GB

This provides enough storage for:
✅ Windows Server
✅ Active Directory
✅ Future security tools and labs

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/52c60fd32dfa386d9e2d5c483843d8f67e0690ee/Windows%20Server%202022/Step%204%20Increasing%20the%20virtual%20disk.png">

## 🪟 Step 5 | Install Windows Server 2025

Installed:
Windows Server 2025 Standard Evaluation Desktop Experience

The installation process included:
✅ System setup
✅ Initial configuration
✅ Administrator password creation

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/074c6911b3311a039075dce2b857f5f9a3ff7b69/Windows%20Server%202022/Step%206%20Ready%20to%20install%20on%20the%20VM.png">

## 🖧 Step 6 | Configure Server Manager

After installation, opened Server Manager to begin configuring enterprise services.

Verified:
✅ Local Server
✅ Server Roles
✅ Initial System Health

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/9c19d485498d23007dbd4c1094fb9d71d5f43260/Windows%20Server%202022/Step%207%20Inside%20Win%20server%202025.png"> 


## 🔐 Step 7 | Install Active Directory Domain Services

Installed:
✅ Active Directory Domain Services (AD DS)

Included management tools:
✅ Group Policy Management
✅ AD DS Administrative Center
✅ PowerShell Tools

This prepares the server to become a Domain Controller.

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/9c19d485498d23007dbd4c1094fb9d71d5f43260/Windows%20Server%202022/Step%2011%20Adding%20different%20features%20.png">

##
## 🌐 Step 8 | Configure Domain Controller

Configured:
✅ New Forest
✅ Root Domain
✅ DNS Services

Functional Levels:

Windows Server 2025

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/acf0b487fb5368cafd7a1589b3cd535ba2c9b414/Windows%20Server%202022/Step%2012%20Set%20up%20passworf%20for%20Directory%20Service%20Restore%20Mode.png">

##

## 🔑 Step 9 | Configure DSRM Password

Configured the:
Directory Services Restore Mode (DSRM) password

Purpose:
The DSRM password is used for:
✅ Active Directory recovery
✅ Domain controller maintenance
✅ Disaster recovery operations

<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/acf0b487fb5368cafd7a1589b3cd535ba2c9b414/Windows%20Server%202022/Step%2013%20This%20is%20when%20we%20are%20creating%20a%20new%20domain%20forest%20.png">

## 🧠 Step 10 | Configure NetBIOS Name

Configured the NetBIOS domain name for proper domain identification inside the network environment.

Example:
TMS
<img width="1000" alt="image" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/50ad4ad8fc6762f52924ad29c7299bc5e71861ad/Windows%20Server%202022/Step%20100%20NetBios.png">
