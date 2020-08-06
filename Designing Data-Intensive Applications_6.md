# What are the advantages and disadvantages of a fixed partition?
Advantage:

- Simplicity
- Address resolution in load time
- Base registration (does not even require a limit registration)
- It can be limited simply with a suitable address space in the compiler.

Disadvantages

- stiffness
- Limited multiprocessing degree
      - If there are less than 7 processes, resources are wasted.
      - If there are more than 7, they have to wait for space to open for them.
- Waste of space (internal fragmentation)
    - By allocating memory in fixed blocks, a small process could waste a lot of space

# What are the advantages and disadvantages of a dynamic calving?
Advantage:
- There is no internal fragmentation

Disadvantages:
- external fragmentation, memory must be compacted. Compacting takes time.

# What is relocation?
Relocation only exists on dynamic partitions.
With this memory allocation scheme, the memory manager relocates programs to collect empty blocks and compact them, to make a memory block large enough to accept some or all tasks waiting to enter.
The relocation happens for 3 instances:
- Weather
- Number of queued tasks
- Percentage of how memory is occupied

# What is pagination?
Paging consists of dividing the memory into a set of frames of equal size, each process is divided into a series of pages the size of the frames, even the space for the operating system is also paged, a process is loaded in the frames that require (all pages), not necessarily contiguous ie followed.

# What is a parallel query?
Parallel query is a method used to increase the execution speed of SQL queries by creating multiple query processes that divide the workload of a SQL statement and executing it in parallel or at the same time.

# What are some partitioning methods and how do they work?
- Range partitioning: A table that is partitioned by range is partitioned in such a way that each partition contains rows for which the partitioning expression value lies within a given range. Ranges should be contiguous but not overlapping, and are defined using the VALUES LESS THAN operator.
- LIST partitioning: is similar to range partitioning in many ways. As in partitioning by RANGE, each partition must be explicitly defined. The chief difference between the two types of partitioning is that, in list partitioning, each partition is defined and selected based on the membership of a column value in one of a set of value lists, rather than in one of a set of contiguous ranges of values. This is done by using PARTITION BY LIST (expr) where expr is a column value or an expression based on a column value and returning an integer value, and then defining each partition by means of a VALUES IN (value_list), where value_list is a comma-separated list of integers.
- Hash partitioning: Partitioning by HASH is used primarily to ensure an even distribution of data among a predetermined number of partitions. With range or list partitioning, you must specify explicitly into which partition a given column value or set of column values ​​is to be stored.
- KEY partitioning: Each row in a partitioned table is unambiguously assigned to a single partition. The partitioning key consists of one or more columns that determine the partition where each row is stored.
