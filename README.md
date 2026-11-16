# Enterprise Office Network & ELV/ICT Infrastructure Design

A simulated, end-to-end design of a multi-floor enterprise office network and its ELV/ICT systems (CCTV, access control, VoIP). This is a personal design project: no real client, all values are assumptions documented in [`docs/01-requirements-assumptions.md`](docs/01-requirements-assumptions.md).

## Project Scope

### Part A: Enterprise Network Design
- Layer 2 / Layer 3 switching (collapsed core + access)
- VLAN segmentation and inter-VLAN routing
- IP addressing and subnetting
- Firewall, NAT, Wi-Fi, PoE and fiber uplink architecture
- Topology diagrams, VLAN/IP allocation plans, configuration documentation

### Part B: ELV / ICT Infrastructure Design
- Conceptual IP CCTV, access control and VoIP architecture
- PoE power budget, fiber/SFP selection, structured cabling layout, BOQ
- Simulated commissioning checklists, snag reports, As-Built documentation

## Repository Structure

```
enterprise-network-ict-design/
├── README.md
├── docs/
│   ├── 00-project-scope.md
│   ├── 01-requirements-assumptions.md
│   ├── network/        # VLAN/IP plan, firewall, Wi-Fi, fiber
│   └── elv/            # CCTV, access control, VoIP, PoE budget, cabling
├── diagrams/           # Topology diagrams (Mermaid / PNG)
├── configs/
│   ├── switches/       # Core, distribution, access configs
│   └── firewall/       # Policy, NAT, ACL
├── boq/                # Bill of quantities
└── commissioning/      # Checklists, snag report, As-Built
```

## Progress

- [x] Part 1: Scope and requirements
- [ ] Part 2: VLAN and IP addressing plan
- [ ] Part 3: Topology diagrams
- [ ] Part 4: Switch configurations
- [ ] Part 5: Firewall, NAT, ACL
- [ ] Part 6: Wi-Fi and PoE for APs
- [ ] Part 7: Fiber uplinks and SFP selection
- [ ] Part 8: ELV architecture (CCTV, access control, VoIP)
- [ ] Part 9: PoE power budget and structured cabling
- [ ] Part 10: BOQ
- [ ] Part 11: Commissioning, snag report, As-Built
- [ ] Part 12: Final review

## Tools / Standards Referenced
Cisco Packet Tracer (simulation), draw.io / Mermaid (diagrams), IEEE 802.1Q, 802.3af/at/bt (PoE), 802.11ac/ax (Wi-Fi), TIA/EIA-568 and ISO/IEC 11801 (structured cabling).

## Disclaimer
This is a simulated design for learning and portfolio purposes. No real site, client or confidential data is used.
