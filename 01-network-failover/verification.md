# Verification & Failover Testing

## Test 1 — Normal Operation

The PC-MNL successfully reached the data center server.

Source:
192.168.10.1

Destination:
192.168.40.1

The primary route through R2-PRIMARY was active.

## Test 2 — Primary Link Failure

The link between R1-MANILA and R2-PRIMARY was disconnected.

This simulated a failure of the primary WAN path.

## Test 3 — Failover

OSPF detected the topology change and recalculated the route.

Traffic was redirected through:

PC-MNL
→ R1-MANILA
→ R3-BACKUP
→ R4-DC
→ SRV-DC

Connectivity was restored after OSPF convergence.

## Test 4 — Primary Route Recovery

The R1-MANILA to R2-PRIMARY link was restored.

OSPF reconverged and the primary route became preferred again.

## Result

The network successfully demonstrated automatic WAN failover
and recovery using OSPF.
