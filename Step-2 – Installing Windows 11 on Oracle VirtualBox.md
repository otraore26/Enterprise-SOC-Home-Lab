# 🖥️ Windows 11 Enterprise Lab Deployment

This project documents the deployment and configuration of a Windows 11 Pro virtual machine inside Oracle VirtualBox as part of my enterprise cybersecurity homelab.

The Windows 11 workstation was later prepared for Active Directory domain integration within the `tms.com` lab environment.

---

# 📌 Objectives

✅ Deploy Windows 11 Pro in VirtualBox  
✅ Configure enterprise workstation settings  
✅ Prepare Windows client for Active Directory  
✅ Simulate enterprise endpoint deployment  
✅ Practice Windows administration and virtualization  

---

# 🧰 Technologies Used

- Oracle VirtualBox
- Windows 11 Pro
- Windows Server 2025
- Active Directory
- DNS
- PowerShell
- Command Prompt

---

# 🌐 Lab Environment

| Component | Details |
|---|---|
| Domain Name | `tms.com` |
| Client Machine | Windows 11 Pro |
| Domain Controller | Windows Server 2025 |
| Virtualization Platform | Oracle VirtualBox |

---

# 📥 Step 1 — Download Windows 11 ISO

Downloaded the official Windows 11 ISO image from Microsoft for x64 devices.

<img width="1000" alt="Step 1" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%201%20Download%20Windows%2011.png">

---

# 🖥️ Step 2 — Create Windows 11 Virtual Machine

Created a new Windows 11 virtual machine inside Oracle VirtualBox and mounted the ISO image.

<img width="1000" alt="Step 2" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%202%20Installing%20WIN11%20On%20Virtualbox.png">

---

# ⚙️ Step 3 — Configure Hardware Resources

Allocated hardware resources for the virtual machine.

Configuration:
- 5 GB RAM
- 4 Virtual CPUs

<img width="1000" alt="Step 3" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%203%20Increase%20the%20Hardware%20.png">

---

# 💽 Step 4 — Configure Virtual Disk

Created and configured an 80 GB virtual disk for the Windows 11 virtual machine.

<img width="1000" alt="Step 4" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%204%20Increasing%20the%20Virtual%20disk.png">

---

# 🚀 Step 5 — Start Windows 11 Installation

Booted the virtual machine and launched the Windows 11 setup process.

<img width="1000" alt="Step 5" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%205%20Win%2011%20running%20on%20VB.png">

---

# 🌍 Step 6 — Configure Keyboard Settings

Selected keyboard layout and regional settings during installation.

<img width="1000" alt="Step 6" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%206%20Selecting%20Keyboard.png">

---

# 🏢 Step 7 — Select Windows 11 Pro Edition

Selected Windows 11 Pro because it includes enterprise features useful for cybersecurity and Active Directory labs.

Features include:
- Domain Join
- Group Policy
- Remote Desktop
- BitLocker

<img width="1000" alt="Step 7" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%207%20Selecting%20Win%2011%20Pro%20since%20it%20includes%20features%20useful%20for%20labs.png">

---

# 💾 Step 8 — Select Installation Disk

Selected the virtual disk where Windows 11 would be installed.

<img width="1000" alt="Step 8" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%208%20Selecting%20location%20to%20install%20WIN11.png">

---

# 🔓 Step 9 — Bypass Microsoft Account Requirement
<img width="1000" alt="Step 8" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%209%20how%20by%20pass%20Win11%20Local%20Setup%20.png">

<img width="1000" alt="Step 8" src="https://github.com/otraore26/Windows-Server-2025-Windows-11-Enterprise-Lab/blob/388b43b2702b0d9d4b5d0d8a8b77fb1db3ab26a8/Windows%2011/Step%2010%20Win11%20Setup%20Bypass.png">

Used Command Prompt during setup to bypass the Microsoft online account requirement.

Command used:

```cmd
start ms-cxh:localonly

