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

## IAM Access Analyzer

- Find out which resources are shared externally
	- S3 Bucket
	- IAM roles
	- KMS Keys
	- Lambda Functions Layers
	- SQS Queues
	- Secret Manager Secrets

- Define Zone OF Trust = AWS Account or AWS Organization
- Access outside zone of trusts => findings

- IAM Access Analyzer Policy Validation
	-	Validate your policy against IAM policy
	- General warning
	- Provides actionable recommendation

- IAM Access Analyzer Policy Generation
	- Generates IAM policy based on access activity
	- CloudTrail logs is reviewed to generate the policy
	- Review CloudTtrain Logs

## STS

1) Define an IAM Role within your account or cross-account
2) Define which principals can access this IAM Role
3) Use AWS STS (Security Token Service) to retrieve credentials and impersonate the IAM Role you have access to (AssumeRole API)

Which situtations do you want to assume a role with using STS

- Providing access for an IAM user in one AWS account that you own to access resources in another account that you own
- Provide access to IAM users in AWS accounts owned by third parties
- Provide access for services offered by AWS to AWS resources
- Provide access for externally authenticated users
- Ability to revoke active sessions and credentials for a role (by adding a policy using a time statement - AWSRevokeOlderSessions)

### Providing Access to an IAM User in Your or Another AWS Account that you own

- You can grant your IAM users permission to switch to roles within your AWS account or to roles defined in other AWS accounts that you own.

Benefits:
- You must explicity grant your user permission to assume the role.
- Your users must actively switch to the role using the AWS Management Console
- You can add multi-factor (MFA) protection to the role so that only users who sign in with MFA devide can assume the role
- Least privilege + auditing using CloudTrail







