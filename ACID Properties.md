# ACID Properties — 

**`Atomicity`**:    

Atomicity guarantees that each transaction is treated as a single "unit", which either succeeds completely, or fails completely:  
It never executes in partially.  
if any of the statements constituting a transaction fails to complete,  
the entire transaction fails and the database is left unchanged.  
An atomic system must guarantee atomicity in each and every situation,  
including power failures, errors and crashes.  
A partial txn can cause more damage to the system than rejecting the whole set of transactions outright  

**`Consistency`** ensures that a transaction can only bring the database from one valid state to another.  
Any data written to the database must be valid according to all defined rules, including constraints, cascades, triggers, etc.  

**`Isolation`**:  
Transactions are often executed concurrently.  
Isolation ensures that concurrent execution of transactions leaves the database in the same state  
that would have been obtained if the transactions were executed sequentially  

**`Durability`** guarantees that once a transaction has been committed,  
it will remain committed even in the case of a system failure (e.g., power outage or crash).  
This usually means that completed transactions (or their effects) are recorded in non-volatile memory  

**Usecase:**  
All these properties are applied,  
when the transactions getting carried out on the same host/machine,  
where a single monolithic instance of DB server is deployed and running.  

note: for distributed version of the ACID properties, please refer [**`Distributed Transaction`**](https://en.wikipedia.org/wiki/Distributed_transaction)  

Reference:  
1. https://en.wikipedia.org/wiki/ACID

