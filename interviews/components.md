# Components

## Search
- Dedicated search engine like Elasticsearch
- Supports full text search using inverse indices
- Supports geospatial data
- Change data capture (e.g. debezium): read from WAL send to event stream

## Counter
- Postgres has support for atomic increments with serializable snapshot isolation
- Redis has a counter data structure with atomic increments

## Geospatial data
- Elasticsearch and Postgres support geospatial indices
- Elasticsearch and Postgres support geospatial polygon data

## Replication
- Asynchronous replication
- Quorum writes

## Event streams and message queues
- Kafka can do both
- Kinesis vs SQS
