# Design and Implementation of a Secure Campus Area Network System
# Case Study and Requirements
## Overview

This project presents a detailed and comprehensive network design for . The network infrastructure has been designed using Cisco Packet Tracer, ensuring a secure, scalable, and reliable system that supports the educational and administrative needs of the college.

# 1. Project Overview

Martin Luther King University operates two campuses located 100 miles apart in the United States, hosting diverse faculties including `Health Sciences`, `Business`, `Engineering` and `Art/Design`.To ensure seamless connectivity and technological cohesion, an integral component of the university is its Information Technology (IT) department situated at the main campus. The university's `IT Department` at the main campus manages a unified network connecting both campuses, supporting approximately 30,000 users. With user counts expected to double by 2025, the project emphasizes `scalability` and robust infrastructure.

# 2. Network Topology
The network employs a hierarchical model comprising core, distribution, and access layers to ensure scalability and redundancy. Key components include:

`Core Layer`: Cisco Catalyst 3850 switches for high-speed backbone connectivity.
`Distribution Layer`: Cisco ASA firewalls for security and Catalyst 2960 switches for local network aggregation.
`Access Layer`: Lightweight Access Points (LAPs) managed by Cisco Wireless LAN Controllers (WLCs) for seamless WiFi access.
`Server Farm (DMZ)`: Centralized servers (DHCP, DNS, FTP, WEB, Email, SMTP) housed in a secure DMZ at the main campus.

## Branch Campus:

Core Layer: Cisco Catalyst 3850 Switches
Distribution Layer: Cisco ASA Firewall, Catalyst 2960 Switches
Access Layer: Lightweight Access Points managed by Cisco WL
