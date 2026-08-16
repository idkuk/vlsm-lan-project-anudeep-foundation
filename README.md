# LAN Network Project - Anudeep Foundation

## Overview
This project presents an enterprise-grade Local Area Network (LAN) architecture designed and simulated using **Cisco Packet Tracer** as part of the Anudeep Foundation training program[cite: 1]. 

The topology demonstrates efficient IP address management using **Variable Length Subnet Masking (VLSM)**, automated network configuration via **DHCP**, and secure inter-network communication using **static WAN routing** across two interconnected routers[cite: 1].

---

## Network Architecture & Specifications

### Key Highlights
* **VLSM Optimization**: Segmented a single `192.168.10.0/24` network into four optimized subnets to eliminate IP address wastage[cite: 1].
* **Dynamic IP Allocation**: Automated host configuration across Engineering, Sales, and Support departments using dedicated DHCP pools[cite: 1].
* **WAN Interconnection**: Established full end-to-end connectivity across two Cisco routers via static serial routing[cite: 1].

### Subnetting Breakdown
| Subnet Name | Network ID | Subnet Mask | Usable Range / Gateway | Max Hosts | Role |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **ENG_POOL** | `192.168.10.0` | `255.255.255.192` (/26) | `192.168.10.1` | 62 | Engineering LAN[cite: 1] |
| **SALES_POOL** | `192.168.10.64` | `255.255.255.224` (/27) | `192.168.10.65` | 30 | Sales LAN[cite: 1] |
| **SUPPORT_POOL** | `192.168.10.96` | `255.255.255.240` (/28) | `192.168.10.97` | 14 | Support LAN[cite: 1] |
| **WAN_LINK** | `192.168.10.112` | `255.255.255.252` (/30) | `192.168.10.113` - `.114` | 2 | Router-to-Router Link[cite: 1] |

---

## Verification & Test Results
* **Reachability**: 100% ICMP reachability across all endpoints (0% packet loss)[cite: 1].
* **Latency**: Average 0ms within local LANs and 13ms across the WAN link[cite: 1].

---

## How to Open & Test
1. Download or clone this repository.
2. Open the `.pkt` file in **Cisco Packet Tracer**.
3. Access any PC CLI and run `ping <destination-ip>` to verify communication.
