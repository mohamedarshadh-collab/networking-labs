# Lab 1: VLAN and Inter-VLAN Routing (Router-on-a-Stick)

Tool: Cisco Packet Tracer

## Objective
Create VLAN 10 (Sales) and VLAN 20 (IT) across two switches and
enable communication between them using router-on-a-stick.

## Topology
![Topology](topology.png)

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

### VLANs and trunk ports (Switch0)
![VLAN and trunk](vlan-trunk.png)

### Router subinterfaces
![Router subinterfaces](router-subinterfaces.png)

### Ping tests from PC0
Same VLAN (192.168.10.3) and inter-VLAN (192.168.20.2). The first inter-VLAN
request times out because of ARP resolution, the rest succeed. TTL=127 shows
the packets were routed through the router.

![Ping test](ping-test.png)
