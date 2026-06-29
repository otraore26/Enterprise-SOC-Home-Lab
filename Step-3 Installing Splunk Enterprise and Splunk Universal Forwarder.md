<div align="center">

# 🚀 Splunk Enterprise Installation on Red Hat Enterprise Linux 10

### SIEM Deployment Lab • Red Hat Enterprise Linux 10 • Oracle VirtualBox

![Splunk](https://img.shields.io/badge/Splunk-Enterprise-green?style=for-the-badge&logo=splunk)
![Red Hat](https://img.shields.io/badge/Red_Hat-RHEL_10-red?style=for-the-badge&logo=redhat)
![Linux](https://img.shields.io/badge/Linux-System_Admin-blue?style=for-the-badge&logo=linux)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

<img src="images/7 Splunk Enterprise.png" width="900">

### Successfully Installed and Configured Splunk Enterprise 10.2.2 on Red Hat Enterprise Linux 10

</div>

---

# 📖 Overview

This project demonstrates the complete deployment of **Splunk Enterprise 10.2.2** on **Red Hat Enterprise Linux 10** running inside **Oracle VirtualBox**.

During this lab I performed:

- ✅ Downloading Splunk Enterprise
- ✅ Installing Splunk using RPM
- ✅ Starting the Splunk Service
- ✅ Accepting the Splunk License
- ✅ Creating the Administrator Account
- ✅ Accessing Splunk Web
- ✅ Configuring Receiving Port (9997)
- ✅ Configuring Data Inputs
- ✅ Verifying Log Ingestion

---

# 🖥️ Lab Environment

| Component | Details |
|-----------|----------|
| 💻 Hypervisor | Oracle VirtualBox |
| 🐧 Operating System | Red Hat Enterprise Linux 10 |
| 📊 SIEM | Splunk Enterprise 10.2.2 |
| 🌐 Browser | Firefox |
| 🔌 Receiving Port | TCP 9997 |
| 🌍 Web Interface | Port 8000 |

---

# 📌 Architecture

```text
                    +-------------------------+
                    | Windows 11 / Browser    |
                    +------------+------------+
                                 |
                                 | HTTP (8000)
                                 |
                  +--------------v--------------+
                  |    Splunk Enterprise         |
                  |   Red Hat Enterprise Linux   |
                  +--------------+--------------+
                                 |
                                 |
                          Linux System Logs
                                 |
                     /var/log/messages
                     /var/log/audit/audit.log
```

---

# 🚀 Installation Walkthrough

---

# Step 1 — Download Splunk Enterprise

Visit the Splunk download page.

<img src="https://github.com/otraore26/Enterprise-SOC-Home-Lab/blob/999e081ba344fc08ea15182ace67605ebbbe229d/Splunk%20Screenshoots/1-1Inside%20Splunk%20Website.png" width="1000">

---

Select **Splunk Enterprise**.

<img src="https://github.com/otraore26/Enterprise-SOC-Home-Lab/blob/d9559adc814d87b60a146a79381496696554dea2/Splunk%20Screenshoots/1-2%20How%20to%20download%20free%20Splunk%20Enterprise%20.png" width="1000">

---

# Step 2 — Download the Installer

Download the Linux RPM package.

```bash
cd ~/Downloads

wget https://download.splunk.com/products/splunk/releases/10.2.2/linux/splunk-10.2.2-linux-x86_64.rpm
```

<img src="images/3 Downloading to the Redhat Server.png" width="1000">

---

# Step 3 — Install Splunk

Install the RPM package.

```bash
sudo rpm -ivh splunk-10.2.2*.rpm
```

Installation Path

```
/opt/splunk
```

<img src="images/4 Installing Splunk on Redhat.png" width="1000">

---

# Step 4 — Verify Installation

```bash
cd /opt

ls
```

Expected Output

```
splunk
```

<img src="images/5 Splunk Installation on Redhat Linux.png" width="1000">

---

# Step 5 — Start Splunk

```bash
cd /opt/splunk/bin

sudo ./splunk start --accept-license
```

Splunk automatically:

- Generates SSL certificates
- Creates indexes
- Starts the Splunk daemon

<img src="images/6 1 Splunk.png" width="1000">

<br>

<img src="images/6 2 Splunk.png" width="1000">

---

# Step 6 — Verify Hostname

```bash
hostname
```

Example

```
vbox
```

<img src="images/6 3 To verify the hostname.png" width="900">

---

# Step 7 — Login to Splunk

Open

```
http://127.0.0.1:8000
```

Create the Administrator account.

<img src="images/Splunk password.png" width="1000">

<br>

<img src="images/7 Splunk Enterprise.png" width="1000">

---

# Step 8 — Enable Receiving Port

Navigate to

```
Settings
↓

Forwarding and Receiving
↓

Receive Data
↓

New Receiving Port
```

Configure

```
9997
```

<img src="images/8 Reciving data is enable.png" width="1000">

---

# Step 9 — Configure Data Inputs

Go to

```
Settings
↓

Data Inputs
```

<img src="images/Step 9 go setting and go to the Data.png" width="1000">

---

Click **Add Data**

<img src="images/Step 10 Then you will scrow down and select Forward.png" width="1000">

---

Choose the Forward option.

<img src="images/Step 11 Select the data.png" width="1000">

---

# Step 10 — Start Splunk Service

```bash
cd /opt/splunk/bin

sudo ./splunk start
```

Or

```bash
sudo ./splunk start --run-as-root
```

<img src="images/How to run splunk as a root user.png" width="1000">

<br>

<img src="images/Step 12 Running a bash scripting to run Splunkl.png" width="1000">

---

# Step 11 — Verify Splunk

Splunk should display

```
Waiting for web server...

Done
```

<img src="images/Step 13 Splunk server.png" width="1000">

---

# 🔍 Verify Data Ingestion

Run

```spl
index=*
```

Verify events are successfully indexed.

Example logs include:

- Linux Audit Logs
- System Messages
- Authentication Logs
- Syslog Events

---

# 🛠 Useful Commands

Start Splunk

```bash
sudo /opt/splunk/bin/splunk start
```

Stop Splunk

```bash
sudo /opt/splunk/bin/splunk stop
```

Restart Splunk

```bash
sudo /opt/splunk/bin/splunk restart
```

Status

```bash
sudo /opt/splunk/bin/splunk status
```

Hostname

```bash
hostname
```

---

# 📂 Project Structure

```
Splunk-Enterprise-RHEL10
│
├── README.md
│
├── images
│   ├── 1-1Inside Splunk Website.png
│   ├── 1-2 How to download free Splunk Enterprise.png
│   ├── ...
│   └── Step 13 Splunk server.png
```

---

# 💡 Skills Demonstrated

| Linux | Splunk | Networking | SIEM |
|-------|---------|------------|------|
| ✅ RPM Installation | ✅ Splunk Enterprise | ✅ Port Configuration | ✅ Log Ingestion |
| ✅ Linux Administration | ✅ Web Interface | ✅ TCP 9997 | ✅ Data Inputs |
| ✅ Bash | ✅ Indexing | ✅ Forwarding | ✅ Search |

---

# 🎯 Learning Outcomes

✔ Installed Splunk Enterprise on Red Hat Enterprise Linux 10

✔ Configured Splunk Web Interface

✔ Enabled Receiving Port 9997

✔ Configured Data Inputs

✔ Verified Linux Log Collection

✔ Successfully deployed a functional SIEM environment

---

<div align="center">

## ⭐ If you found this project helpful, feel free to star the repository!

Made with ❤️ by **Ousmane Traore**

</div>
