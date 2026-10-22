# Packet-Tracer-Project-4---STP-and-EtherChannel-Implementation


---
## Requirements:
Create a topology consisting of three switches (SW1, SW2, and SW3) and two end devices connected through redundant switch links.

Implement Spanning Tree Protocol (STP) to prevent Layer 2 switching loops.

Configure SW1 as the Root Bridge by modifying its bridge priority.
Verify the Root Bridge election and identify the port roles and states assigned by STP.
Demonstrate that STP maintains a loop-free topology by blocking redundant paths when necessary.

Implement EtherChannel using LACP between SW2 and SW3 by bundling two physical links into a single logical Port-Channel.

---
Verify successful EtherChannel formation.
Confirm that all member interfaces actively participate in the Port-Channel.

> Verify configurations using:

```bash
show spanning-tree
show etherchannel summary
```

---
Test network resilience by:

Performing end-to-end connectivity tests between PC1 and PC2.
Simulating a link failure on one EtherChannel member interface and verifying that communication remains uninterrupted.

