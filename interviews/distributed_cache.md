![Distributed Cache](images/distributed_cache.png)

# Topics to cover

- Handle TTL
  - Backgrond process to clean up expired keys
- LRU eviction
  - Hashmap and linked list
- Availability and fault tolerance
  - Sync or async replication
  - Quorums
- Scalability
  - Shard or partition keys
  - Consistent hashing
- Hot keys
  - Copy to mutiple shards for reads
  - Batch updates or split the key across partitions (e.g. counter)
- Node failures
  - Gossip or coordinator (e.g. zookeeper)
