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
