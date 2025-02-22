# DynamoDB Scaling

There are two ways to scale DynamoDB, either provisioning capacity or on-demand capacity.

## Provisioning Capacity

![DynamoDB scaling](../../assets/dynamodb-provisioning-capacity.png)
![DynamoDB scaling](../../assets/dynamodb-terms.png)

You can have two partition calculation (by size or by capacity)

![DynamoDB scaling](../../assets/dynamodb-partition-calculatiosn.png)

For example, if we have 10 GB table and 2,000 Read Capacity Units and Write Capacity Units

![DynamoDB scaling](../../assets/dynamodb-partition-calculations-2.png)
![DynamoDB scaling](../../assets/dynamodb-partition-example.png)

AWS does allow Burst Capacity against a single partition but it is not recommended.

**DynamoDB Stores Data**

- How to land hashes on the different partitions
- The partition key gets translated into a hash value
- If we have one partition, all the data is going to land on the same partition

If we have two partition or three then it DynamoDB splits them equally

![DynamoDB scaling](../../assets/dynamodb-stores-data.png)

## Use Case: Getting data from sensors

1. Hot Partition or hot key issue

![DynamoDB scaling](../../assets/dynamodb-use-case.png)

2. Better way to structure would be to have the partition key by sensor_id

![DynamoDB scaling](../../assets/dynamodb-use-case-2.png)
![DynamoDB scaling](../../assets/dynamodb-use-case-arch.png)

## Key things

- Using Target Tracking method to try to stay close to target utilization
- Currently does not scale if table’s consumption drops to zero
- Also supports Global Secondary Index

On demand scaling is

- Alternative to Autoscaling
- Cost more
- Instantly allocated capacity

## DynamoDB Accelerator - in memory cache

![DynamoDB scaling](../../assets/dynamodb-dax.png)
![DynamoDB scaling](../../assets/dynamodb-dax-uses.png)

### [CloudFront Part Two](../cloudfront-part-2/README.md)...
