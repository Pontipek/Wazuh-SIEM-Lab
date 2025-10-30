# Cybersecurity SIEM Lab with Wazuh

## Overview
This lab demonstrates how to set up and configure Wazuh, an open-source Security Information and Event Management (SIEM) platform. Wazuh provides real-time monitoring, intrusion detection, log analysis, and incident response capabilities for Linux and Windows environments. In this setup, Windows acts as the Wazuh Agent, Ubuntu as the Manager, and VMware/VirtualBox hosts the virtual environment.

## Lab Components
| Component | Role | Description |
|------------|------|-------------|
| **Ubuntu (VM)** | Wazuh Manager | Central management and analysis dashboard |
| **Windows (Host)** | Wazuh Agent | Collects and sends system logs to the manager |
| **VirtualBox** | Virtualization Platform | Runs Ubuntu in an isolated environment |
| **Wazuh** | SIEM Platform | Detects threats, analyzes logs, and visualizes data |

## 🗺️ System Diagram
                 ┌──────────────────────────────────┐
                 │          Ubuntu VM               │
                 │   Wazuh Manager & Dashboard      │
                 │          IP: 192.168.1.100       │
                 └───────────────┬──────────────────┘
                                 │
                     Host-Only / NAT Network
                                 │
                 ┌───────────────┴──────────────────┐
                 │           Windows Host           │
                 │        Wazuh Agent / Client      │
                 │          IP: 192.168.1.110       │
                 └──────────────────────────────────┘


                         🔁 Data Flow
────────────────────────────────────────────────────────────
 Windows Agent  ───▶  Sends logs & alerts  ───▶  Wazuh Manager
 Wazuh Manager  ───▶  Analyzes & displays results  ───▶  Dashboard
────────────────────────────────────────────────────────────

## ⚙️ Setup Steps
### Install Ubuntu on VirtualBox / VMware
1. Download Virtual Machine Software
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)  
- [VMware Workstation / Fusion](https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion)

2. Download Ubuntu ISO
- [Ubuntu Official Download](https://ubuntu.com/download)

3. Create a New Virtual Machine
**Settings:**
- **Name:** `Ubuntu-Wazuh-Manager`  
- **Type:** Linux  
- **Version:** Ubuntu (64-bit)  
- **Memory:** 4 GB  
- **Storage:** 20 GB+  

Mount the Ubuntu ISO and complete the installation.

**Video Tutorial:**  
- [Download Ubuntu on VirtualBox](https://www.youtube.com/watch?v=IOSEdXVmmpM)  
- [Download Ubuntu on VMware](https://www.youtube.com/watch?v=CNAmlDEzqKo)

### Install Wazuh Agent on Windows (Host)


### Install Wazuh Manageron Ubuntu (VM)

## Testing the Setup
   
## 🧾 Resources
- [Wazuh Official Documentation](https://documentation.wazuh.com)
- [Install Ubuntu on VirtualBox (Video)](https://www.youtube.com/watch?v=IOSEdXVmmpM)
- [VirtualBox Download Page](https://www.virtualbox.org/wiki/Downloads)
