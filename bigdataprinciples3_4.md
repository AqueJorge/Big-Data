# Chapter 3
## How is the workhorses of thrift composed?
- Primitive data types (strings, integers, longs, and doubles)
- Collections of other types (lists, maps, and sets)
- Other structs and unions

## What are the thrift-like tools that the book mentions?
- Protocol Buffers and Avro

## What is serialization?
- It consists of a process of encoding an object on a storage medium in order to transmit it through a network connection as a series of bytes or in a format humanly more readable as XML or JSON, among others

## What is apache trhift?
- Is a binary communication protocol and interface definition language. It is used to define and create services for numerous languages. It forms a remote procedure call framework and was developed in Facebook for "scalable development of multi-language services".

# Chapter 4

## What is the master database?
- The master database is the main configuration database in SQL Server. Contains information about all the databases that exist on the server, including the physical database files and their locations. The master database also contains SQL Server configuration and login account information.

## What is the distributed file system?
- It is a method to access and access files in a client / server architecture. In a distributed file system, one or more central servers store files that can be accessed, with appropriate authorization rights, by any number of remote clients on the network.

## Why is it recommended to partition data?
- Improve scalability: By vertically scaling a single database system, you could hit a physical hardware limit.
- Improve performance. Data access operations on each partition are performed on a smaller data volume.
- Improve security. In some cases, you can separate confidential and non-confidential data in different partitions and apply different security controls to confidential data.
- They provide operational flexibility. Partitioning offers many opportunities to fine-tune operations, maximize administrative efficiency, and reduce costs.
- Improve availability. Separating data across multiple servers avoids a single point of failure. If an instance fails, only the data for that partition is no longer available.

## What is the vertical partition?
- Vertical partitioning. In this strategy, each partition contains a subset of the data warehouse item fields. The fields are divided according to their usage pattern. For example, fields that are frequently accessed may be placed in one vertical partition and fields that may be used more rarely in another.