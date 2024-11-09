# AWS S3

AWS S3 is an object store, first introduced in 2006. The maximum object size is 5TB, with the largest object in a single PUT being 5GB.

It is recommended to use multi-part uploads if the size of the file is larger than 100MB.

As part of the configuration of the services, you can:

- Cross-region replication
- Intelligent Tiering Archive
- Lifecycle Management (which allow you to adhere to data retition policies)
  - Optimize storage costs
- Encryption at Rest
  - SSE-S3 : Use S3’s existing encryption for AES-256
  - SSE-C: Upload your own AES-256 encryption key  which S3 will to write objects
  - SSE-KMS: Use a key generated and managed by AWS Key Management Service
  - Client-side: Encypt objects using your own local encryption process before uploading to S3 (PGP, GPG, etc).
- Integrate into Analytics Capabilities

## Tips and Tricks

1. Transfer Acceleration: Speed up uploads using Cloudfront in reserve.
2. Requester Pays: The request rather than the bucket owner pays for requests and data transfer.
3. Tags: Assign tags to ob# Ajects for use in costing, billing, security, etc.
4. Events: Trigger notifications to SNS, SQS, or Lambda when certain events happen in your bucket
5. Static Web Hosting: Simple and massively scalable static website hosting]

## Managing Permissions in S3

1. Bucket Policies vs IAM
    1. Bucket Policies. Give a particular principle access to all object or a subset of objects in the policy. (Resouce-based)
    2. IAM temporary permission in the form as a role. (Identity-based)
2. Sharing Across Accounts
    1. When connecting across accounts, it is a bit more complex.  On the first AWS account, the bucket policy is not allowed, in the S3 bucket. We have to establish a permission and trust policy. Attached it to the bucket and trust policy which allows an entity from another account to assume that role.
    2. In the second AWS account, we will create a role that gives permission to assume the role that has been granted to that account in the trust policy. Our IAM user, in the second account can assume this role, which allows them to assume the role defined in the first account.
3. Connecting to Resources
    1. Does not have to be a user.
    2. AWS rotates the access key when using IAM
4. Things to Take Away
    1. If we need to connect to a S3 bucket, rather than doing it over an Internet Gateway, we can use an ENI and traverse AWS Private internet. Cost is lower and latency is lower.
