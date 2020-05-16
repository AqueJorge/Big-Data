# Chapter 1

*What are the main characteristics that a big data system should have?*
- Robustness, Low latency, Scalability, Generalization, Ad Hoc querys, Debugging, Minimum Maintenance
 

*When should we consider using Sql or Nosql?*
- If we have a small business we should start with Sql, instead When the data structures we handle are variable, Analysis of large amounts of data in read mode, etc., we should use Nosql


*How does the "sharding" or "horizontal partitioning" in a database?*
- it use multiple database servers and spread the table across all the servers. Each server will have a subset of the data for the table

*What is the diference between vertical scaling and  horizontal scaling?*
- Vertical scalability makes use of hardware to improve performance, instead horizontal scalability involves having multiple servers (known as Nodes) working as a whole

# Chapter 2

*How does the "Lamda Arquitecture" in a database?*
- It consists of creating Big Data systems based on layers: Batch Layer, service layer and speed layer.


- *Batch Layer*: Stores the master copy of the immutable data and pre-computes the batch views using algorithms that can be arbitrarily distributed in a Map-Reduce group that scales according to the number of available nodes.

- *Service layer*: It is a distributed database where batch views that have previously been computed in the batch layer are loaded and allow random readings.

- *Speed layer*: It is in charge of pre-computing views in batches, but of recent data and updates the views in real time. Supporting random writes is more complex than the service layer.

*When we should consider store unstructure data?*
 - If your algorithm for extracting the data is simple and accurate, like extracting an age from an HTML page, you should store the results of that algorithm. If the algorithm is subject to change, due to improvements or broadening the requirements, store the unstructured form of the data.

*Why imnutable data is better than mutable?*
- There are 2 main reasons, Human-fault tolerance( With an immutable data model, no data can be lost) and Simplicity(you only need the ability to append new data units to the master dataset. )

*What are the benefits of the fact-based model*
- Is queryable at any time in its history 
- Tolerates human errors 
- Handles partial information 
- Has the advantages of both normalized and denormalized forms 