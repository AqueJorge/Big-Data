# What does means "replication"?
-  Means keeping a copy of the same data on multiple machines that are connected via a network.

# what are some reasons to replicate data?
- To keep data geographically close to your users (and thus reduce latency)
- To allow the system to continue working even if some of its parts have failed
(and thus increase availability)
- To scale out the number of machines that can serve read queries (and thus
increase read throughput)

# What is a "replica" and how do we ensure that all the data ends up on all the replicas?
- Each node that stores a copy of the database is called a replica, Every write to the database needs to be processed by every replica; otherwise, the rep‐
licas would no longer contain the same data. The most common solution for this is
called leader-based replication 

# An automatic failover process usually consists of the following steps:

1 - Determining that the leader has failed. There are many things that could poten‐
tially go wrong: crashes, power outages, network issues, and more. There is no
foolproof way of detecting what has gone wrong, so most systems simply use a
timeout: nodes frequently bounce messages back and forth between each other,
and if a node doesn’t respond for some period of time—say, 30 seconds—it is
assumed to be dead. (If the leader is deliberately taken down for planned mainte‐
nance, this doesn’t apply.)

2 - Choosing a new leader. This could be done through an election process (where
the leader is chosen by a majority of the remaining replicas), or a new leader
could be appointed by a previously elected controller node. The best candidate for
leadership is usually the replica with the most up-to-date data changes from the
old leader (to minimize any data loss). 

3 - Reconfiguring the system to use the new leader. Clients now need to send
their write requests to the new leader (we discuss this in “Request Routing” on
page 214). If the old leader comes back, it might still believe that it is the leader,
not realizing that the other replicas have forced it to step down. The system
needs to ensure that the old leader becomes a follower and recognizes the new
leader.

# What is a WAL and how it works?
Write-Ahead Logging (WAL) is a standard method for ensuring data integrity. A detailed description can be found in most (if not all) books about transaction processing. Briefly, WAL's central concept is that changes to data files (where tables and indexes reside) must be written only after those changes have been logged, that is, after log records describing the changes have been flushed to permanent storage. If we follow this procedure, we do not need to flush data pages to disk on every transaction commit, because we know that in the event of a crash we will be able to recover the database using the log: any changes that have not been applied to the data pages can be redone from the log records. (This is roll-forward recovery, also known as REDO.)

# What is Trigger-based replication?
- To implement trigger-based replication, use event triggers stored in the database. When an event to be replicated occurs (that is, a record is created, modified, or deleted) the database uses the event to record the change in a replication change log. ABL (Advanced Business Language) provides full support for trigger-based replication.
