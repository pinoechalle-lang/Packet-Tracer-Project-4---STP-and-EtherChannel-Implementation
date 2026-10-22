# Packet-Tracer-Project-4---STP-and-EtherChannel-Implementation
![Project 4 Screenshot](https://github.com/pinoechalle-lang/Packet-Tracer-Project-4---STP-and-EtherChannel-Implementation/blob/main/Screenshot%202026-10-23%20030032.png?raw=true)

##### This project simulates enterprise switching environments where redundant links are deployed between switches to eliminate single points of failure. STP prevents Layer 2 loops, while EtherChannel enables bandwidth aggregation and uninterrupted network operation during individual link failures.
---
## Requirements:
Create a topology consisting of:

Three Cisco switches (SW1, SW2, and SW3)
Two end devices for connectivity testing
Multiple redundant links between switches

---
The STP is automatic by default in the Cisco Switch 2960. However, you still need to influence the STP election.

Configure SW1 as the Root Bridge by modifying its bridge priority.
Verify Root Bridge election, port roles, and port states.
Demonstrate how STP selects optimal paths and blocks redundant links to maintain a loop-free topology.

---
Configure PAgP EtherChannel between:

- SW1 and SW2
- SW1 and SW3

Configure LACP EtherChannel between:

- SW2 and SW3

---
Bundle multiple physical links into logical Port-Channels and demonstrate the concept of bandwidth aggregation.

Calculate the theoretical total bandwidth provided by each EtherChannel bundle based on the speed of the member interfaces.
Compare the bandwidth of a single physical link with the aggregated bandwidth of the EtherChannel.

---
## Verification

Verify all configurations using appropriate commands, including:
```bash
show spanning-tree
show etherchannel summary
show interfaces port-channel
```

Perform connectivity and failover testing by:
- Verifying end-to-end communication between devices.
- Disabling individual EtherChannel member links and confirming uninterrupted network connectivity.
- Observing STP behavior during topology changes and link failures.



