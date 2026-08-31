# 🖥️ BIS-Lab Headless Cybersecurity Homelab

## 📌 Project Overview

BIS-Lab is a personal cybersecurity homelab built using repurposed computer hardware configured as a headless server environment.

The purpose of this project was to gain hands-on experience with networking, secure remote administration, system configuration, troubleshooting, and cybersecurity fundamentals in a controlled lab environment.

The lab consists of a dedicated server managed remotely from an administrative workstation over a local network.

**Project Date:** August 12, 2026  
**Project Status:** ✅ Successful

---

## 🎯 Project Objectives

- Build a dedicated cybersecurity homelab using existing hardware
- Configure a system for headless server operation
- Establish network communication between a workstation and server
- Configure SSH for secure remote administration
- Test TCP/IP and ICMP network connectivity
- Practice hostname resolution and DHCP networking
- Configure wired Ethernet connectivity
- Practice command-line troubleshooting
- Apply basic security and access-control concepts
- Build a platform for future cybersecurity labs

---

## 🧰 Technologies & Concepts

- SSH (Secure Shell)
- TCP/IP
- TCP Port 22
- ICMP
- DHCP
- Ethernet
- Hostname Resolution
- Remote System Administration
- Client/Server Architecture
- Disk Encryption
- Command-Line Administration
- Network Troubleshooting
- Headless Server Management

---

## 🔒 Documentation Privacy

This repository uses sanitized system information for security and privacy.

Actual hostnames, usernames, private IP addresses, MAC addresses, serial numbers, account information, and other device identifiers are intentionally excluded or replaced with generic lab identifiers.

| Documentation Name | Purpose |
|---|---|
| `BIS-Lab-Server` | Headless lab server |
| `Admin-Workstation` | Administrative workstation |
| `Lab-Network` | Local lab network |
| `<lab-user>` | Authorized lab account |
| `<PRIVATE-IP>` | Private network address |

---

## ⚙️ Phase 1 — Initial System Configuration

### Server Preparation

The server system was prepared for dedicated homelab use before remote administration was configured.

Initial configuration included:

- Resetting the system to create a clean lab environment
- Creating a dedicated lab account separate from personal accounts
- Enabling full-disk encryption to protect stored data
- Using a temporary HDMI-connected display during initial configuration
- Connecting the server to the local network
- Preparing the system for eventual headless operation

### Administrative Workstation

A separate Windows workstation was designated as the primary administration and cybersecurity workstation.

The workstation was prepared with tools for:

- Remote system administration
- Network troubleshooting
- Packet analysis
- Python development
- Git and GitHub repository management
- Network simulation

Software used included:

- Visual Studio Code
- Python
- Wireshark
- Cisco Packet Tracer
- Git

### Lab Architecture

The initial lab design separated the administrative workstation from the dedicated lab server.

```text
             Lab-Network
             /         \
            /           \
Admin-Workstation    BIS-Lab-Server
        |                  |
 Administration       Homelab Host
 SSH / Analysis       Headless Server
 Development          Future Lab Services
```

**Phase 1 Status:** ✅ Completed

---

## 🌐 Phase 2 — Network Connectivity Testing

After the initial system configuration, I tested communication between the administrative workstation and the homelab server across the local network.

### Connectivity Test

The first test used ICMP to verify that the workstation could communicate with the server.

Command used:

```powershell
ping BIS-Lab-Server
```

### Verification

The connectivity test completed successfully.

- Packets sent: 4
- Packets received: 4
- Packets lost: 0
- Packet loss: 0%

**Result:** ✅ Successful

### Troubleshooting

During the initial test, the command was entered incorrectly in PowerShell, resulting in a command-not-found error.

After identifying and correcting the syntax error, the connectivity test was repeated successfully.

This demonstrated basic command-line troubleshooting and verification rather than assuming the network itself was the source of the failure.

### Concepts Practiced

- ICMP
- TCP/IP networking
- Hostname resolution
- Local network connectivity
- Command-line troubleshooting
- Client/server communication

**Phase 2 Status:** ✅ Completed

---

## 🔐 Phase 3 — SSH Remote Administration

After confirming network connectivity, I configured secure remote administration between the administrative workstation and the headless lab server.

### SSH Configuration

Remote Login was enabled on the lab server to allow SSH connections across the local network.

SSH uses:

- TCP port 22
- User authentication
- Host key verification
- Encrypted remote communication

The administrative workstation was then used to establish an SSH session with the lab server.

```powershell
ssh <lab-user>@BIS-Lab-Server
```

### Verification

The SSH connection was successfully established from the administrative workstation to the lab server.

This confirmed:

- Network connectivity
- Hostname resolution
- SSH service availability
- User authentication
- Remote shell access

**Result:** ✅ Successful

### Security Configuration

Remote administrative access was limited to authorized users.

This helped reduce unnecessary remote access and applied the principle of least privilege to the lab environment.

### Concepts Practiced

- SSH (Secure Shell)
- TCP port 22
- Remote system administration
- Client/server architecture
- User authentication
- Host key verification
- Principle of least privilege
- Command-line administration

**Phase 3 Status:** ✅ Completed

---

## 🖥️ Phase 4 — Headless Server Configuration

After verifying SSH remote access, I configured the lab server to operate in a headless environment without requiring a permanently attached monitor, keyboard, or mouse.

### Headless Configuration

The server was configured to remain accessible over the network while operating without a display.

Configuration included:

- Preventing automatic system sleep when the display is off
- Enabling Wake for Network Access
- Verifying network connectivity
- Verifying SSH remained enabled
- Confirming remote authentication
- Testing remote shell access after disconnecting the display

### Verification

After completing the configuration, I disconnected the temporary display and accessed the server remotely from the administrative workstation.

The server remained reachable through SSH and could be administered without direct physical interaction.

**Result:** ✅ Successful

### Concepts Practiced

- Headless server administration
- Remote system management
- Power management
- Network availability
- SSH administration
- Remote shell access
- Client/server architecture

**Phase 4 Status:** ✅ Completed

---

## 🌐 Phase 5 — Wired Ethernet Configuration

To improve network stability and reliability, I connected the headless lab server directly to the local network using a CAT5e Ethernet cable.

### Ethernet Configuration

The server was connected to the `Lab-Network` using an RJ45 Ethernet connection.

The network configuration used:

- Wired Ethernet
- CAT5e cable
- DHCP address assignment
- IPv4 networking
- Local subnet and default gateway
- Ethernet network interface

### Network Interface Verification

I used macOS networking commands to verify the Ethernet connection and inspect the network interface configuration.

```bash
networksetup -getinfo Ethernet
```

I also inspected the Ethernet interface using:

```bash
ifconfig en0
```

For security and privacy, actual IP addresses, MAC addresses, and other network identifiers are intentionally excluded from this documentation.

Example sanitized network information:

```text
IP Address: <PRIVATE-IP>
Subnet: <PRIVATE-SUBNET>
Router: <PRIVATE-GATEWAY>
Interface: en0
Address Assignment: DHCP
```

### Verification

The Ethernet interface was active and received its network configuration through DHCP.

Remote connectivity to the headless server remained operational after transitioning to the wired connection.

**Result:** ✅ Successful

### Concepts Practiced

- Ethernet networking
- CAT5e cabling
- RJ45 connections
- IPv4 addressing
- DHCP
- Subnet masks
- Default gateways
- Network interfaces
- macOS network administration
- Wired network troubleshooting

**Phase 5 Status:** ✅ Completed

---

## 🚀 Future Improvements

The initial headless homelab infrastructure is operational. Future development will focus on expanding the environment for cybersecurity, networking, and system administration practice.

Planned improvements include:

- [ ] Configure SSH key-based authentication
- [ ] Harden SSH configuration
- [ ] Install Homebrew package management
- [ ] Deploy a container environment
- [ ] Deploy the first Linux-based lab workload
- [ ] Implement system and network monitoring
- [ ] Add security monitoring tools
- [ ] Expand network security testing
- [ ] Document additional cybersecurity experiments

### Long-Term Goal

The goal of BIS-Lab is to create an evolving cybersecurity homelab that can be used to practice real-world skills including system administration, networking, security monitoring, troubleshooting, and defensive security.

---

## 📌 Project Summary

This project established the foundation for the BIS cybersecurity homelab.

Through the project, I configured a dedicated system for headless operation, established network connectivity, enabled SSH remote administration, transitioned the server to wired Ethernet, and verified remote access from a separate administrative workstation.

The project provided hands-on experience with:

- TCP/IP networking
- Ethernet and DHCP
- ICMP connectivity testing
- SSH remote administration
- Headless server management
- macOS network configuration
- Command-line troubleshooting
- Basic security principles
- Technical documentation

BIS-Lab will continue to evolve as I develop additional cybersecurity, networking, system administration, and security monitoring skills.

---

**Project Status:** 🟢 Operational — Development Ongoing
