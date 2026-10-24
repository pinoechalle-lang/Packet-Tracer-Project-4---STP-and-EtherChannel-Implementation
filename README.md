# Packet-Tracer-Project-4---STP-and-EtherChannel-Implementation
![Project 4 Screenshot](https://github.com/pinoechalle-lang/Packet-Tracer-Project-4---STP-and-EtherChannel-Implementation/blob/main/Screenshot%202026-10-23%20030032.png?raw=true)

##### This project simulates enterprise switching environments where redundant links are deployed between switches to eliminate single points of failure. STP prevents Layer 2 loops, while EtherChannel enables bandwidth aggregation and uninterrupted network operation during individual link failures.
---
## Requirements:
Create a topology consisting of:

Three Cisco switches (SW1, SW2, and SW3)
Two end devices for connectivity testing
Multiple redundant links between switches

- SW1 (F0/1-2) <===> (F0/1-2) SW2
- SW1 (F0/3-4) <===> (F0/1-2) SW3
- SW2 (F0/3-4) <===> (F0/3-4) SW3
  
- PC A <---> (F0/5) SW2
- PC B <---> (F0/5) SW3
---
Configure the following VLANs:
- VLAN 124 for PC A
- VLAN 89 for PC B

Configure switch-to-switch connections as trunk links to allow VLAN traffic to traverse the Layer 2 topology.
> NOTE: Make sure the logical port-channel is configured under the port interface, while the trunk is configured under the logical port-channel interface. These two are different things.

---
The STP is automatic by default in the Cisco Switch 2960. However, you still need to influence the STP election.

Configure SW1 as the Root Bridge for all VLANs involved by modifying its bridge priority.
Verify Root Bridge election, port roles, and port states.
Demonstrate how STP selects optimal paths and blocks redundant links to maintain a loop-free topology.

---
Configure PAgP EtherChannel between:
- SW1 (po1) <===> (po1) SW2
- SW1 (po2) <===> (po2) SW3

Configure LACP EtherChannel between:
- SW2 (po3) <===> (po3) SW3

> NOTE: po means port-channel, which is a term used to describe an EtherChannel logical group. "*po1*" means port-channel 1.

---
Bundle multiple physical links into logical Port-Channels and demonstrate the concept of bandwidth aggregation.

Calculate the theoretical total bandwidth provided by each EtherChannel bundle based on the speed of the member interfaces.
Compare the bandwidth of a single physical link with the aggregated bandwidth of the EtherChannel.

---
## Verification

Verify all configurations using appropriate commands, including:
```bash
show spanning-tree
show spanning-tree vlan <vlan>
show spanning-tree summary

show etherchannel summary
show etherchannel detail
show interfaces port-channel

show vlan brief
show interfaces trunk
```

Perform connectivity and failover testing by:
- Verifying end-to-end communication between devices.
- Disabling individual EtherChannel member links and confirming uninterrupted network connectivity.
- Observing STP behavior during topology changes and link failures.

To verify if ICMP packets work, simply set-up a router and connect it to SW1 through its port Gigabit Ethernet 0/1 (g0/1), as this specific port has been configured for trunking.


