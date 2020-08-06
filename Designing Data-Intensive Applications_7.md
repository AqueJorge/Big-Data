# What is a transaction?
A transaction in a Database Management System is a set of orders that are executed as a unit of work, that is, in an indivisible or atomic form. A transaction must have ACID

# What is isolation?
In computer security, the isolation of processes or isolated environment is a mechanism to execute programs safely and separately. It is often used to run new code, or dubious reliability software from third parties.

# Why is a transaction abortion not entirely perfect?
- If the transaction actually succeeded, but the network failed while the server tried to acknowledge the successful commit to the client (so the client thinks it failed), then retrying the transaction causes it to be performed twice — unless you have an additional application- level deduplication mechanism in place.
- If the error is due to overload, retrying the transaction will make the problem worse, not better. To avoid such feedback cycles, you can limit the number of retries, use exponential backoff, and handle overload-related errors differently from other errors (if possible). • It is only worth retrying after transient errors (for example due to deadlock, isolation violation, temporary network interruptions, and failover); after a permanent error (e.g., constraint violation) a retry would be pointless.
- If the transaction also has side effects outside of the database, those side effects may happen even if the transaction is aborted. For example, if you’re sending an email, you wouldn’t want to send the email again every time you retry the transaction. If you want to make sure that several different systems either commit or abort together, two-phase commit can help.

# What is a dirty reading?
A dirty read occurs when a transaction is allowed to read a row that has been modified by another concurrent transaction but has not yet been committed.

# What is a snapshot?
In computing, a volume snapshot or snapshot is a snapshot of the state of a system at a given time.

#What is Serializability?
Serializability is the classical concurrency scheme. It ensures that a schedule for executing concurrent transactions is equivalent to one that executes the transactions serially in some order. It assumes that all accesses to the database are done using read and write operations.
