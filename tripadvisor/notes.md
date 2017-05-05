Active/Passive Model
Backup datacenter has be invaluable
Stopped having to buy servers by fixing bottlenecks
Disaster recovery is not DR until its able to failover

** System Tuning
- Put WAL, data, and temp partitions onto different disks (even on SSDs)
- IO scheduler _might_ be wrong.  noop for SSD and NS, deadline for spinning arrays
- RAID controller should be dump.  (Write through mode, No Read Ahead)
- Learning `perf`

Wireshare speaks the PG Protocol

Cascading Failures
Work queues need to have detection and response to those sorts of issues
- 500ing a few requests to keep the site up is almost always the right call
- statement_timeout is a _must_
- Separating READ/WRITE connection pools even for one database.


>> https://github.com/mkelleycs/postgres_index_integrity_check
