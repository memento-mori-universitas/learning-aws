# AWS Batch

- Run thousands of containerized batch jobs
- Plans, schedules, and executes your compute workloads.
- Dynamically provisions CPU or memory-optimized compute resources based on needs.
- Runs jobs using ECS, EKS, or Fargate
- Reduce cost by optionally running your jobs using spot instances.

![AWS Batch](../../assets/aws-batch.png)

## Steps for creating a batch

1. Create a Compute Environment: Managed or Unmanaged, Spot or On-Demand, vCPUs
2. Create a Job Queue with priority and assigned to a Compute Environment
3. Create a Job Definition: Script or JSON, env variables, mount points, IAM role, coantainer images, etc.
4. Schedule the Job

### Up next [AWS Step Functions](../aws-step-functions/README.md)...