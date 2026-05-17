# Basic-Switch-Network-Implementation-project-01
# Basic Switch Network - Cisco Packet Tracer

A fundamental LAN switching project built with Cisco Packet Tracer. This project demonstrates core networking concepts including Ethernet switching, basic switch configuration, IP addressing, and network connectivity.

![Packet Tracer Logo](https://img.shields.io/badge/Cisco-Packet%20Tracer-blue)
![Project Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📋 Project Overview

This project implements a **star topology LAN** using a Layer 2 Switch and multiple end devices. It serves as an excellent foundational project for networking students and beginners to showcase their understanding of switched networks.

### Objectives
- Understand Layer 2 switching and MAC address learning
- Configure basic switch management settings
- Implement proper IP addressing scheme
- Verify end-to-end connectivity

## 🖼️ Network Topology

**Topology Type:** Star Topology

- **Central Device**: Cisco 2960 Switch (`S1`)
- **End Devices**: 4 PCs (PC1 to PC4)
- **Connection Type**: Straight-through Ethernet cables

### Network Topology Table

| Device | Type         | Model     | Ports Used      | Connected To    | Purpose              |
|--------|--------------|-----------|-----------------|-----------------|----------------------|
| S1     | Switch       | 2960      | Fa0/1 - Fa0/4   | PC1 - PC4       | Central Switching    |
| PC1    | PC           | PC-PT     | FastEthernet    | S1 Fa0/1        | Workstation          |
| PC2    | PC           | PC-PT     | FastEthernet    | S1 Fa0/2        | Workstation          |
| PC3    | PC           | PC-PT     | FastEthernet    | S1 Fa0/3        | Workstation          |
| PC4    | PC           | PC-PT     | FastEthernet    | S1 Fa0/4        | Workstation          |

## 🔢 IP Addressing Table

| Device | Interface      | IP Address       | Subnet Mask      | Default Gateway  | VLAN |
|--------|----------------|------------------|------------------|------------------|------|
| S1     | VLAN 1 (SVI)   | 192.168.1.1     | 255.255.255.0   | -                | 1    |
| PC1    | NIC            | 192.168.1.10    | 255.255.255.0   | 192.168.1.1      | 1    |
| PC2    | NIC            | 192.168.1.11    | 255.255.255.0   | 192.168.1.1      | 1    |
| PC3    | NIC            | 192.168.1.12    | 255.255.255.0   | 192.168.1.1      | 1    |
| PC4    | NIC            | 192.168.1.13    | 255.255.255.0   | 192.168.1.1      | 1    |

**Network:** `192.168.1.0/24`

## ⚙️ Features & Configurations

### Switch Configuration (S1)
- Hostname and MOTD Banner
- Enable secret & line passwords
- Management IP on VLAN 1
- Interface descriptions
- Basic port security (optional)
- SSH & Telnet configuration

### Verification Commands Used
```bash
show running-config
show ip interface brief
show mac address-table
show vlan brief
ping
