# Design and Implementation of a Secure Campus Area Network System
# Case Study and Requirements
## Overview

This project presents a detailed and comprehensive network design for . The network infrastructure has been designed using Cisco Packet Tracer, ensuring a secure, scalable, and reliable system that supports the educational and administrative needs of the college.

# 1. Project Overview

Martin Luther King University operates two campuses located 100 miles apart in the United States, hosting diverse faculties including `Health Sciences`, `Business`, `Engineering` and `Art/Design`.To ensure seamless connectivity and technological cohesion, an integral component of the university is its Information Technology (IT) department situated at the main campus. The university's `IT Department` at the main campus manages a unified network connecting both campuses, supporting approximately 30,000 users. With user counts expected to double by 2025, the project emphasizes `scalability` and robust infrastructure.

# 2. Network Topology
The network employs a hierarchical model comprising core, distribution, and access layers to ensure scalability and redundancy. Key components include:
## main campus
`Core Layer`: Cisco Catalyst 3850 switches for high-speed backbone connectivity.

`Distribution Layer`: Cisco ASA firewalls for security and Catalyst 2960 switches for local network aggregation.

`Access Layer`: Lightweight Access Points (LAPs) managed by Cisco Wireless LAN Controllers (WLCs) for seamless WiFi access.

`Server Farm (DMZ)`: Centralized servers (DHCP, DNS, FTP, WEB, Email, SMTP) housed in a secure DMZ at the main campus.

## Branch Campus:

`Core Layer`: Cisco Catalyst 3850 Switches

`Distribution Layer`: Cisco ASA Firewall, Catalyst 2960 Switches

`Access Layer`: Lightweight Access Points managed by Cisco WLC

# 3. IP Addressing Scheme
## Main Campus:

`MANAGEMENT`: 192.168.10.0/24

`LAN`:  172.16.0.0/16

`WLAN`: 10.10.0.0/16

`DMZ`: 10.20.20.0/27

## Branch Campus:


`LAN`:  172.17.0.0/16

`WLAN`: 10.11.0.0/16

# 4. Technologies Implemented

## Design Tool: Cisco Packet Tracer

## Hierarchical Design: Incorporates redundancy for enhanced network resilience.

## ISPs: Connectivity to Airtel ISP Router within the network infrastructure.

## WLC: Each department is equipped with a Wireless Access Point (WAP) to provide WiFi access to employees, corporate users, external auditors, and guests, all centrally managed by a Wireless LAN Controller (WLC).

`VoIP`: Deployed IP phones in each department to support Voice over IP (VoIP) communication.

`VLAN`: VLANs with IDs 10 for Management, 20 for LAN, 50 for WLAN, and 199 for Blackhole (unused ports).

EtherChannel: Implemented LACP for EtherChannel configuration, enhancing link aggregation efficiency.
STP PortFast and BPDUguard: Configured to expedite port transitions from blocking to forwarding states.
Subnetting: Utilized to allocate the appropriate number of IP addresses to each network group.
Basic Settings: Configured hostnames, console passwords, enable passwords, banner messages, password encryption, and disabled IP domain lookup.
Inter-VLAN Routing: Enabled devices in all departments to communicate with one another by configuring the respective multilayer switch for inter-VLAN routing.
Core Switch: Assigned IP addresses to Multilayer switches to enable both routing and switching functionalities.
DHCP Server: Ensured that all devices in the network obtain IP addresses dynamically from Active Directory (AD) servers located at the server farm site.
HSRP: Implemented high-availability router protocols such as HSRP to achieve redundancy, load balancing, and failover capabilities.
Static Addressing: Allocated static IP addresses to devices located in the server room.
Routing Protocol: Utilized OSPF as the routing protocol to advertise routes on the firewall, routers, and multilayer switches.
Standard ACL for SSH: Established a simple standard ACL on the VTY line to permit remote administrative tasks via SSH only for the Senior Network Security Engineer PC.
Cisco ASA Firewall: Configured default static routes, basic settings, security levels, zones, and policies to define access control and resource utilization within the network.
