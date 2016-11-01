theme: Olive green, 8
footer: SURFsara, 25-10-2016
slidenumbers: true
autoscale: true

# NoSQL and MongoDB: 
### JADS Master: Data Engineering

# [fit]![inline 100%](sources/db_landscape.png)

---
### Today

__Part III: MongoDB__
- Data model
- Querying
- Sharding
- Caveats

---
### MongoDB is web scale

> MongoDB (from humongous) is a free and open-source cross-platform document-oriented database program. Classified as a NoSQL database program, MongoDB uses JSON-like documents with schemas. 

-- Wikipedia

---
### Data model: Document oriented
JSON Documents as data.

__Document store__:
- MongoDB

![right 150%](sources/docstores.png)

---
### Data model: Document oriented vs. Relational

![original 75%](sources/mongorelmodel.png)![original 65%](sources/mongodm.png)

---
### MongoDB CRUD
__Per collection:__

- Create documents
- Read documents
- Update documents
- Delete documents

NB: All write operations are atomic on the document level.

---
### MongoDB CRUD: Insert
![original 150%](sources/mongoinsert.png)

---
### MongoDB CRUD: Read
![original 150%](sources/mongofind.png)

---
### MongoDB CRUD: Update
![original 150%](sources/mongoupdate.png)

---
### MongoDB CRUD: Delete
![original 150%](sources/mongodel.png)

---
### Aggregations: Single purpose, pipelineing, mr
![original 110%](sources/mongodist.png)

---
### Aggregations: Single purpose, pipelineing, mr
![original 110%](sources/mongoagg.png)

---
### Aggregations: Single purpose, pipelineing, mr
![original 90%](sources/mongomr.png)

---
### High-availability
![original 70%](sources/mongoreplication.png)

---
### Scalability
![original 125%](sources/mongo-sharding.png)

---
### Scalability
![original 90%](sources/mongosharding2.png)

---
### Critics 
![original 75%](sources/webscale.png)

---
### Caveats
- Durability: Mongo will ack write succesful even though data might not be on disk
- Failure scenarios: stale reads or rollback of writes when an application can access two partitioned processes
- Concurrency control depends on storage engine: collection level/document level
- Queries against an index are not atomic and might miss documents being updated during the query

---
# Questions?

