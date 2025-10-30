# Cybersecurity SIEM Lab with Wazuh

## Overview
This lab demonstrates how to set up and configure Wazuh, an open-source Security Information and Event Management (SIEM) platform. Wazuh provides real-time monitoring, intrusion detection, log analysis, and incident response capabilities for Linux and Windows environments. In this setup, Windows acts as the Wazuh Agent, Ubuntu as the Manager, and VMware/VirtualBox hosts the virtual environment.

## Lab Components
| Component | Role | Description |
|------------|------|-------------|
| **Ubuntu (VM)** | Wazuh Manager | Central management and analysis dashboard |
| **Windows (Host)** | Wazuh Agent | Collects and sends system logs to the manager |
| **VirtualBox/VMware** | Virtualization Platform | Runs Ubuntu in an isolated environment |
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

                     Windows Agent  ───▶  Sends logs & alerts  ───▶  Wazuh Manager


                     Wazuh Manager  ───▶  Analyzes & displays results  ───▶  Dashboard


## ⚙️ Setup Steps
### Install Ubuntu on VirtualBox / VMware
1. Download Virtual Machine Software
- <a href="https://www.virtualbox.org/wiki/Downloads" target="_blank" rel="noopener noreferrer">VirtualBox</a>  
- <a href="https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion" target="_blank" rel="noopener noreferrer">VMware Workstation / Fusion</a>

2. Download Ubuntu ISO
- <a href="https://ubuntu.com/download" target="_blank" rel="noopener noreferrer">Ubuntu Official Download</a>

3. Create a New Virtual Machine
**Settings:**
- **Name:** `Ubuntu-Wazuh-Manager`  
- **Type:** Linux  
- **Version:** Ubuntu (64-bit)  
- **Memory:** 4 GB  
- **Storage:** 20 GB+  

Mount the Ubuntu ISO and complete the installation.

**Video Tutorial:**  
- <a href="https://www.youtube.com/watch?v=IOSEdXVmmpM" target="_blank" rel="noopener noreferrer">Download Ubuntu on VirtualBox</a>  
- <a href="https://www.youtube.com/watch?v=CNAmlDEzqKo" target="_blank" rel="noopener noreferrer">Download Ubuntu on VMware</a>


### Install Wazuh Agent on Windows (Host)


### Install Wazuh Manageron Ubuntu (VM)

## Testing the Setup

## Troubleshoot
   
## 🧾 Resources
- <a href="https://documentation.wazuh.com" target="_blank" rel="noopener noreferrer">Wazuh Official Documentation</a>  
- <a href="https://www.youtube.com/watch?v=IOSEdXVmmpM" target="_blank" rel="noopener noreferrer">Install Ubuntu on VirtualBox (Video)</a>  
- <a href="https://www.virtualbox.org/wiki/Downloads" target="_blank" rel="noopener noreferrer">VirtualBox Download Page</a>

