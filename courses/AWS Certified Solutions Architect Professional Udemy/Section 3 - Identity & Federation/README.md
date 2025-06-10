# Identity & Federation

Roles:
- Short-term credentials
- EC2 Instances Roles
- Service Roles
- Cross Account Role

Policies:
- AWS Managed
- Customer Managed
- Inline Policies
- Resource Based Policies

## IAM Policies Deep Dive

- Anatomy of a policy: Action, Resource, Conditions, Policy Variables
- Explit DENY has precendence over ALLOW
- IAM Access Adivisor: See permissions granted and when last accessed
- IAM Access Analyzer: Analyze resource that are shared with external entity

## IAM AWS Managed Policies 

- Administrator Access: Everything will be allowed
- PowerUserAccess: Not going to allow IAM, organizations & account

<img width="726" alt="Image" src="https://github.com/user-attachments/assets/5d1b8413-431f-4868-86a1-55e147e6389d" />

Note how we dont use Deny, since if we use an explicity Deny, it will automatically Deny the list on the right.

## IAM Policies Conditions

- Operations:
  - String Operator: `{"StringEquals": {"aws:PrincipalTag/job-category": "iamuser-admin"}}`
  - Numeric
  - Date
  - Boolean
  - (Not)IPAddress: ensure only an specific kind of source can access the service
  - ArnEquals
  - Null

## IAM Policies Variables and Tags

Example: `${aws:username}`

AWS Specific:
- aws:CurrentTime
- aws:TokenIssueTime
- aws:principaltype
- aws:SecureTransport
- aws:SourceIP
- aws:userid
- ec2:SourceInstanceARN

Service Specific
- s3:prefix
- s3:max-keys
- s3:x-amz-acl
- sns:Endpoint
- sns:Protocol

Tag Based
- iam:ResouceTag/key-name
- aws:PrincipalTag/key-name

## IAM Roles vs Resource Based Policies 

<img width="791" alt="Image" src="https://github.com/user-attachments/assets/2bc74fb4-4d5c-4d0f-8c90-3094a3e1a9d2" />

Key differences: 

- When you assume a role (user, application or service), you give up your orginal permissions and take the permissions assigned to the role.
- When using a resource-based policy, the principal doesn't have to give up any permissions

Example: User is account A needs to scan a DynamoDB table in Accout A and dump it in an S3 bucket in Account B.

## IAM Permission Boundaries

- IAM Permission Boundaries are supported for user and roles (not groups)
- Advanced feature to use a managed policy to set the maximun permissions an IAM entity can get.

<img width="973" alt="Image" src="https://github.com/user-attachments/assets/e7204187-fea1-49ca-b8fc-7260ab02eec5" />

