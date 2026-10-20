# Secure Campus Area Network System (Cisco Packet Tracer)

Design and implementation of a hierarchical, secure campus network in Cisco Packet Tracer. The network combines Cisco ASA firewalls with Inside, Outside and DMZ zones, NAT and ACLs, OSPF routing, HSRP and EtherChannel for high availability, VLAN segmentation with inter-VLAN routing, a wireless LAN with controllers and access points, Active Directory based DHCP, telephony services, and SSH-secured remote management.

## Overview

A campus network must keep different user groups separate, stay available when a link or device fails, and protect internal resources from outside threats. This project builds that network in simulation using a hierarchical design and layers security, redundancy and wireless access on top of it.

## Features

- Hierarchical design: structured network layers for scalability and easier management.
- Cisco ASA firewalls: security zones for Inside, Outside and DMZ, with NAT and ACLs controlling traffic between them.
- OSPF routing: dynamic routing between network devices.
- High availability: HSRP for gateway redundancy and EtherChannel for link aggregation and redundancy.
- VLAN segmentation: separate broadcast domains for different user groups, with inter-VLAN routing.
- Wireless LAN: wireless LAN controllers and access points providing segregated Corporate, Employee and Guest Wi-Fi.
- Active Directory DHCP: centralized IP address assignment for clients.
- Telephony services: voice services running over the campus network.
- SSH management: encrypted remote management of network devices.

## Technologies and Concepts

| Area                 | Details                                                     |
|----------------------|-------------------------------------------------------------|
| Simulator            | Cisco Packet Tracer                                         |
| Perimeter security   | Cisco ASA firewalls, Inside / Outside / DMZ zones, NAT, ACLs|
| Routing              | OSPF                                                        |
| High availability    | HSRP, EtherChannel                                          |
| Layer 2 and 3        | VLANs, 802.1Q trunking, inter-VLAN routing                  |
| Wireless             | Wireless LAN controllers, access points, Corporate / Employee / Guest SSIDs |
| Services             | Active Directory, DHCP, telephony                           |
| Management           | SSH                                                         |

## How It Works

1. The network follows a hierarchical model, with access switches connecting end devices, a distribution layer aggregating them, and a core connecting to the firewalls.
2. VLANs separate user groups, and inter-VLAN routing allows controlled communication between them.
3. HSRP provides a redundant default gateway, and EtherChannel bundles links between switches so that a single link failure does not interrupt traffic.
4. OSPF advertises routes between the routers and the firewalls.
5. The Cisco ASA firewalls divide the network into Inside, Outside and DMZ zones. NAT translates internal addresses for outside access, and ACLs decide which traffic may pass between zones.
6. Wireless LAN controllers manage the access points and provide separate Wi-Fi networks for corporate, employee and guest users, so guests are kept apart from internal resources.
7. The Active Directory server provides DHCP, and telephony services support voice communication.
8. Administrators manage routers, switches and firewalls over SSH.

## Getting Started

1. Install Cisco Packet Tracer.
2. Open the project file (`.pkt`) from this repository.
3. Verify connectivity between VLANs, DHCP address assignment, OSPF neighbours and HSRP status.
4. Test NAT and access to the DMZ from the Outside zone, and confirm that ACLs block unintended traffic.
5. Connect wireless clients to the Corporate, Employee and Guest networks and check that they are segregated.
6. Test SSH access to the network devices from a management PC.

## Repository Structure

```
Campus-Network/
|-- README.md
`-- campus_network.pkt
```

## Future Scope

- Redundant ASA firewalls in failover mode
- VPN access for remote users and sites
- Network access control with 802.1X authentication
- Quality of service for voice traffic
- Network monitoring with SNMP and syslog
