# HK_FABRIC

# Table of Contents
<!-- toc -->

- [Fabric Switches and Management IP](#fabric-switches-and-management-ip)
  - [Fabric Switches with inband Management IP](#fabric-switches-with-inband-management-ip)
- [Fabric Topology](#fabric-topology)
- [Fabric IP Allocation](#fabric-ip-allocation)
  - [Fabric Point-To-Point Links](#fabric-point-to-point-links)
  - [Point-To-Point Links Node Allocation](#point-to-point-links-node-allocation)
  - [Overlay Loopback Interfaces (BGP EVPN Peering)](#overlay-loopback-interfaces-bgp-evpn-peering)
  - [Loopback0 Interfaces Node Allocation](#loopback0-interfaces-node-allocation)
  - [VTEP Loopback VXLAN Tunnel Source Interfaces (Leafs Only)](#vtep-loopback-vxlan-tunnel-source-interfaces-leafs-only)
  - [VTEP Loopback Node allocation](#vtep-loopback-node-allocation)

<!-- toc -->
# Fabric Switches and Management IP

| POD | Type | Node | Management IP | Platform | Provisioned in CloudVision |
| --- | ---- | ---- | ------------- | -------- | -------------------------- |
| HK_FABRIC | l3leaf | HK-LEAF1A | 192.168.26.133/24 | vEOS-LAB | Provisioned |
| HK_FABRIC | l3leaf | HK-LEAF1B | 192.168.26.134/24 | vEOS-LAB | Provisioned |
| HK_FABRIC | l3leaf | HK-LEAF2A | 192.168.26.135/24 | vEOS-LAB | Provisioned |
| HK_FABRIC | l3leaf | HK-LEAF2B | 192.168.26.136/24 | vEOS-LAB | Provisioned |
| HK_FABRIC | spine | HK-SPINE1 | 192.168.26.131/24 | vEOS-LAB | Provisioned |
| HK_FABRIC | spine | HK-SPINE2 | 192.168.26.132/24 | vEOS-LAB | Provisioned |

> Provision status is based on Ansible inventory declaration and do not represent real status from CloudVision.

## Fabric Switches with inband Management IP
| POD | Type | Node | Management IP | Inband Interface |
| --- | ---- | ---- | ------------- | ---------------- |

# Fabric Topology

| Type | Node | Node Interface | Peer Type | Peer Node | Peer Interface |
| ---- | ---- | -------------- | --------- | ----------| -------------- |
| l3leaf | HK-LEAF1A | Ethernet1 | spine | HK-SPINE1 | Ethernet1 |
| l3leaf | HK-LEAF1A | Ethernet2 | spine | HK-SPINE2 | Ethernet1 |
| l3leaf | HK-LEAF1A | Ethernet3 | mlag_peer | HK-LEAF1B | Ethernet3 |
| l3leaf | HK-LEAF1A | Ethernet4 | mlag_peer | HK-LEAF1B | Ethernet4 |
| l3leaf | HK-LEAF1B | Ethernet1 | spine | HK-SPINE1 | Ethernet2 |
| l3leaf | HK-LEAF1B | Ethernet2 | spine | HK-SPINE2 | Ethernet2 |
| l3leaf | HK-LEAF2A | Ethernet1 | spine | HK-SPINE1 | Ethernet3 |
| l3leaf | HK-LEAF2A | Ethernet2 | spine | HK-SPINE2 | Ethernet3 |
| l3leaf | HK-LEAF2A | Ethernet3 | mlag_peer | HK-LEAF2B | Ethernet3 |
| l3leaf | HK-LEAF2A | Ethernet4 | mlag_peer | HK-LEAF2B | Ethernet4 |
| l3leaf | HK-LEAF2B | Ethernet1 | spine | HK-SPINE1 | Ethernet4 |
| l3leaf | HK-LEAF2B | Ethernet2 | spine | HK-SPINE2 | Ethernet4 |

# Fabric IP Allocation

## Fabric Point-To-Point Links

| P2P Summary | Available Addresses | Assigned addresses | Assigned Address % |
| ----------- | ------------------- | ------------------ | ------------------ |
| 172.31.255.0/24 | 256 | 16 | 6.25 % |

## Point-To-Point Links Node Allocation

| Node | Node Interface | Node IP Address | Peer Node | Peer Interface | Peer IP Address |
| ---- | -------------- | --------------- | --------- | -------------- | --------------- |
| HK-LEAF1A | Ethernet1 | 172.31.255.1/31 | HK-SPINE1 | Ethernet1 | 172.31.255.0/31 |
| HK-LEAF1A | Ethernet2 | 172.31.255.3/31 | HK-SPINE2 | Ethernet1 | 172.31.255.2/31 |
| HK-LEAF1B | Ethernet1 | 172.31.255.5/31 | HK-SPINE1 | Ethernet2 | 172.31.255.4/31 |
| HK-LEAF1B | Ethernet2 | 172.31.255.7/31 | HK-SPINE2 | Ethernet2 | 172.31.255.6/31 |
| HK-LEAF2A | Ethernet1 | 172.31.255.9/31 | HK-SPINE1 | Ethernet3 | 172.31.255.8/31 |
| HK-LEAF2A | Ethernet2 | 172.31.255.11/31 | HK-SPINE2 | Ethernet3 | 172.31.255.10/31 |
| HK-LEAF2B | Ethernet1 | 172.31.255.13/31 | HK-SPINE1 | Ethernet4 | 172.31.255.12/31 |
| HK-LEAF2B | Ethernet2 | 172.31.255.15/31 | HK-SPINE2 | Ethernet4 | 172.31.255.14/31 |

## Overlay Loopback Interfaces (BGP EVPN Peering)

| Overlay Loopback Summary | Available Addresses | Assigned addresses | Assigned Address % |
| ------------------------ | ------------------- | ------------------ | ------------------ |
| 192.168.255.0/24 | 256 | 6 | 2.35 % |

## Loopback0 Interfaces Node Allocation

| POD | Node | Loopback0 |
| --- | ---- | --------- |
| HK_FABRIC | HK-LEAF1A | 192.168.255.3/32 |
| HK_FABRIC | HK-LEAF1B | 192.168.255.4/32 |
| HK_FABRIC | HK-LEAF2A | 192.168.255.5/32 |
| HK_FABRIC | HK-LEAF2B | 192.168.255.6/32 |
| HK_FABRIC | HK-SPINE1 | 192.168.255.1/32 |
| HK_FABRIC | HK-SPINE2 | 192.168.255.2/32 |

## VTEP Loopback VXLAN Tunnel Source Interfaces (Leafs Only)

| VTEP Loopback Summary | Available Addresses | Assigned addresses | Assigned Address % |
| --------------------- | ------------------- | ------------------ | ------------------ |
| 192.168.254.0/24 | 256 | 4 | 1.57 % |

## VTEP Loopback Node allocation

| POD | Node | Loopback1 |
| --- | ---- | --------- |
| HK_FABRIC | HK-LEAF1A | 192.168.254.3/32 |
| HK_FABRIC | HK-LEAF1B | 192.168.254.3/32 |
| HK_FABRIC | HK-LEAF2A | 192.168.254.5/32 |
| HK_FABRIC | HK-LEAF2B | 192.168.254.5/32 |
