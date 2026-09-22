# Telecommunication Company Network Design

## Overview

This project presents an enterprise network design for a telecommunication company, simulated and implemented using Cisco Packet Tracer.

The network is designed to represent a multi-floor corporate environment with departmental network segmentation, centralized core switching, dynamic routing, server infrastructure, wireless connectivity, a DMZ, perimeter security, and cloud connectivity.

The network connects multiple departments across different floors while providing dedicated infrastructure for enterprise services and cloud resources.

---

## Network Architecture

The network follows a hierarchical enterprise network design consisting of:

- Core network
- Access-layer switches
- Departmental networks
- DMZ and server infrastructure
- Perimeter security zone
- Wireless network infrastructure
- Azure cloud infrastructure
- Multiple floors

The core switching layer provides connectivity between the different parts of the enterprise network, while access switches connect end devices belonging to individual departments.

---

## Departments

The network contains separate network segments for different organizational departments, including:

- HR
- Brand & Marketing
- Admin / Corporate
- IT Support
- Software Engineering
- Cloud Engineering

Each department contains its own end devices such as:

- Desktop PCs
- Laptops
- Printers
- Smartphones
- Other network-connected devices

Departmental separation is represented through VLAN-based network segmentation.

---

## Network Topology

The topology consists of multiple network layers and infrastructure zones.

### Core Network

A central Cisco core switch acts as an important aggregation point for the enterprise network.

The core switch connects to multiple access switches serving different floors and departmental networks.

### Access Network

Multiple Cisco Catalyst 2960 access switches are used to connect departmental devices.

The access switches provide connectivity for PCs, laptops, printers, smartphones, and other end devices.

### Multi-Floor Network

The topology represents multiple corporate floors, including:

- 4th Floor
- 5th Floor

Access switches on the different floors provide connectivity to the departments located on those floors.

---

## VLAN Segmentation

VLANs are used to logically separate different groups of devices within the enterprise network.

The Packet Tracer configuration contains VLAN-based segmentation, including VLAN 50 and VLAN 60 on the access-layer switches.

For example, the `CAIRO-ACCESS-SW3` switch contains ports assigned to VLAN 50 and VLAN 60.

This segmentation helps organize departmental traffic and separates devices into logical broadcast domains.

---

## Routing

### OSPF

Open Shortest Path First (OSPF) is used for dynamic routing within the network.

The core switch is configured with an OSPF process, and the Packet Tracer output shows an OSPF neighbor relationship reaching the `FULL` state.

Example observed OSPF status:

    OSPF Process 35
    Neighbor 1.1.3.3
    State: FULL

Using OSPF allows network devices to dynamically exchange routing information instead of relying entirely on manually configured static routes.

---

## EtherChannel / Port Channels

The network uses multiple Port-channel interfaces to provide aggregated links between network devices.

Port-channel interfaces are visible on the core and access switching infrastructure.

This provides a higher-capacity logical connection between switches and can improve link availability by combining multiple physical interfaces into a logical interface.

The exact EtherChannel negotiation protocol is not documented in this repository unless explicitly configured and verified in the Packet Tracer configuration.

---

## DMZ and Server Infrastructure

A dedicated DMZ is included in the network topology.

The DMZ contains several enterprise servers, including:

- DNS Server
- ERP Server
- Mail Server
- File Storage Server

The DMZ is separated from the internal corporate network through the perimeter/security infrastructure.

This design allows enterprise services to be placed in a dedicated network zone rather than directly inside the internal user network.

---

## Perimeter Security

The topology contains a perimeter security zone between the external network and the internal enterprise network.

A Cisco ASA 5506-X firewall is represented in the topology as the perimeter firewall.

The network is organized into:

- Outside Zone
- Perimeter / DMZ Zone
- Inside Zone

This provides a logical separation between external connectivity, publicly exposed services, and the internal corporate network.

---

## Wireless Network

Wireless networking infrastructure is included in the topology.

The wireless section contains:

- Cisco wireless gateway/controller infrastructure
- Wireless users
- Wi-Fi-connected devices
- Smartphones
- Laptops

The topology represents wireless connectivity as part of the overall enterprise network.

---

## Azure Cloud Connectivity

The project also models connectivity between the enterprise network and Microsoft Azure infrastructure.

The Azure section contains:

- Azure Cloud router
- Azure VM
- Azure VPN
- Azure Blob Storage

This demonstrates how enterprise infrastructure can be connected to cloud-based computing and storage resources.

---

## Network Devices

The topology contains several types of Cisco networking devices, including:

- Cisco routers
- Cisco Catalyst switches
- Cisco ASA firewall
- Wireless networking devices
- Servers
- PCs
- Laptops
- Smartphones
- Printers

---

## Technologies Used

- Cisco Packet Tracer
- VLAN
- OSPF
- EtherChannel / Port-channel
- Layer 2 Switching
- Layer 3 Routing
- Network Segmentation
- DMZ
- Firewall / Perimeter Security
- Wireless Networking
- Cloud Networking
- Microsoft Azure

---

## Project Objectives

The main objectives of this project were to:

1. Design an enterprise network for a telecommunication company.
2. Connect multiple departments across different floors.
3. Implement VLAN-based network segmentation.
4. Configure dynamic routing using OSPF.
5. Use aggregated switch links through Port-channels.
6. Separate enterprise servers using a DMZ architecture.
7. Model perimeter security using a firewall.
8. Provide wireless connectivity for enterprise users.
9. Integrate enterprise infrastructure with cloud resources.
10. Simulate and test the complete network using Cisco Packet Tracer.

---

## Network Testing

The network was simulated using Cisco Packet Tracer.

The topology was tested using Packet Tracer's simulation environment to observe network events and communication between network devices.

The project also includes evidence of an established OSPF neighbor relationship, with the OSPF neighbor reaching the `FULL` state.

---

## Project File

The main project file is:

    TELECOMMUNICATION_COMPANY_NETWORK.pkt

The `.pkt` file can be opened using Cisco Packet Tracer.

---

## How to Open the Project

1. Install Cisco Packet Tracer.
2. Clone or download this repository.
3. Open `TELECOMMUNICATION_COMPANY_NETWORK.pkt`.
4. Switch to Logical view to inspect the complete network topology.
5. Open individual routers and switches to inspect their configurations.
6. Use Simulation Mode to observe network communication and protocol events.

---

## Project Structure

    telecommunication-network-design/
    │
    ├── TELECOMMUNICATION_COMPANY_NETWORK.pkt
    └── README.md

---

## Author

Prithviraj K C

Computer Science and Engineering  
PES University, Bengaluru
