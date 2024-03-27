## Description
This toy project implements four key components of a database system.

## Key Components
- storage_mgr.h
The storage manager deals with pages (blocks) of fixed size (PAGE SIZE). In addition to reading and writing pages from a file, it provides methods for creating, opening, and closing files.
- buffer_mgr.h
The buffer manager manages a fixed number of pages in memory that represent pages from a page file managed by the storage manager.
The memory pages managed by the buffer manager are called page frames or frames for short. We call the combination of a page file and the page frames storing pages from that file a Buffer Pool.
- record_mgr.h
The record manager handles tables with a fixed schema. Clients can insert records, delete records, update records, and scan through the records in a table.
A scan is associated with a search condition and only returns records that match the search condition. Each table should be stored in a separate page file and your record manager should access the pages of the file through the buffer manager implemented in the last assignment.
- btree_mgr.h
BTree manager handles the B+ tree index.