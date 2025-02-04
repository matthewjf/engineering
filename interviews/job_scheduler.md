![Job Scheduler](images/job_scheduler.png)

# Topics to cover
### Time precision
  - Message queue with built-in delivery delay (SQS)
  - Alternatively, use a sorted set implementation
### 10K jobs per second
  - You can introduce a job queue for creation to handle load spikes
  - DynamoDB with partitions can handle write throughput
  - SQS can handle scaling automatically
  - Long running containers or lambdas for workers
### At least once execution
  - SQS visibility timeout and idempotency
