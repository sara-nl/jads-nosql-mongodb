theme: Olive green, 8
footer: SURFsara, 25-10-2016
slidenumbers: true
autoscale: true

# NoSQL and MongoDB: 
### JADS Master: Data Engineering

# [fit]![inline 100%](sources/db_landscape.png)

---
### Today

__Part II: Partitioning, CAP, NewSQL__
- Partitioning
- CAP
- NewSQL (if time permits)

---
### Scaling: often means partitioning

![original 100%](sources/scalingrdbms3.png)

---
### Partitioning

![original 100%](sources/part1.png)

---
### Partitioning

![original 100%](sources/part2.png)

---
### Partitioning

![original 100%](sources/part3.png)

---
### Partitioning and CAP

![original 160%](sources/cap1.png)

---
### Partitioning and CAP
__Consistency__: All nodes see the same data at the same time

__Availability__: A guarantee that every request receives a response about whether it succeeded or failed

__Partition tolerance__: Ability to cope with a partitioned network of system nodes

---
### Partitioning and CAP

![original 100%](sources/caps1.png)

---
### Partitioning and CAP

![original 100%](sources/caps2.png)

---
### Partitioning and CAP

![original 100%](sources/caps3.png)

---
### Partition tolerance
 1. The network is reliable
 2. Latency is zero
 3. Bandwidth is infinite
 4. The network is secure
 5. Topology doesn't change
 6. There is one administrator
 7. Transport cost is zero
 8. The network is homogeneous

![original, right 100%](sources/networks.png)

---
### CAP Misconceptions
1. CA?
2. No CA when P?
3. C is all or nothing
4. CAP is all about eventual consistency

---
### PACELC
__If Partioned__:
Tradeoff Availability and Consistency

__Else__:
Tradeoff Latency and Consistency

__Types of systems__:
- PC/EC -> Most consistent
- PA/EL -> No consistency but low latency
- PA/EC -> Give up consistency when partitioned
- PC/EL -> Madness? See PNUTS

---
### Consistency in a distributed system
__Nodes must exchange information on writes__:
    - Inform replicas
    - Inform client


__How to deal with conflicts?__:
    - Last write win?
    - Vector clocks
    - Multiversion storage
    - Hardware clocks

---
### Consistency: atomicity and ordering
![original 100%](sources/aando.png)

---
### Consistency: vector clocks
![original 100%](sources/vectorclocks.png)

---
### Consistency: tunable CAP
__Riak__:
*N*: number of total copies
*R*: minimal number of responding clients when reading
*W*: minimal number of responding clients when writing

__Cassandra__:
Tunable write consistency
Tunable read consistency

__MongoDB__:
Write result setting
Read result setting

![right, 20%](sources/knobs.jpg)

---
### Tunable CAP: Amazon shopping Basket

Amazon uses DynamoDB for shopping baskets. DynamoDB, like Riak is a distributed
key-value store where N-R-W can be set for operation.

If you were Amazon, how would you choose N-R-W for a shopping basket?

---
### Eventual consistency

__Key property of non-ACID__
    - If no further changes
    - All nodes will end up consistent

__Weak guarantee__
    - When is eventually? It doesn’t say..
    - In practice: expect inconsistency; always!

__In practice__:
    - Stronger guarantees: predicting/measuring behavior
    - Systems often appear strongly consistent

---
### Eventual consistency
![original 100%](sources/consistency.jpg)

---
# Questions?

---
### Meanwhile at
![original 100%](sources/Google.png)

---
### NewSQL
![original 100%](sources/f1_1.png)

---
### NewSQL
![original 100%](sources/f1_2.png)

---
### NewSQL
Some Requirements:

__Scalable__
    - By adding hardware
    - No manual sharding
    
__Available__
    - No downtime,  ever

__Consistent__
    - Full ACID

__Usable__
    - Full SQL with indexes
   
![original, right 100%](sources/f1_3.png) 

---
### NewSQL

__Spanner__:
- Semi-relational distributed DB
    - SQL queries
    - Versioned data
- Consistent reads/writes
- Atomic schema updates
- High availability
- Removing nodes has no effect except on throughput (PC/EC)

__TrueTime__:
- Timestamp: consistent ordering on transactions
- Uses: GPS and atomic clocks

![original, right 150%](sources/paxos.png) 

---
### NewSQL
__F1__:
- Distributed SQL queries
- Consistent indexes
- Automatic change history (triggers)

![original, right 150%](sources/f1_4.png) 

---
### NewSQL
__F1__:
- 100 TB of uncompressed data 
    - Over 5 data centers
    - Five nines uptime

- Hundreds of thousands of request/second

- SQL queries scan trillions of rows/day

- No observable increase of latency compared to MySQL

- NoSQL (key -> row) and full SQL

![right 100%](sources/f1_5.png) 

---
# Questions?