theme: Olive green, 8
footer: SURFsara, 25-10-2016
slidenumbers: true
autoscale: true

# NoSQL and MongoDB: 
### JADS Master: Data Engineering

# [fit]![inline 100%](sources/db_landscape.png)

---

### Today

- __Part I: NoSQL drivers, data models and hype__
- __Part II: Partitioning, CAP, NewSQL__
- __Part II: MongoDB, examples, discussion__

### Next week:

- __Part IV: Hands-on exercise MongoDB__

---

### Today

__Part I: NoSQL drivers, data models and hype__
- NoSQL driving forces
- Data models
- Hype? (if time permits) 

![right 50%](sources/nosql.png)

---
### NoSQL - driving forces  

1. *Scaling out*: partitioning
2. *Performance*: remove complexity, simplify assumptions
4. *Impedance mismatch*: from relational data structures to programming language constructs

---
### Partitioning for RDBMS?
![original, right 75%](sources/joins.png)
![original, left 75%](sources/acid.jpg)

---

### Scaling relational databases

![original 100%](sources/scalingrdbms.png)

---

### Scaling relational databases

![original 100%](sources/scalingrdbms2.png)

---

### Scaling relational databases

![original 100%](sources/scalingrdbms3.png)

---

### Scaling relational databases

![original 100%](sources/cqrsmvc.png)

---
### Performance: The cost of not being on time
![original, 100%](sources/costs.png)

---
### Performance: The cost of not being on time
![original, 150%](sources/ing1.png)

---
### Impedance mismatch
![original, 100%](sources/impedancem1.png)

---
__Object oriented__
*vs.* __Relational__ data structures

![original, 100%](sources/ORMS.png)

---
### Impedance mismatch
![original, 100%](sources/impedancem2.png)

---
### Data models
![original, fit](sources/dmodels.png)

---
### Data model: Key-value
Similar to dictionaries and (hash)maps

__Key-value stores__:
- Riak
- DynamoDB
- Redis
- memcached

![right 150%](sources/kvstores.png)

---
### Data model: Column based
__Column stores__:
- HBase
- Cassandra
- MonetDB
- Google: BigTable

![right 150%](sources/columnstores.png)

---
### Data model: Document oriented
JSON Documents as data.

__Document stores__:
- MongoDB
- CouchDB
- CouchBase

![right 150%](sources/docstores.png)

---
### Data model: Graphs
Graphs and graph queries as first class citizens.

__Graph stores__:
- Neo4J
- OpenLink
- Titan

![right 150%](sources/graphstores.png)


---
### Data model: Specialized
Distributed 
Lucene 
Indexes

![original 150%](sources/es.png)

---
### Schema on read vs. Schema on write

![original 100%](sources/sabg.png)

---
# Questions?

---
### Hype?
![original 100%](sources/endor.png)

---
### Hype?
![original 100%](sources/oracles.png)

---
### Hype?
![original 150%](sources/jobtrends1.png)

---
### Hype?
![original 150%](sources/jobtrends2.png)

---
### Hype?
![original 150%](sources/jobtrends3.png)

---
### Hype?
![original 150%](sources/jobtrends4.png)

---
### Hype?
![original 150%](sources/oodb.png)

---
### Hype?
![original 150%](sources/xmldb.png)

---
### Hype?
![original 150%](sources/nosqldb.png)

---
### Hype?
![original 100%](sources/trendsovertime.png)

---
### Future directions
- Internal polyglot support
- Multi-model systems
- NewSQL: Can you have a scalable databases without going NoSQL? (“beating” CAP)
- Further support for NoSQL in RDBMs
- DBaaS and Baas

---

### Beware of vendor speak
![original 100%](sources/vendorspeak.png)

---
# Questions?


