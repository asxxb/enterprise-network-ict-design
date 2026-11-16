# 01 - Requirements and Assumptions

## 1. Building and Users
| Item | Assumption |
|---|---|
| Floors | Ground + 3 (G, 1, 2, 3) plus server/comms room on Ground |
| Total staff | ~200 (G: 40, 1: 60, 2: 60, 3: 40) |
| Meeting rooms | 2 per floor, with Wi-Fi and wired ports |
| Visitors | Guest Wi-Fi at reception and meeting rooms |

## 2. Connected Devices (estimates)
| Device | Qty | Notes |
|---|---|---|
| User workstations / laptops | 200 | 1 wired port + Wi-Fi |
| IP phones | 200 | PoE, daisy-chained to PC or separate port |
| Wi-Fi access points | 12 | 3 per floor, PoE+ |
| IP CCTV cameras | 32 | 8 per floor, PoE |
| Access control readers/controllers | 16 | Doors, lifts lobby, server room |
| Network printers | 8 | 2 per floor |
| Servers (on-prem) | 6 | Directory, file, VoIP PBX, NVR, etc. |

## 3. Functional Requirements
1. Segregate traffic by function (users, voice, servers, CCTV, access control, guest, management).
2. Voice traffic prioritised using QoS.
3. Guest users isolated from internal resources.
4. Redundant uplinks between floors and core.
5. Internet access via firewall with NAT.
6. All ELV systems on isolated VLANs.

## 4. Non-Functional Requirements
- **Availability:** no single point of failure on core-to-floor links
- **Scalability:** 30% spare capacity in ports and address space
- **Security:** least-privilege inter-VLAN policy, port security, DHCP snooping
- **Manageability:** dedicated management VLAN, SNMP/syslog/NTP

## 5. Design Assumptions
- Collapsed core: core switch pair in the Ground floor comms room
- One access switch stack per floor, fiber uplink to core
- ISP provides one 1 Gbps fiber handoff (single ISP for this design)
- Private addressing from 10.0.0.0/8 with a structured plan (Part 2)
- Cabling: Cat6 horizontal (max 90 m), OM4/OS2 fiber for risers
