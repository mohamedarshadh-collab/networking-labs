# Lab 1: VLAN and Inter-VLAN Routing (Router-on-a-Stick)

Tool: Cisco Packet Tracer

## Objective
Create VLAN 10 (Sales) and VLAN 20 (IT) across two switches and
enable communication between them using router-on-a-stick.

## Topology
(topology screenshot, later add pannalaam)

## IP Addressing
| Device | VLAN | IP | Gateway |
|--------|------|----|---------|
| PC0 | 10 | 192.168.10.2 | 192.168.10.1 |
| PC2 | 10 | 192.168.10.3 | 192.168.10.1 |
| PC1 | 20 | 192.168.20.2 | 192.168.20.1 |
| PC3 | 20 | 192.168.20.3 | 192.168.20.1 |

## Key Configuration
- VLANs created on both switches, access ports assigned
- 802.1Q trunks between switches and to router
- Router subinterfaces Gi0/0.10 and Gi0/0.20 with dot1Q encapsulation

## Verification
- show vlan brief
- show interfaces trunk
- Ping within VLAN and between VLANs (screenshots)
