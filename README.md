# Setting-up-Remote-Access

# Assisted Lab: Setting Up Remote Access

## Overview

This lab demonstrates how to securely configure and use remote access technologies in a mixed Windows and Linux environment. It covers Microsoft Remote Desktop (RDP), Secure Shell (SSH), and remote administration using both graphical and command-line tools.

The exercises reinforce Security+ concepts related to secure enterprise infrastructure and secure remote administration. :contentReference[oaicite:0]{index=0}

---

## Objectives

- Configure Microsoft Remote Desktop on Windows
- Allow authorized users to access a remote Windows system
- Verify SSH installation and configuration on Kali Linux
- Confirm SSH service status
- Connect from Windows to Linux using:
  - PuTTY (GUI)
  - OpenSSH Client (CLI)
- Perform basic remote administration tasks
- Understand secure remote management best practices

---

## Technologies Used

- Windows Server 2019
- Kali Linux
- Microsoft Remote Desktop (RDP)
- OpenSSH Server
- OpenSSH Client
- PuTTY
- Windows Command Prompt
- Linux Terminal

---

## Skills Demonstrated

- Remote Desktop configuration
- Secure remote administration
- SSH authentication
- Windows administration
- Linux administration
- Command-line operations
- Network connectivity verification
- User permission management

---

# Lab Environment

| Machine | Operating System | Purpose |
|----------|------------------|---------|
| DC10 | Windows Server 2019 | Administrator workstation |
| PC10 | Windows Server 2019 | Remote Desktop target |
| KALI | Kali Linux | SSH server |

:contentReference[oaicite:1]{index=1}

---

# Part 1 – Configure Microsoft Remote Desktop

### Tasks Completed

- Enabled Remote Desktop
- Allowed remote connections
- Added authorized user (Rene)
- Connected remotely from DC10 to PC10
- Verified remote desktop functionality
- Verified computer name
- Verified network configuration using `ipconfig`
- Disconnected the remote session

### Commands Used

```cmd
ipconfig
```

### Skills Learned

- Enable RDP
- Remote user authorization
- Remote administration
- Windows remote management

---

# Part 2 – Verify SSH on Kali Linux

### Tasks Completed

Verified OpenSSH installation

```bash
apt list openssh-server
```

Verified Password Authentication

```bash
cat /etc/ssh/sshd_config | grep PasswordAuthentication
```

Checked SSH service status

```bash
systemctl status ssh
```

Determined IP address

```bash
ip a s eth0
```

### Skills Learned

- SSH configuration
- Linux service management
- Authentication methods
- Linux networking

---

# Part 3 – SSH Using PuTTY (GUI)

### Tasks Completed

- Connected to Kali using PuTTY
- Accepted SSH host key
- Logged in as root
- Verified hostname
- Created a directory remotely
- Closed SSH session

### Commands Used

```bash
hostname

mkdir remote

exit
```

### Skills Learned

- GUI-based SSH connections
- Secure authentication
- Remote Linux administration

---

# Part 4 – SSH Using Command Line

### Tasks Completed

Connected using Windows OpenSSH Client

```cmd
ssh root@<Kali-IP>
```

Created a hidden login configuration

```bash
touch ~/.hushlogin
```

Disconnected

```bash
exit
```

Reconnected and confirmed the login banner was suppressed.

### Skills Learned

- CLI SSH connections
- OpenSSH Client usage
- Linux user customization
- Secure remote administration

---

# Security Concepts

- Remote Desktop Protocol (RDP)
- Secure Shell (SSH)
- Password Authentication
- Secure Remote Access
- Least Privilege
- Authentication
- Encryption
- Remote Administration
- Enterprise Infrastructure Security

---

# Security+ Objectives Covered

**CompTIA Security+ (SY0-701)**

- **3.2** Apply security principles to secure enterprise infrastructure.
- **5.6** Implement security awareness practices.

:contentReference[oaicite:2]{index=2}

---

# Key Takeaways

- Remote Desktop enables secure administration of Windows systems.
- SSH provides encrypted remote access for Linux administration.
- PuTTY offers a graphical SSH client for Windows.
- OpenSSH allows secure command-line remote management.
- Restricting remote access to authorized users improves security.
- Verifying service status ensures remote services are operational.
- Remote administration should always use encrypted protocols instead of insecure alternatives.

---

# Repository Structure

```
Setting-Up-Remote-Access/
│
├── README.md
├── screenshots/
│   ├── remote-desktop-enabled.png
│   ├── ssh-status.png
│   ├── putty-login.png
│   ├── ssh-cli.png
│   └── hushlogin.png
└── notes/
    └── lab-notes.md
```

---

# What I Learned

Through this lab, I gained practical experience configuring secure remote access in Windows and Linux environments. I learned how to enable and manage Remote Desktop, verify and troubleshoot SSH services, establish encrypted remote sessions using both GUI and command-line tools, and perform basic remote administration tasks. These are essential skills for Security+, SOC Analyst, and System Administration roles.

---

## Author

**Bayram Guney**

Cybersecurity | Security+ | Network+ | A+ | SOC Analyst Candidate
