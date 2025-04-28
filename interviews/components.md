# Components

## Search
- Dedicated search engine like Elasticsearch
- Supports full text search using inverse indices
- Supports geospatial data
- **Change data capture** (e.g. debezium)
  - Read from write-ahead-log and send to event stream.

## Counter
- Postgres has support for atomic increments with **serializable snapshot isolation**
  - Example: `UPDATE users SET login_count = login_count + 1 WHERE id = 42;`
  - This works so long as you don't read the current value in the same transaction
- Redis has a counter data structure with atomic increments

## Geospatial data
- Elasticsearch and Postgres support geospatial indices
- Elasticsearch and Postgres support geospatial polygon data
- Index options are Quadtree, Geohash, Google S2

## Replication
- Asynchronous replication
  - Some web frameworks will pin a request to master shard when a write occurs. For this to be effective, traffic must be read heavy.
- Quorum writes
  - R+W>N can guarantee to read your own writes. This can be effective when using a DB like Dynamo.

## Event Streams / Message Queues
- Kafka can do both
  - Kafka doesn't support retries out of the box. SQS supports retries and a dead letter queue. 
- Kinesis vs SQS
  - Kineses for real time event processing.
- Redis also has pub/sub
  - Good for pushing realtime updates but not source of truth.
