# Network Failover & Redundant WAN Routing

Cisco Packet Tracer lab demonstrating OSPF-based network redundancy and
automatic failover between primary and backup WAN paths.


## 1. Normal Network Operation

The network initially uses the primary WAN path through R2-PRIMARY.

![Normal Topology](screenshots/topology.png)

## 2. Primary Routing Path

The routing table shows that the data center network is reached through
the primary R2-PRIMARY path.

![Normal Routing](screenshots/01-norrmal-routing.png)

## 3. Primary Link Failure

The R1-MANILA to R2-PRIMARY link was disconnected to simulate a WAN failure.

![Primary Failure](screenshots/02-primary-failure.png)

## 4. OSPF Failover

After OSPF convergence, the route to the data center was redirected
through R3-BACKUP.

![Failover Routing](screenshots/03-failover-routing.png)

## 5. Connectivity After Failover

Connectivity to the data center server was restored through the backup path.

![Failover Ping](screenshots/04-failover-ping.png)

## 6. Primary Route Recovery

After reconnecting the primary WAN link, OSPF reconverged and traffic
returned to the preferred path.

![Primary Restored](screenshots/05-primary-restored.png)
