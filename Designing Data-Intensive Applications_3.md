# What is a hash?
- For a long time DBAs have been encouraged to use variations on the YAPP method of performance tuning, which focuses on wait event monitoring, rather than hit ratios. Tools like Statspack, AWR, ADDM and SQL Trace are all very useful for gathering wait event information during tuning, but they tend to focus on looking back at what has happened, rather than what is currently happening. The [G]V$ dynamic performance views provide masses of real-time information, but it can be difficult for beginners and experienced people alike to make good use of this information.

# What is a hash index?
- A hash index is an array of N buckets or slots, each one containing a pointer to a row. Hash indexes use a hash function F(K, N) in which given a key K and the number of buckets N , the function maps the key to the corresponding bucket of the hash index. I want to emphasize that the buckets do not store the keys or its hashed value. They only store the memory address in which the data is placed.

# What is a hash function?
- A hash function is any algorithm that maps data of variable length to data of a fixed length in a deterministic and close to random way. 

# What is a SSTable?
- SSTable (engl. Sorted Strings Table) is a file of key/value string pairs, sorted by keys.

- An SSTable provides a persistent,ordered immutable map from keys to values, where both keys and values are arbitrary byte strings.

- Internally, each SSTable contains a sequence of blocks (typically each block is 64KB in size, but this is configurable).

# LSMtree and B-Tree
LSM-Trees and B-Trees are the two primary data structures used as storage engines in modern key-value (KV) stores. These two structures are optimal for different workloads; LSM-Trees perform better on update queries, whereas B-Trees are preferable for short range lookups. KV stores today use one or the other. However, for modern applications with increasingly diverse workloads, limiting KV stores to utilize only one of the two designs leads to a significant loss in performance. We propose a novel method of online transitioning a KV store from an LSM-Tree to a B-Tree and vice versa. This allows KV stores to smoothly adapt to changing workloads and use the optimal data structure as the workload changes

# What does mean LSMtree and what is it?
- In computer science, the log-structured merge-tree (or LSM tree) is a data structure with performance characteristics that make it attractive for providing indexed access to files with high insert volume, such as transactional log data. LSM trees, like other search trees, maintain key-value pairs. LSM trees maintain data in two or more separate structures, each of which is optimized for its respective underlying storage medium; data is synchronized between the two structures efficiently, in batches.

# What is a B-Tree?
- B-tree is a self-balancing tree data structure that maintains sorted data and allows searches, sequential access, insertions, and deletions in logarithmic time. The B-tree generalizes the binary search tree, allowing for nodes with more than two children.[2] Unlike other self-balancing binary search trees, the B-tree is well suited for storage systems that read and write relatively large blocks of data, such as discs. It is commonly used in databases and file systems.

