# CAP Theorem

## Definitions

**CAP** stands for:

* **Consistency (C)**
  Data should be the same across all servers once a change is made — **immediately** after the write.

* **Availability (A)**
  The system should respond to every request immediately, even if it means returning **stale data**.

* **Partition Tolerance (P)**
  Occurs in distributed systems when the network breaks and servers are forced to operate independently because they cannot communicate.

---

## Core Rule of the CAP Theorem

When a **network partition** happens, a distributed system must choose between:

1. **Consistency**
2. **Availability**

It cannot guarantee both simultaneously.

> In practice, partition tolerance is required, so the real trade-off is **Consistency vs Availability** during failures.

---

## CP Systems (Consistency + Partition Tolerance)

**Priority:** Correct data over responsiveness.

### Behavior

* Nodes may reject reads/writes
* System may become temporarily unavailable
* Ensures data correctness across all nodes

### Typical Use Cases

* Banking systems
* Payment processing
* Financial transactions
* Inventory management

### Examples

* ZooKeeper
* MongoDB (strong consistency configurations)
* HBase
* etcd

---

## AP Systems (Availability + Partition Tolerance)

**Priority:** Responsiveness over immediate correctness.

### Behavior

* Nodes always respond to requests
* Data may be temporarily inconsistent (stale)
* System synchronizes data later

### Typical Use Cases

* Social media platforms
* DNS systems
* Messaging systems
* Caching layers

### Examples

* Cassandra
* DynamoDB
* CouchDB
* Riak

---

## CA Systems (Consistency + Availability)

**Works only when partitions do not occur.**

### Key Insight

* Requires a perfectly reliable network
* Not realistic in distributed systems
* Typically applies to:

  * Single-node databases
  * Non-distributed systems
  * Local systems

> Therefore, **CA is mostly theoretical in distributed environments.**

---

## One-Line Summary

**CAP theorem states that during a network partition, a distributed system must choose between consistency and availability, since it cannot guarantee both simultaneously.**
