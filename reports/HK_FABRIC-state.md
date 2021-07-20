
# Validate State Report

**Table of Contents:**

- [Validate State Report](validate-state-report)
  - [Test Results Summary](#test-results-summary)
  - [Failed Test Results Summary](#failed-test-results-summary)
  - [All Test Results](#all-test-results)

## Test Results Summary

### Summary Totals

| Total Tests | Total Tests Passed | Total Tests Failed |
| ----------- | ------------------ | ------------------ |
| 261 | 244 | 17 |

### Summary Totals Devices Under Tests

| DUT | Total Tests | Tests Passed | Tests Failed | Categories Failed |
| --- | ----------- | ------------ | ------------ | ----------------- |
| HK-LEAF1A |  45 | 43 | 2 | NTP, Interface State |
| HK-LEAF1B |  40 | 39 | 1 | NTP |
| HK-LEAF2A |  57 | 54 | 3 | NTP, Interface State |
| HK-LEAF2B |  57 | 51 | 6 | NTP, Interface State, LLDP Topology, IP Reachability, BGP |
| HK-SPINE1 |  31 | 30 | 1 | NTP |
| HK-SPINE2 |  31 | 27 | 4 | NTP, LLDP Topology, IP Reachability, BGP |

### Summary Totals Per Category

| Test Category | Total Tests | Tests Passed | Tests Failed |
| ------------- | ----------- | ------------ | ------------ |
| NTP |  6 | 0 | 6 |
| Interface State |  113 | 108 | 5 |
| LLDP Topology |  24 | 22 | 2 |
| MLAG |  4 | 4 | 0 |
| IP Reachability |  16 | 14 | 2 |
| BGP |  42 | 40 | 2 |
| Routing Table |  32 | 32 | 0 |
| Loopback0 Reachability |  24 | 24 | 0 |

## Failed Test Results Summary

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 1 | HK-LEAF1A | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 2 | HK-LEAF1B | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 3 | HK-LEAF2A | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 4 | HK-LEAF2B | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 5 | HK-SPINE1 | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 6 | HK-SPINE2 | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 40 | HK-LEAF1A | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel7 - server01_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 43 | HK-LEAF2A | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel10 - server01_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 44 | HK-LEAF2A | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel11 - server02_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 46 | HK-LEAF2B | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel10 - server01_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 47 | HK-LEAF2B | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel11 - server02_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 135 | HK-LEAF2B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet2 - remote: HK-SPINE2_Ethernet4 | FAIL | remote: Interface Down - N/A |
| 143 | HK-SPINE2 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet4 - remote: HK-LEAF2B_Ethernet2 | FAIL | remote: Interface Down - N/A |
| 155 | HK-LEAF2B | IP Reachability | ip reachability test p2p links | Source: HK-LEAF2B_Ethernet2 - Destination: HK-SPINE2_Ethernet4 | FAIL | 100% packet loss |
| 163 | HK-SPINE2 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE2_Ethernet4 - Destination: HK-LEAF2B_Ethernet2 | FAIL | 100% packet loss |
| 181 | HK-LEAF2B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.14 | FAIL | Session state "Connect" |
| 189 | HK-SPINE2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.15 | FAIL | Session state "Connect" |

## All Test Results

| Test ID | Node | Test Category | Test Description | Test | Test Result | Failure Reason |
| ------- | ---- | ------------- | ---------------- | ---- | ----------- | -------------- |
| 1 | HK-LEAF1A | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 2 | HK-LEAF1B | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 3 | HK-LEAF2A | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 4 | HK-LEAF2B | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 5 | HK-SPINE1 | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 6 | HK-SPINE2 | NTP | Synchronised with NTP server | NTP | FAIL | not synchronised to NTP server |
| 7 | HK-LEAF1A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet3 - MLAG_PEER_HK-LEAF1B_Ethernet3 | PASS |  |
| 8 | HK-LEAF1A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet4 - MLAG_PEER_HK-LEAF1B_Ethernet4 | PASS |  |
| 9 | HK-LEAF1A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_HK-SPINE1_Ethernet1 | PASS |  |
| 10 | HK-LEAF1A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_HK-SPINE2_Ethernet1 | PASS |  |
| 11 | HK-LEAF1A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet5 - server01_Eth1 | PASS |  |
| 12 | HK-LEAF1A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet7 - server01_Eth4 | PASS |  |
| 13 | HK-LEAF1A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet8 - server01_Eth5 | PASS |  |
| 14 | HK-LEAF1A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet6 - server02_Eth1 | PASS |  |
| 15 | HK-LEAF1B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet3 - MLAG_PEER_HK-LEAF1A_Ethernet3 | PASS |  |
| 16 | HK-LEAF1B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet4 - MLAG_PEER_HK-LEAF1A_Ethernet4 | PASS |  |
| 17 | HK-LEAF1B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_HK-SPINE1_Ethernet2 | PASS |  |
| 18 | HK-LEAF1B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_HK-SPINE2_Ethernet2 | PASS |  |
| 19 | HK-LEAF2A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet3 - MLAG_PEER_HK-LEAF2B_Ethernet3 | PASS |  |
| 20 | HK-LEAF2A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet4 - MLAG_PEER_HK-LEAF2B_Ethernet4 | PASS |  |
| 21 | HK-LEAF2A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_HK-SPINE1_Ethernet3 | PASS |  |
| 22 | HK-LEAF2A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_HK-SPINE2_Ethernet3 | PASS |  |
| 23 | HK-LEAF2A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet10 - server01_Eth2 | PASS |  |
| 24 | HK-LEAF2A | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet11 - server02_Eth2 | PASS |  |
| 25 | HK-LEAF2B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet3 - MLAG_PEER_HK-LEAF2A_Ethernet3 | PASS |  |
| 26 | HK-LEAF2B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet4 - MLAG_PEER_HK-LEAF2A_Ethernet4 | PASS |  |
| 27 | HK-LEAF2B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_HK-SPINE1_Ethernet4 | PASS |  |
| 28 | HK-LEAF2B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_HK-SPINE2_Ethernet4 | PASS |  |
| 29 | HK-LEAF2B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet10 - server01_Eth3 | PASS |  |
| 30 | HK-LEAF2B | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet11 - server02_Eth3 | PASS |  |
| 31 | HK-SPINE1 | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_HK-LEAF1A_Ethernet1 | PASS |  |
| 32 | HK-SPINE1 | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_HK-LEAF1B_Ethernet1 | PASS |  |
| 33 | HK-SPINE1 | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_HK-LEAF2A_Ethernet1 | PASS |  |
| 34 | HK-SPINE1 | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_HK-LEAF2B_Ethernet1 | PASS |  |
| 35 | HK-SPINE2 | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet1 - P2P_LINK_TO_HK-LEAF1A_Ethernet2 | PASS |  |
| 36 | HK-SPINE2 | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet2 - P2P_LINK_TO_HK-LEAF1B_Ethernet2 | PASS |  |
| 37 | HK-SPINE2 | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet3 - P2P_LINK_TO_HK-LEAF2A_Ethernet2 | PASS |  |
| 38 | HK-SPINE2 | Interface State | Ethernet Interface Status & Line Protocol == "up" | Ethernet4 - P2P_LINK_TO_HK-LEAF2B_Ethernet2 | PASS |  |
| 39 | HK-LEAF1A | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel3 - MLAG_PEER_HK-LEAF1B_Po3 | PASS |  |
| 40 | HK-LEAF1A | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel7 - server01_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 41 | HK-LEAF1B | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel3 - MLAG_PEER_HK-LEAF1A_Po3 | PASS |  |
| 42 | HK-LEAF2A | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel3 - MLAG_PEER_HK-LEAF2B_Po3 | PASS |  |
| 43 | HK-LEAF2A | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel10 - server01_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 44 | HK-LEAF2A | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel11 - server02_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 45 | HK-LEAF2B | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel3 - MLAG_PEER_HK-LEAF2A_Po3 | PASS |  |
| 46 | HK-LEAF2B | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel10 - server01_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 47 | HK-LEAF2B | Interface State | Port-Channel Interface Status & Line Protocol == "up" | Port-Channel11 - server02_PortChanne1 | FAIL | interface status: down - line protocol status: lowerLayerDown |
| 48 | HK-LEAF1A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS |  |
| 49 | HK-LEAF1A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS |  |
| 50 | HK-LEAF1A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan130 - Tenant_A_APP_Zone_1 | PASS |  |
| 51 | HK-LEAF1A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan131 - Tenant_A_APP_Zone_2 | PASS |  |
| 52 | HK-LEAF1A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3011 - MLAG_PEER_L3_iBGP: vrf Tenant_A_APP_Zone | PASS |  |
| 53 | HK-LEAF1A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan120 - Tenant_A_WEB_Zone_1 | PASS |  |
| 54 | HK-LEAF1A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan121 - Tenant_A_WEBZone_2 | PASS |  |
| 55 | HK-LEAF1A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3010 - MLAG_PEER_L3_iBGP: vrf Tenant_A_WEB_Zone | PASS |  |
| 56 | HK-LEAF1B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS |  |
| 57 | HK-LEAF1B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS |  |
| 58 | HK-LEAF1B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan130 - Tenant_A_APP_Zone_1 | PASS |  |
| 59 | HK-LEAF1B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan131 - Tenant_A_APP_Zone_2 | PASS |  |
| 60 | HK-LEAF1B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3011 - MLAG_PEER_L3_iBGP: vrf Tenant_A_APP_Zone | PASS |  |
| 61 | HK-LEAF1B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan120 - Tenant_A_WEB_Zone_1 | PASS |  |
| 62 | HK-LEAF1B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan121 - Tenant_A_WEBZone_2 | PASS |  |
| 63 | HK-LEAF1B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3010 - MLAG_PEER_L3_iBGP: vrf Tenant_A_WEB_Zone | PASS |  |
| 64 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS |  |
| 65 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS |  |
| 66 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan130 - Tenant_A_APP_Zone_1 | PASS |  |
| 67 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan131 - Tenant_A_APP_Zone_2 | PASS |  |
| 68 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3011 - MLAG_PEER_L3_iBGP: vrf Tenant_A_APP_Zone | PASS |  |
| 69 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan140 - Tenant_A_DB_BZone_1 | PASS |  |
| 70 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan141 - Tenant_A_DB_Zone_2 | PASS |  |
| 71 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3012 - MLAG_PEER_L3_iBGP: vrf Tenant_A_DB_Zone | PASS |  |
| 72 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan110 - Tenant_A_OP_Zone_1 | PASS |  |
| 73 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan111 - Tenant_A_OP_Zone_2 | PASS |  |
| 74 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone | PASS |  |
| 75 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan120 - Tenant_A_WEB_Zone_1 | PASS |  |
| 76 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan121 - Tenant_A_WEBZone_2 | PASS |  |
| 77 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3010 - MLAG_PEER_L3_iBGP: vrf Tenant_A_WEB_Zone | PASS |  |
| 78 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan210 - Tenant_B_OP_Zone_1 | PASS |  |
| 79 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan211 - Tenant_B_OP_Zone_2 | PASS |  |
| 80 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3019 - MLAG_PEER_L3_iBGP: vrf Tenant_B_OP_Zone | PASS |  |
| 81 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan310 - Tenant_C_OP_Zone_1 | PASS |  |
| 82 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan311 - Tenant_C_OP_Zone_2 | PASS |  |
| 83 | HK-LEAF2A | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3029 - MLAG_PEER_L3_iBGP: vrf Tenant_C_OP_Zone | PASS |  |
| 84 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4093 - MLAG_PEER_L3_PEERING | PASS |  |
| 85 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan4094 - MLAG_PEER | PASS |  |
| 86 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan130 - Tenant_A_APP_Zone_1 | PASS |  |
| 87 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan131 - Tenant_A_APP_Zone_2 | PASS |  |
| 88 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3011 - MLAG_PEER_L3_iBGP: vrf Tenant_A_APP_Zone | PASS |  |
| 89 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan140 - Tenant_A_DB_BZone_1 | PASS |  |
| 90 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan141 - Tenant_A_DB_Zone_2 | PASS |  |
| 91 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3012 - MLAG_PEER_L3_iBGP: vrf Tenant_A_DB_Zone | PASS |  |
| 92 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan110 - Tenant_A_OP_Zone_1 | PASS |  |
| 93 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan111 - Tenant_A_OP_Zone_2 | PASS |  |
| 94 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3009 - MLAG_PEER_L3_iBGP: vrf Tenant_A_OP_Zone | PASS |  |
| 95 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan120 - Tenant_A_WEB_Zone_1 | PASS |  |
| 96 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan121 - Tenant_A_WEBZone_2 | PASS |  |
| 97 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3010 - MLAG_PEER_L3_iBGP: vrf Tenant_A_WEB_Zone | PASS |  |
| 98 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan210 - Tenant_B_OP_Zone_1 | PASS |  |
| 99 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan211 - Tenant_B_OP_Zone_2 | PASS |  |
| 100 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3019 - MLAG_PEER_L3_iBGP: vrf Tenant_B_OP_Zone | PASS |  |
| 101 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan310 - Tenant_C_OP_Zone_1 | PASS |  |
| 102 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan311 - Tenant_C_OP_Zone_2 | PASS |  |
| 103 | HK-LEAF2B | Interface State | Vlan Interface Status & Line Protocol == "up" | Vlan3029 - MLAG_PEER_L3_iBGP: vrf Tenant_C_OP_Zone | PASS |  |
| 104 | HK-LEAF1A | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS |  |
| 105 | HK-LEAF1B | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS |  |
| 106 | HK-LEAF2A | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS |  |
| 107 | HK-LEAF2B | Interface State | Vxlan Interface Status & Line Protocol == "up" | Vxlan1 | PASS |  |
| 108 | HK-LEAF1A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS |  |
| 109 | HK-LEAF1A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS |  |
| 110 | HK-LEAF1B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS |  |
| 111 | HK-LEAF1B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS |  |
| 112 | HK-LEAF2A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS |  |
| 113 | HK-LEAF2A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS |  |
| 114 | HK-LEAF2A | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback100 - Tenant_A_OP_Zone_VTEP_DIAGNOSTICS | PASS |  |
| 115 | HK-LEAF2B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS |  |
| 116 | HK-LEAF2B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback1 - VTEP_VXLAN_Tunnel_Source | PASS |  |
| 117 | HK-LEAF2B | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback100 - Tenant_A_OP_Zone_VTEP_DIAGNOSTICS | PASS |  |
| 118 | HK-SPINE1 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS |  |
| 119 | HK-SPINE2 | Interface State | Loopback Interface Status & Line Protocol == "up" | Loopback0 - EVPN_Overlay_Peering | PASS |  |
| 120 | HK-LEAF1A | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet3 - remote: HK-LEAF1B_Ethernet3 | PASS |  |
| 121 | HK-LEAF1A | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet4 - remote: HK-LEAF1B_Ethernet4 | PASS |  |
| 122 | HK-LEAF1A | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet1 - remote: HK-SPINE1_Ethernet1 | PASS |  |
| 123 | HK-LEAF1A | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet2 - remote: HK-SPINE2_Ethernet1 | PASS |  |
| 124 | HK-LEAF1B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet3 - remote: HK-LEAF1A_Ethernet3 | PASS |  |
| 125 | HK-LEAF1B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet4 - remote: HK-LEAF1A_Ethernet4 | PASS |  |
| 126 | HK-LEAF1B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet1 - remote: HK-SPINE1_Ethernet2 | PASS |  |
| 127 | HK-LEAF1B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet2 - remote: HK-SPINE2_Ethernet2 | PASS |  |
| 128 | HK-LEAF2A | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet3 - remote: HK-LEAF2B_Ethernet3 | PASS |  |
| 129 | HK-LEAF2A | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet4 - remote: HK-LEAF2B_Ethernet4 | PASS |  |
| 130 | HK-LEAF2A | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet1 - remote: HK-SPINE1_Ethernet3 | PASS |  |
| 131 | HK-LEAF2A | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet2 - remote: HK-SPINE2_Ethernet3 | PASS |  |
| 132 | HK-LEAF2B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet3 - remote: HK-LEAF2A_Ethernet3 | PASS |  |
| 133 | HK-LEAF2B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet4 - remote: HK-LEAF2A_Ethernet4 | PASS |  |
| 134 | HK-LEAF2B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet1 - remote: HK-SPINE1_Ethernet4 | PASS |  |
| 135 | HK-LEAF2B | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet2 - remote: HK-SPINE2_Ethernet4 | FAIL | remote: Interface Down - N/A |
| 136 | HK-SPINE1 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet1 - remote: HK-LEAF1A_Ethernet1 | PASS |  |
| 137 | HK-SPINE1 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet2 - remote: HK-LEAF1B_Ethernet1 | PASS |  |
| 138 | HK-SPINE1 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet3 - remote: HK-LEAF2A_Ethernet1 | PASS |  |
| 139 | HK-SPINE1 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet4 - remote: HK-LEAF2B_Ethernet1 | PASS |  |
| 140 | HK-SPINE2 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet1 - remote: HK-LEAF1A_Ethernet2 | PASS |  |
| 141 | HK-SPINE2 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet2 - remote: HK-LEAF1B_Ethernet2 | PASS |  |
| 142 | HK-SPINE2 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet3 - remote: HK-LEAF2A_Ethernet2 | PASS |  |
| 143 | HK-SPINE2 | LLDP Topology | lldp topology - validate peer and interface | local: Ethernet4 - remote: HK-LEAF2B_Ethernet2 | FAIL | remote: Interface Down - N/A |
| 144 | HK-LEAF1A | MLAG | MLAG State active & Status connected | MLAG | PASS |  |
| 145 | HK-LEAF1B | MLAG | MLAG State active & Status connected | MLAG | PASS |  |
| 146 | HK-LEAF2A | MLAG | MLAG State active & Status connected | MLAG | PASS |  |
| 147 | HK-LEAF2B | MLAG | MLAG State active & Status connected | MLAG | PASS |  |
| 148 | HK-LEAF1A | IP Reachability | ip reachability test p2p links | Source: HK-LEAF1A_Ethernet1 - Destination: HK-SPINE1_Ethernet1 | PASS |  |
| 149 | HK-LEAF1A | IP Reachability | ip reachability test p2p links | Source: HK-LEAF1A_Ethernet2 - Destination: HK-SPINE2_Ethernet1 | PASS |  |
| 150 | HK-LEAF1B | IP Reachability | ip reachability test p2p links | Source: HK-LEAF1B_Ethernet1 - Destination: HK-SPINE1_Ethernet2 | PASS |  |
| 151 | HK-LEAF1B | IP Reachability | ip reachability test p2p links | Source: HK-LEAF1B_Ethernet2 - Destination: HK-SPINE2_Ethernet2 | PASS |  |
| 152 | HK-LEAF2A | IP Reachability | ip reachability test p2p links | Source: HK-LEAF2A_Ethernet1 - Destination: HK-SPINE1_Ethernet3 | PASS |  |
| 153 | HK-LEAF2A | IP Reachability | ip reachability test p2p links | Source: HK-LEAF2A_Ethernet2 - Destination: HK-SPINE2_Ethernet3 | PASS |  |
| 154 | HK-LEAF2B | IP Reachability | ip reachability test p2p links | Source: HK-LEAF2B_Ethernet1 - Destination: HK-SPINE1_Ethernet4 | PASS |  |
| 155 | HK-LEAF2B | IP Reachability | ip reachability test p2p links | Source: HK-LEAF2B_Ethernet2 - Destination: HK-SPINE2_Ethernet4 | FAIL | 100% packet loss |
| 156 | HK-SPINE1 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE1_Ethernet1 - Destination: HK-LEAF1A_Ethernet1 | PASS |  |
| 157 | HK-SPINE1 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE1_Ethernet2 - Destination: HK-LEAF1B_Ethernet1 | PASS |  |
| 158 | HK-SPINE1 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE1_Ethernet3 - Destination: HK-LEAF2A_Ethernet1 | PASS |  |
| 159 | HK-SPINE1 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE1_Ethernet4 - Destination: HK-LEAF2B_Ethernet1 | PASS |  |
| 160 | HK-SPINE2 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE2_Ethernet1 - Destination: HK-LEAF1A_Ethernet2 | PASS |  |
| 161 | HK-SPINE2 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE2_Ethernet2 - Destination: HK-LEAF1B_Ethernet2 | PASS |  |
| 162 | HK-SPINE2 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE2_Ethernet3 - Destination: HK-LEAF2A_Ethernet2 | PASS |  |
| 163 | HK-SPINE2 | IP Reachability | ip reachability test p2p links | Source: HK-SPINE2_Ethernet4 - Destination: HK-LEAF2B_Ethernet2 | FAIL | 100% packet loss |
| 164 | HK-LEAF1A | BGP | ArBGP is configured and operating | ArBGP | PASS |  |
| 165 | HK-LEAF1B | BGP | ArBGP is configured and operating | ArBGP | PASS |  |
| 166 | HK-LEAF2A | BGP | ArBGP is configured and operating | ArBGP | PASS |  |
| 167 | HK-LEAF2B | BGP | ArBGP is configured and operating | ArBGP | PASS |  |
| 168 | HK-SPINE1 | BGP | ArBGP is configured and operating | ArBGP | PASS |  |
| 169 | HK-SPINE2 | BGP | ArBGP is configured and operating | ArBGP | PASS |  |
| 170 | HK-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.1 | PASS |  |
| 171 | HK-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.0 | PASS |  |
| 172 | HK-LEAF1A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.2 | PASS |  |
| 173 | HK-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.0 | PASS |  |
| 174 | HK-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.4 | PASS |  |
| 175 | HK-LEAF1B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.6 | PASS |  |
| 176 | HK-LEAF2A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.5 | PASS |  |
| 177 | HK-LEAF2A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.8 | PASS |  |
| 178 | HK-LEAF2A | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.10 | PASS |  |
| 179 | HK-LEAF2B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 10.255.251.4 | PASS |  |
| 180 | HK-LEAF2B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.12 | PASS |  |
| 181 | HK-LEAF2B | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.14 | FAIL | Session state "Connect" |
| 182 | HK-SPINE1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.1 | PASS |  |
| 183 | HK-SPINE1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.5 | PASS |  |
| 184 | HK-SPINE1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.9 | PASS |  |
| 185 | HK-SPINE1 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.13 | PASS |  |
| 186 | HK-SPINE2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.3 | PASS |  |
| 187 | HK-SPINE2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.7 | PASS |  |
| 188 | HK-SPINE2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.11 | PASS |  |
| 189 | HK-SPINE2 | BGP | ip bgp peer state established (ipv4) | bgp_neighbor: 172.31.255.15 | FAIL | Session state "Connect" |
| 190 | HK-LEAF1A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.1 | PASS |  |
| 191 | HK-LEAF1A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.2 | PASS |  |
| 192 | HK-LEAF1B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.1 | PASS |  |
| 193 | HK-LEAF1B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.2 | PASS |  |
| 194 | HK-LEAF2A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.1 | PASS |  |
| 195 | HK-LEAF2A | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.2 | PASS |  |
| 196 | HK-LEAF2B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.1 | PASS |  |
| 197 | HK-LEAF2B | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.2 | PASS |  |
| 198 | HK-SPINE1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.3 | PASS |  |
| 199 | HK-SPINE1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.4 | PASS |  |
| 200 | HK-SPINE1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.5 | PASS |  |
| 201 | HK-SPINE1 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.6 | PASS |  |
| 202 | HK-SPINE2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.3 | PASS |  |
| 203 | HK-SPINE2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.4 | PASS |  |
| 204 | HK-SPINE2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.5 | PASS |  |
| 205 | HK-SPINE2 | BGP | bgp evpn peer state established (evpn) | bgp_neighbor: 192.168.255.6 | PASS |  |
| 206 | HK-LEAF1A | Routing Table | Remote Lo1 address | 192.168.254.3 | PASS |  |
| 207 | HK-LEAF1A | Routing Table | Remote Lo1 address | 192.168.254.5 | PASS |  |
| 208 | HK-LEAF1B | Routing Table | Remote Lo1 address | 192.168.254.3 | PASS |  |
| 209 | HK-LEAF1B | Routing Table | Remote Lo1 address | 192.168.254.5 | PASS |  |
| 210 | HK-LEAF2A | Routing Table | Remote Lo1 address | 192.168.254.3 | PASS |  |
| 211 | HK-LEAF2A | Routing Table | Remote Lo1 address | 192.168.254.5 | PASS |  |
| 212 | HK-LEAF2B | Routing Table | Remote Lo1 address | 192.168.254.3 | PASS |  |
| 213 | HK-LEAF2B | Routing Table | Remote Lo1 address | 192.168.254.5 | PASS |  |
| 214 | HK-LEAF1A | Routing Table | Remote Lo0 address | 192.168.255.3 | PASS |  |
| 215 | HK-LEAF1A | Routing Table | Remote Lo0 address | 192.168.255.4 | PASS |  |
| 216 | HK-LEAF1A | Routing Table | Remote Lo0 address | 192.168.255.5 | PASS |  |
| 217 | HK-LEAF1A | Routing Table | Remote Lo0 address | 192.168.255.6 | PASS |  |
| 218 | HK-LEAF1B | Routing Table | Remote Lo0 address | 192.168.255.3 | PASS |  |
| 219 | HK-LEAF1B | Routing Table | Remote Lo0 address | 192.168.255.4 | PASS |  |
| 220 | HK-LEAF1B | Routing Table | Remote Lo0 address | 192.168.255.5 | PASS |  |
| 221 | HK-LEAF1B | Routing Table | Remote Lo0 address | 192.168.255.6 | PASS |  |
| 222 | HK-LEAF2A | Routing Table | Remote Lo0 address | 192.168.255.3 | PASS |  |
| 223 | HK-LEAF2A | Routing Table | Remote Lo0 address | 192.168.255.4 | PASS |  |
| 224 | HK-LEAF2A | Routing Table | Remote Lo0 address | 192.168.255.5 | PASS |  |
| 225 | HK-LEAF2A | Routing Table | Remote Lo0 address | 192.168.255.6 | PASS |  |
| 226 | HK-LEAF2B | Routing Table | Remote Lo0 address | 192.168.255.3 | PASS |  |
| 227 | HK-LEAF2B | Routing Table | Remote Lo0 address | 192.168.255.4 | PASS |  |
| 228 | HK-LEAF2B | Routing Table | Remote Lo0 address | 192.168.255.5 | PASS |  |
| 229 | HK-LEAF2B | Routing Table | Remote Lo0 address | 192.168.255.6 | PASS |  |
| 230 | HK-SPINE1 | Routing Table | Remote Lo0 address | 192.168.255.3 | PASS |  |
| 231 | HK-SPINE1 | Routing Table | Remote Lo0 address | 192.168.255.4 | PASS |  |
| 232 | HK-SPINE1 | Routing Table | Remote Lo0 address | 192.168.255.5 | PASS |  |
| 233 | HK-SPINE1 | Routing Table | Remote Lo0 address | 192.168.255.6 | PASS |  |
| 234 | HK-SPINE2 | Routing Table | Remote Lo0 address | 192.168.255.3 | PASS |  |
| 235 | HK-SPINE2 | Routing Table | Remote Lo0 address | 192.168.255.4 | PASS |  |
| 236 | HK-SPINE2 | Routing Table | Remote Lo0 address | 192.168.255.5 | PASS |  |
| 237 | HK-SPINE2 | Routing Table | Remote Lo0 address | 192.168.255.6 | PASS |  |
| 238 | HK-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF1A - 192.168.255.3 Destination: 192.168.255.3 | PASS |  |
| 239 | HK-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF1A - 192.168.255.3 Destination: 192.168.255.4 | PASS |  |
| 240 | HK-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF1A - 192.168.255.3 Destination: 192.168.255.5 | PASS |  |
| 241 | HK-LEAF1A | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF1A - 192.168.255.3 Destination: 192.168.255.6 | PASS |  |
| 242 | HK-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF1B - 192.168.255.4 Destination: 192.168.255.3 | PASS |  |
| 243 | HK-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF1B - 192.168.255.4 Destination: 192.168.255.4 | PASS |  |
| 244 | HK-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF1B - 192.168.255.4 Destination: 192.168.255.5 | PASS |  |
| 245 | HK-LEAF1B | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF1B - 192.168.255.4 Destination: 192.168.255.6 | PASS |  |
| 246 | HK-LEAF2A | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF2A - 192.168.255.5 Destination: 192.168.255.3 | PASS |  |
| 247 | HK-LEAF2A | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF2A - 192.168.255.5 Destination: 192.168.255.4 | PASS |  |
| 248 | HK-LEAF2A | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF2A - 192.168.255.5 Destination: 192.168.255.5 | PASS |  |
| 249 | HK-LEAF2A | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF2A - 192.168.255.5 Destination: 192.168.255.6 | PASS |  |
| 250 | HK-LEAF2B | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF2B - 192.168.255.6 Destination: 192.168.255.3 | PASS |  |
| 251 | HK-LEAF2B | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF2B - 192.168.255.6 Destination: 192.168.255.4 | PASS |  |
| 252 | HK-LEAF2B | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF2B - 192.168.255.6 Destination: 192.168.255.5 | PASS |  |
| 253 | HK-LEAF2B | Loopback0 Reachability | Loopback0 Reachability | Source: HK-LEAF2B - 192.168.255.6 Destination: 192.168.255.6 | PASS |  |
| 254 | HK-SPINE1 | Loopback0 Reachability | Loopback0 Reachability | Source: HK-SPINE1 - 192.168.255.1 Destination: 192.168.255.3 | PASS |  |
| 255 | HK-SPINE1 | Loopback0 Reachability | Loopback0 Reachability | Source: HK-SPINE1 - 192.168.255.1 Destination: 192.168.255.4 | PASS |  |
| 256 | HK-SPINE1 | Loopback0 Reachability | Loopback0 Reachability | Source: HK-SPINE1 - 192.168.255.1 Destination: 192.168.255.5 | PASS |  |
| 257 | HK-SPINE1 | Loopback0 Reachability | Loopback0 Reachability | Source: HK-SPINE1 - 192.168.255.1 Destination: 192.168.255.6 | PASS |  |
| 258 | HK-SPINE2 | Loopback0 Reachability | Loopback0 Reachability | Source: HK-SPINE2 - 192.168.255.2 Destination: 192.168.255.3 | PASS |  |
| 259 | HK-SPINE2 | Loopback0 Reachability | Loopback0 Reachability | Source: HK-SPINE2 - 192.168.255.2 Destination: 192.168.255.4 | PASS |  |
| 260 | HK-SPINE2 | Loopback0 Reachability | Loopback0 Reachability | Source: HK-SPINE2 - 192.168.255.2 Destination: 192.168.255.5 | PASS |  |
| 261 | HK-SPINE2 | Loopback0 Reachability | Loopback0 Reachability | Source: HK-SPINE2 - 192.168.255.2 Destination: 192.168.255.6 | PASS |  |
