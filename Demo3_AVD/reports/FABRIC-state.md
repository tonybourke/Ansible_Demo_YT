# Validate State Report

**Table of Contents:**

- [Validate State Report](validate-state-report)
  - [Test Results Summary](#test-results-summary)
  - [Failed Test Results Summary](#failed-test-results-summary)
  - [All Test Results](#all-test-results)

## Test Results Summary

### Summary Totals

| Total Tests | Total Tests Passed | Total Tests Failed | Total Tests Skipped |
| ----------- | ------------------ | ------------------ | ------------------- |
| 256 | 218 | 14 | 24 |

### Summary Totals Device Under Test

| Device Under Test | Total Tests | Tests Passed | Tests Failed | Tests Skipped | Categories Failed | Categories Skipped |
| ------------------| ----------- | ------------ | ------------ | ------------- | ----------------- | ------------------ |
| leaf1 | 50 | 43 | 3 | 4 | Interfaces, System | Hardware |
| leaf2 | 50 | 43 | 3 | 4 | Interfaces, System | Hardware |
| leaf3 | 50 | 43 | 3 | 4 | Interfaces, System | Hardware |
| leaf4 | 50 | 43 | 3 | 4 | Interfaces, System | Hardware |
| spine1 | 28 | 23 | 1 | 4 | System | Hardware |
| spine2 | 28 | 23 | 1 | 4 | System | Hardware |

### Summary Totals Per Category

| Test Category | Total Tests | Tests Passed | Tests Failed | Tests Skipped |
| ------------- | ----------- | ------------ | ------------ | ------------- |
| BGP | 36 | 36 | 0 | 0 |
| Connectivity | 64 | 64 | 0 | 0 |
| Hardware | 24 | 0 | 0 | 24 |
| Interfaces | 78 | 70 | 8 | 0 |
| MLAG | 4 | 4 | 0 | 0 |
| Routing | 38 | 38 | 0 | 0 |
| System | 12 | 6 | 6 | 0 |

## Failed Test Results Summary

| ID | Device Under Test | Categories | Test | Description | Inputs | Result | Messages |
| -- | ----------------- | ---------- | ---- | ----------- | ------ | -------| -------- |
| 31 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel10 = 'up' | FAIL | Port-Channel10 - Expected: up/up, Actual: down/lowerLayerDown |
| 32 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel11 = 'up' | FAIL | Port-Channel11 - Expected: up/up, Actual: down/lowerLayerDown |
| 49 | leaf1 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 81 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel10 = 'up' | FAIL | Port-Channel10 - Expected: up/up, Actual: down/lowerLayerDown |
| 82 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel11 = 'up' | FAIL | Port-Channel11 - Expected: up/up, Actual: down/lowerLayerDown |
| 99 | leaf2 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 131 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel10 = 'up' | FAIL | Port-Channel10 - Expected: up/up, Actual: down/lowerLayerDown |
| 132 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel11 = 'up' | FAIL | Port-Channel11 - Expected: up/up, Actual: down/lowerLayerDown |
| 149 | leaf3 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 181 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel10 = 'up' | FAIL | Port-Channel10 - Expected: up/up, Actual: down/lowerLayerDown |
| 182 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel11 = 'up' | FAIL | Port-Channel11 - Expected: up/up, Actual: down/lowerLayerDown |
| 199 | leaf4 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 227 | spine1 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 255 | spine2 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |

## All Test Results

| ID | Device Under Test | Categories | Test | Description | Inputs | Result | Messages |
| -- | ----------------- | ---------- | ---- | ----------- | ------ | -------| -------- |
| 1 | leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: spine1 (IP: 172.16.10.11) | PASS | - |
| 2 | leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: spine2 (IP: 172.16.10.12) | PASS | - |
| 3 | leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf2 (IP: 172.16.12.129) | PASS | - |
| 4 | leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: spine1 (IP: 172.16.13.0) | PASS | - |
| 5 | leaf1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: spine2 (IP: 172.16.13.2) | PASS | - |
| 6 | leaf1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: leaf2 Ethernet1 | PASS | - |
| 7 | leaf1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: leaf2 Ethernet2 | PASS | - |
| 8 | leaf1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: spine1 Ethernet3 | PASS | - |
| 9 | leaf1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet4 - Remote: spine2 Ethernet3 | PASS | - |
| 10 | leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.1) - Destination: leaf1 Loopback0 (IP: 172.16.10.1) | PASS | - |
| 11 | leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.1) - Destination: leaf2 Loopback0 (IP: 172.16.10.2) | PASS | - |
| 12 | leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.1) - Destination: leaf3 Loopback0 (IP: 172.16.10.3) | PASS | - |
| 13 | leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.1) - Destination: leaf4 Loopback0 (IP: 172.16.10.4) | PASS | - |
| 14 | leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.1) - Destination: spine1 Loopback0 (IP: 172.16.10.11) | PASS | - |
| 15 | leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.1) - Destination: spine2 Loopback0 (IP: 172.16.10.12) | PASS | - |
| 16 | leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.13.1) - Destination: spine1 Ethernet3 (IP: 172.16.13.0) | PASS | - |
| 17 | leaf1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet4 (IP: 172.16.13.3) - Destination: spine2 Ethernet3 (IP: 172.16.13.2) | PASS | - |
| 18 | leaf1 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 19 | leaf1 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 20 | leaf1 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 21 | leaf1 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 22 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_leaf2_Ethernet1 = 'up' | PASS | - |
| 23 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet10 - Connection to host1 = 'up' | PASS | - |
| 24 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet11 - Connection to host1 = 'up' | PASS | - |
| 25 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - MLAG_leaf2_Ethernet2 = 'up' | PASS | - |
| 26 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_spine1_Ethernet3 = 'up' | PASS | - |
| 27 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_spine2_Ethernet3 = 'up' | PASS | - |
| 28 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 29 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 30 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_leaf2_Port-Channel1 = 'up' | PASS | - |
| 31 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel10 = 'up' | FAIL | Port-Channel10 - Expected: up/up, Actual: down/lowerLayerDown |
| 32 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel11 = 'up' | FAIL | Port-Channel11 - Expected: up/up, Actual: down/lowerLayerDown |
| 33 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan100 - VLAN_100 = 'up' | PASS | - |
| 34 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan200 - VLAN_200 = 'up' | PASS | - |
| 35 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_VRF_A = 'up' | PASS | - |
| 36 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 37 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 38 | leaf1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 39 | leaf1 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 40 | leaf1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 41 | leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.1 - Peer: leaf1 | PASS | - |
| 42 | leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.11 - Peer: spine1 | PASS | - |
| 43 | leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.12 - Peer: spine2 | PASS | - |
| 44 | leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.2 - Peer: leaf2 | PASS | - |
| 45 | leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.3 - Peer: leaf3 | PASS | - |
| 46 | leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.4 - Peer: leaf4 | PASS | - |
| 47 | leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.11.1 - Peer: leaf1 | PASS | - |
| 48 | leaf1 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.11.3 - Peer: leaf3 | PASS | - |
| 49 | leaf1 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 50 | leaf1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 51 | leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: spine1 (IP: 172.16.10.11) | PASS | - |
| 52 | leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: spine2 (IP: 172.16.10.12) | PASS | - |
| 53 | leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf1 (IP: 172.16.12.128) | PASS | - |
| 54 | leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: spine1 (IP: 172.16.13.4) | PASS | - |
| 55 | leaf2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: spine2 (IP: 172.16.13.6) | PASS | - |
| 56 | leaf2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: leaf1 Ethernet1 | PASS | - |
| 57 | leaf2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: leaf1 Ethernet2 | PASS | - |
| 58 | leaf2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: spine1 Ethernet4 | PASS | - |
| 59 | leaf2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet4 - Remote: spine2 Ethernet4 | PASS | - |
| 60 | leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.2) - Destination: leaf1 Loopback0 (IP: 172.16.10.1) | PASS | - |
| 61 | leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.2) - Destination: leaf2 Loopback0 (IP: 172.16.10.2) | PASS | - |
| 62 | leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.2) - Destination: leaf3 Loopback0 (IP: 172.16.10.3) | PASS | - |
| 63 | leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.2) - Destination: leaf4 Loopback0 (IP: 172.16.10.4) | PASS | - |
| 64 | leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.2) - Destination: spine1 Loopback0 (IP: 172.16.10.11) | PASS | - |
| 65 | leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.2) - Destination: spine2 Loopback0 (IP: 172.16.10.12) | PASS | - |
| 66 | leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.13.5) - Destination: spine1 Ethernet4 (IP: 172.16.13.4) | PASS | - |
| 67 | leaf2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet4 (IP: 172.16.13.7) - Destination: spine2 Ethernet4 (IP: 172.16.13.6) | PASS | - |
| 68 | leaf2 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 69 | leaf2 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 70 | leaf2 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 71 | leaf2 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 72 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_leaf1_Ethernet1 = 'up' | PASS | - |
| 73 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet10 - Connection to host1 = 'up' | PASS | - |
| 74 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet11 - Connection to host1 = 'up' | PASS | - |
| 75 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - MLAG_leaf1_Ethernet2 = 'up' | PASS | - |
| 76 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_spine1_Ethernet4 = 'up' | PASS | - |
| 77 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_spine2_Ethernet4 = 'up' | PASS | - |
| 78 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 79 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 80 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_leaf1_Port-Channel1 = 'up' | PASS | - |
| 81 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel10 = 'up' | FAIL | Port-Channel10 - Expected: up/up, Actual: down/lowerLayerDown |
| 82 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel11 = 'up' | FAIL | Port-Channel11 - Expected: up/up, Actual: down/lowerLayerDown |
| 83 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan100 - VLAN_100 = 'up' | PASS | - |
| 84 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan200 - VLAN_200 = 'up' | PASS | - |
| 85 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_VRF_A = 'up' | PASS | - |
| 86 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 87 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 88 | leaf2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 89 | leaf2 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 90 | leaf2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 91 | leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.1 - Peer: leaf1 | PASS | - |
| 92 | leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.11 - Peer: spine1 | PASS | - |
| 93 | leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.12 - Peer: spine2 | PASS | - |
| 94 | leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.2 - Peer: leaf2 | PASS | - |
| 95 | leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.3 - Peer: leaf3 | PASS | - |
| 96 | leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.4 - Peer: leaf4 | PASS | - |
| 97 | leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.11.1 - Peer: leaf1 | PASS | - |
| 98 | leaf2 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.11.3 - Peer: leaf3 | PASS | - |
| 99 | leaf2 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 100 | leaf2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 101 | leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: spine1 (IP: 172.16.10.11) | PASS | - |
| 102 | leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: spine2 (IP: 172.16.10.12) | PASS | - |
| 103 | leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf4 (IP: 172.16.12.133) | PASS | - |
| 104 | leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: spine1 (IP: 172.16.13.8) | PASS | - |
| 105 | leaf3 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: spine2 (IP: 172.16.13.10) | PASS | - |
| 106 | leaf3 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: leaf4 Ethernet1 | PASS | - |
| 107 | leaf3 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: leaf4 Ethernet2 | PASS | - |
| 108 | leaf3 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: spine1 Ethernet5 | PASS | - |
| 109 | leaf3 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet4 - Remote: spine2 Ethernet5 | PASS | - |
| 110 | leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.3) - Destination: leaf1 Loopback0 (IP: 172.16.10.1) | PASS | - |
| 111 | leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.3) - Destination: leaf2 Loopback0 (IP: 172.16.10.2) | PASS | - |
| 112 | leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.3) - Destination: leaf3 Loopback0 (IP: 172.16.10.3) | PASS | - |
| 113 | leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.3) - Destination: leaf4 Loopback0 (IP: 172.16.10.4) | PASS | - |
| 114 | leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.3) - Destination: spine1 Loopback0 (IP: 172.16.10.11) | PASS | - |
| 115 | leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.3) - Destination: spine2 Loopback0 (IP: 172.16.10.12) | PASS | - |
| 116 | leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.13.9) - Destination: spine1 Ethernet5 (IP: 172.16.13.8) | PASS | - |
| 117 | leaf3 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet4 (IP: 172.16.13.11) - Destination: spine2 Ethernet5 (IP: 172.16.13.10) | PASS | - |
| 118 | leaf3 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 119 | leaf3 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 120 | leaf3 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 121 | leaf3 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 122 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_leaf4_Ethernet1 = 'up' | PASS | - |
| 123 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet10 - Connection to host2 = 'up' | PASS | - |
| 124 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet11 - Connection to host2 = 'up' | PASS | - |
| 125 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - MLAG_leaf4_Ethernet2 = 'up' | PASS | - |
| 126 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_spine1_Ethernet5 = 'up' | PASS | - |
| 127 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_spine2_Ethernet5 = 'up' | PASS | - |
| 128 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 129 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 130 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_leaf4_Port-Channel1 = 'up' | PASS | - |
| 131 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel10 = 'up' | FAIL | Port-Channel10 - Expected: up/up, Actual: down/lowerLayerDown |
| 132 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel11 = 'up' | FAIL | Port-Channel11 - Expected: up/up, Actual: down/lowerLayerDown |
| 133 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan100 - VLAN_100 = 'up' | PASS | - |
| 134 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan200 - VLAN_200 = 'up' | PASS | - |
| 135 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_VRF_A = 'up' | PASS | - |
| 136 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 137 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 138 | leaf3 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 139 | leaf3 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 140 | leaf3 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 141 | leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.1 - Peer: leaf1 | PASS | - |
| 142 | leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.11 - Peer: spine1 | PASS | - |
| 143 | leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.12 - Peer: spine2 | PASS | - |
| 144 | leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.2 - Peer: leaf2 | PASS | - |
| 145 | leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.3 - Peer: leaf3 | PASS | - |
| 146 | leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.4 - Peer: leaf4 | PASS | - |
| 147 | leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.11.1 - Peer: leaf1 | PASS | - |
| 148 | leaf3 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.11.3 - Peer: leaf3 | PASS | - |
| 149 | leaf3 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 150 | leaf3 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 151 | leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: spine1 (IP: 172.16.10.11) | PASS | - |
| 152 | leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: spine2 (IP: 172.16.10.12) | PASS | - |
| 153 | leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf3 (IP: 172.16.12.132) | PASS | - |
| 154 | leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: spine1 (IP: 172.16.13.12) | PASS | - |
| 155 | leaf4 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: spine2 (IP: 172.16.13.14) | PASS | - |
| 156 | leaf4 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet1 - Remote: leaf3 Ethernet1 | PASS | - |
| 157 | leaf4 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet2 - Remote: leaf3 Ethernet2 | PASS | - |
| 158 | leaf4 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: spine1 Ethernet6 | PASS | - |
| 159 | leaf4 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet4 - Remote: spine2 Ethernet6 | PASS | - |
| 160 | leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.4) - Destination: leaf1 Loopback0 (IP: 172.16.10.1) | PASS | - |
| 161 | leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.4) - Destination: leaf2 Loopback0 (IP: 172.16.10.2) | PASS | - |
| 162 | leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.4) - Destination: leaf3 Loopback0 (IP: 172.16.10.3) | PASS | - |
| 163 | leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.4) - Destination: leaf4 Loopback0 (IP: 172.16.10.4) | PASS | - |
| 164 | leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.4) - Destination: spine1 Loopback0 (IP: 172.16.10.11) | PASS | - |
| 165 | leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: Loopback0 (IP: 172.16.10.4) - Destination: spine2 Loopback0 (IP: 172.16.10.12) | PASS | - |
| 166 | leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.13.13) - Destination: spine1 Ethernet6 (IP: 172.16.13.12) | PASS | - |
| 167 | leaf4 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet4 (IP: 172.16.13.15) - Destination: spine2 Ethernet6 (IP: 172.16.13.14) | PASS | - |
| 168 | leaf4 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 169 | leaf4 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 170 | leaf4 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 171 | leaf4 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 172 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet1 - MLAG_leaf3_Ethernet1 = 'up' | PASS | - |
| 173 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet10 - Connection to host2 = 'up' | PASS | - |
| 174 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet11 - Connection to host2 = 'up' | PASS | - |
| 175 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet2 - MLAG_leaf3_Ethernet2 = 'up' | PASS | - |
| 176 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_spine1_Ethernet6 = 'up' | PASS | - |
| 177 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_spine2_Ethernet6 = 'up' | PASS | - |
| 178 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 179 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback1 - VXLAN_TUNNEL_SOURCE = 'up' | PASS | - |
| 180 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel1 - MLAG_leaf3_Port-Channel1 = 'up' | PASS | - |
| 181 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel10 = 'up' | FAIL | Port-Channel10 - Expected: up/up, Actual: down/lowerLayerDown |
| 182 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Port-Channel11 = 'up' | FAIL | Port-Channel11 - Expected: up/up, Actual: down/lowerLayerDown |
| 183 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan100 - VLAN_100 = 'up' | PASS | - |
| 184 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan200 - VLAN_200 = 'up' | PASS | - |
| 185 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan3009 - MLAG_L3_VRF_VRF_A = 'up' | PASS | - |
| 186 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4093 - MLAG_L3 = 'up' | PASS | - |
| 187 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vlan4094 - MLAG = 'up' | PASS | - |
| 188 | leaf4 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Vxlan1 = 'up' | PASS | - |
| 189 | leaf4 | MLAG | VerifyMlagStatus | Verifies the health status of the MLAG configuration. | - | PASS | - |
| 190 | leaf4 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 191 | leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.1 - Peer: leaf1 | PASS | - |
| 192 | leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.11 - Peer: spine1 | PASS | - |
| 193 | leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.12 - Peer: spine2 | PASS | - |
| 194 | leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.2 - Peer: leaf2 | PASS | - |
| 195 | leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.3 - Peer: leaf3 | PASS | - |
| 196 | leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.10.4 - Peer: leaf4 | PASS | - |
| 197 | leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.11.1 - Peer: leaf1 | PASS | - |
| 198 | leaf4 | Routing | VerifyRoutingTableEntry | Verifies that the provided routes are present in the routing table of a specified VRF. | Route: 172.16.11.3 - Peer: leaf3 | PASS | - |
| 199 | leaf4 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 200 | leaf4 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 201 | spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: leaf1 (IP: 172.16.10.1) | PASS | - |
| 202 | spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: leaf2 (IP: 172.16.10.2) | PASS | - |
| 203 | spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: leaf3 (IP: 172.16.10.3) | PASS | - |
| 204 | spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: leaf4 (IP: 172.16.10.4) | PASS | - |
| 205 | spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf1 (IP: 172.16.13.1) | PASS | - |
| 206 | spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf2 (IP: 172.16.13.5) | PASS | - |
| 207 | spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf3 (IP: 172.16.13.9) | PASS | - |
| 208 | spine1 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf4 (IP: 172.16.13.13) | PASS | - |
| 209 | spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: leaf1 Ethernet3 | PASS | - |
| 210 | spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet4 - Remote: leaf2 Ethernet3 | PASS | - |
| 211 | spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet5 - Remote: leaf3 Ethernet3 | PASS | - |
| 212 | spine1 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: leaf4 Ethernet3 | PASS | - |
| 213 | spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.13.0) - Destination: leaf1 Ethernet3 (IP: 172.16.13.1) | PASS | - |
| 214 | spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet4 (IP: 172.16.13.4) - Destination: leaf2 Ethernet3 (IP: 172.16.13.5) | PASS | - |
| 215 | spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet5 (IP: 172.16.13.8) - Destination: leaf3 Ethernet3 (IP: 172.16.13.9) | PASS | - |
| 216 | spine1 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet6 (IP: 172.16.13.12) - Destination: leaf4 Ethernet3 (IP: 172.16.13.13) | PASS | - |
| 217 | spine1 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 218 | spine1 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 219 | spine1 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 220 | spine1 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 221 | spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_leaf1_Ethernet3 = 'up' | PASS | - |
| 222 | spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_leaf2_Ethernet3 = 'up' | PASS | - |
| 223 | spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet5 - P2P_leaf3_Ethernet3 = 'up' | PASS | - |
| 224 | spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - P2P_leaf4_Ethernet3 = 'up' | PASS | - |
| 225 | spine1 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 226 | spine1 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 227 | spine1 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 228 | spine1 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
| 229 | spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: leaf1 (IP: 172.16.10.1) | PASS | - |
| 230 | spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: leaf2 (IP: 172.16.10.2) | PASS | - |
| 231 | spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: leaf3 (IP: 172.16.10.3) | PASS | - |
| 232 | spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP EVPN Peer: leaf4 (IP: 172.16.10.4) | PASS | - |
| 233 | spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf1 (IP: 172.16.13.3) | PASS | - |
| 234 | spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf2 (IP: 172.16.13.7) | PASS | - |
| 235 | spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf3 (IP: 172.16.13.11) | PASS | - |
| 236 | spine2 | BGP | VerifyBGPSpecificPeers | Verifies the health of specific BGP peer(s) for given address families. | BGP IPv4 Unicast Peer: leaf4 (IP: 172.16.13.15) | PASS | - |
| 237 | spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet3 - Remote: leaf1 Ethernet4 | PASS | - |
| 238 | spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet4 - Remote: leaf2 Ethernet4 | PASS | - |
| 239 | spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet5 - Remote: leaf3 Ethernet4 | PASS | - |
| 240 | spine2 | Connectivity | VerifyLLDPNeighbors | Verifies the connection status of the specified LLDP (Link Layer Discovery Protocol) neighbors. | Local: Ethernet6 - Remote: leaf4 Ethernet4 | PASS | - |
| 241 | spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet3 (IP: 172.16.13.2) - Destination: leaf1 Ethernet4 (IP: 172.16.13.3) | PASS | - |
| 242 | spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet4 (IP: 172.16.13.6) - Destination: leaf2 Ethernet4 (IP: 172.16.13.7) | PASS | - |
| 243 | spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet5 (IP: 172.16.13.10) - Destination: leaf3 Ethernet4 (IP: 172.16.13.11) | PASS | - |
| 244 | spine2 | Connectivity | VerifyReachability | Test network reachability to one or many destination IP(s). | Source: P2P Interface Ethernet6 (IP: 172.16.13.14) - Destination: leaf4 Ethernet4 (IP: 172.16.13.15) | PASS | - |
| 245 | spine2 | Hardware | VerifyEnvironmentCooling | Verifies the status of power supply fans and all fan trays. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentCooling test is not supported on cEOSLab. |
| 246 | spine2 | Hardware | VerifyEnvironmentPower | Verifies the power supplies status. | Accepted States: 'ok' | SKIPPED | VerifyEnvironmentPower test is not supported on cEOSLab. |
| 247 | spine2 | Hardware | VerifyTemperature | Verifies if the device temperature is within acceptable limits. | - | SKIPPED | VerifyTemperature test is not supported on cEOSLab. |
| 248 | spine2 | Hardware | VerifyTransceiversManufacturers | Verifies if all the transceivers come from approved manufacturers. | Accepted Manufacturers: 'Arista Networks', 'Arastra, Inc.', 'Not Present' | SKIPPED | VerifyTransceiversManufacturers test is not supported on cEOSLab. |
| 249 | spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet3 - P2P_leaf1_Ethernet4 = 'up' | PASS | - |
| 250 | spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet4 - P2P_leaf2_Ethernet4 = 'up' | PASS | - |
| 251 | spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet5 - P2P_leaf3_Ethernet4 = 'up' | PASS | - |
| 252 | spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Ethernet6 - P2P_leaf4_Ethernet4 = 'up' | PASS | - |
| 253 | spine2 | Interfaces | VerifyInterfacesStatus | Verifies the operational states of specified interfaces to ensure they match expected configurations. | Interface Loopback0 - ROUTER_ID = 'up' | PASS | - |
| 254 | spine2 | Routing | VerifyRoutingProtocolModel | Verifies the configured routing protocol model. | Routing protocol model: multi-agent | PASS | - |
| 255 | spine2 | System | VerifyNTP | Verifies if NTP is synchronised. | - | FAIL | The device is not synchronized with the configured NTP server(s): 'NTP is disabled.' |
| 256 | spine2 | System | VerifyReloadCause | Verifies the last reload cause of the device. | - | PASS | - |
