# AWS Certified Solution Architect - Professional (SAP-CO2) Exam Guide

*Reference*: https://d1.awsstatic.com/training-and-certification/docs-sa-pro/AWS-Certified-Solutions-Architect-Professional_Exam-Guide.pdf

The exam has four domains which covers the entirety of the exam.

1. Design Solutions for Organization Complexity

2. Design for New Solutions

3. Continuos Improvement for Existing Solution

4. Accelerate Workload Migration and Modernization.

On the following part of the document, we will review each domain and link to specfic examples.

## Domain 1: Design Solutions for Organization Complexity

### Architect network connectivity strategies. Which requires knowledge in:

1. AWS Global Infrastructure
2. AWS networking concepts
    2.1 For example. Amazon VPC, AWS Direct Connect, AWS VPN, transitive routing, AWS container services
3. Hybrid DNS concepts
	3.1 For example, Amazon Route 53 Resolver, on-premise DNS integration
4. Network segmentation
	4.1 For example, subnetting, IP addressing, connectivity among VPCs
5. Network traffic monitoring

The skills required are:

- Evaluating connectivity options for multiple VPCs
- Evaluating connectivity options for on-premise, co-location, and cloud integration
- Selecting AWS Regions and Availability Zones based on network and latency requirements 
- Troubleshooting traffic flows by using AWS tools
- Using service endpoints for service integrations

### Prescibe security controls. Which requires knowledge in:

1. AWS Identity and Access Management (IAM) and AWS IAM Identity Center (AWS Single-Sign-On)
2. Route tables, security groups, and network ACLs
3. Encryption keys and certificate management
	3.1 For example, AWS Keys Management, AWS Certificate Manager
4. AWS security, identity, and compliance tools (for example, AWS CloudTrail, AWS Identity and Access Management Access Analyzer, AWS Security Hub, Amazon Inspector)

The skills required are:

- Evaluating cross-acount access management
- Integrating with third-party providers
- Deploying encryption strategies for data at rest and data in transit
- Developing a strategy for centralized security event notifications and auditing

### Design reliable and resilient architectures. Which requires knowledge in:

1. Recovery time objectives (RTOs) and recovery point objects (RPOs)
2. Disaster recovery strategies
	2.1 For example, using AWS Elastic Disaster Recovert, pilot light, warm standy, and multi-site
3. Data backup and restoration

The skills required are:

- Designing disaster recovery solutions based on RTO and RPO requirements
- Implementing architecture to automatically recover from failure
- Developing the optimal architecture by considering scale-up and scale-out options
- Designing an effective backup and restoration strategy

### Design a multi-account AWS environment. Which requires knowledge in:

1. AWS Organizations and AWS Control Tower
2. Mult-account even notifications
3. AWS resource sharing across environments

The skills required are:

- Evaluating the most appropirate account structure for organizational requirements
- Recommending a strategy for central logging and event notifications
- Developing a multi-account governance model

### Determine cost optimization and visibility strategies.  Which requires knowledge in:

1. AWS cost and usage monitoring tools (for example, AWS Trusted Advisor), AWS Pricing Calculator, AWS Cost Explorer, AWS Budgets)
2. AWS purchasing options (for example, Reserved Instances, Saving Plans, Spot Instances)
3. AWS rightsizing visibility tools (for example, AWS Compute Optimizer, Amazon S3 Sotrage Lens)

The skills required are:

- Monitoring cost and usage with AWS tools
- Developing an effective tagging strategy that maps cost to business units
- Understanding how purchasing options affect cost and performance

## Domain 2: Design for New Solutions

### Design a deployment strategy to meet business requirements. Which requires knowledge in:

- Infrastructure as code (IaC), for example, AWS CloudFormation
- Continuos integration and Continuos delivery (CI/CD)
- Change management process
- Configuration management tools (for example, AWS Systems Manager)

The skills required are:

- Determing an application or upgrade path for new services and features
- Selecting services to develop deployment strategies and implement appropriate rollback mechanisms
- Adopting managed services as needed to reduce Infrastructure provisioning and patching overhead
- Making advanced technologies accessible by delegating complex development and deployment taks to AWS

### Design a solution to ensure business continuity. Which requires knowledge in:

- AWS Global Infrastructure
- AWS networking concepts (for example, Route 53, routing methods)
- RTOs and RPOs
- Disaster recovery scenarios (for example, backup and restore, pilot light, warm standby, multi-site)
- Distaster recovery solutions on AWS

The skills required are:

- Configuring disaster recovery solutions
- Configuring data and database replication
- Performing distaster recovery testing
- Architecting a backup solution that is automated, is cost-effective, and supports business continuity across multiple Availability Zones or Regions
- Designing an architecture that provides application and Infrastructure Availability in the event of a disruption
- Using processes and components for centralized monitoring to proactively recover from system failures

### Determine security controls based on requirements. Which requires knowledge in:

- IAM
- Route tables, security groups, and network ACLs
- Encryption options for data at rest and data in transit
- AWS service endpoints
- Credential management services
- AWS managed security services (for example, AWS Shield, AWS WAF, Amazon GuardDuty, AWS Security Hub)

The skills required are:

- Specifying IAM users and IAM roles that adhere to the principle of least
privilege access
- Specifying inbound and outbound network flows by using security group
rules and network ACL rules
- Developing attack mitigation strategies for large-scale web applications
- Developing encryption strategies for data at rest and data in transit
- Specifying service endpoints for service integrations
- Developing strategies for patch management to remain compliant with
organizational standards

### Design a strategy to meet reliability requirements. Which requires knowledge in:

- AWS Global Infrastructure
- AWS storage services and replication strategies (for example Amazon S3, Amazon RDS, Amazon ElastiCache)
- Multi-AZ and multi-Region architectures
- Auto scaling policies and events
- Application integration (for example, Amazon Simple Notification Service, Amazon SNS, Amazon SWS, AWS Step Functions)
- Service quotas and limits

The skills required are:

- Designing highly available application environments based on business requirements
- Using advanced techniques to design for failure and ensure seamless system recoverability
- Implementing loosely coupled dependencies
- Operation and mantaining high-availability architectures (for example, application failover, database failover)
- Using AWS managed services for high availability
- Implementing DNS routing policies (for example, Route 53 latency-based routing, geolocation routing, simple routing)

### Design a solution to meet perforance objectices. Which requires knowledge in:

- Peformance monitoring technologies
- Storage options on AWS
- Instance familities and use cases
- Purpose-built databases

The skills required are:

- Designing large-scale application architectures for a variety of access patterns
- Designing an elastic architecture based on business objectives
- Applying design patterns to meet performance objectives with caching, buffering and replicas.
- Developing a process methodology for selecting purpose-built services for required tasks
- Designing a rightsizing strategy

### Determine a cost optimization strategy to meet solution goals and objects. Which requires knowledge in:

- AWS cost and usage monitoring tools (for example, Cost Explorer, Trusted Advisor, AWS Pricing Calculator)
- Pricing model (for example, Reserved Instances, Savings Plans)
- Storage tiering
- Data transfer costs
- AWS managed service offerings

The skills required are:

- Identifying opportunities to select and rightsize infrastructure for cost-effective resources
- Identifying appropriate pricing models
- Performing data transfer modeling and selecting services to reduce data transfer costs
- Developing a strategy and implemeting controls for expenditure and usage awareness

## Domain 3: Continous Improvements for Existing Solutions

### Determine a strategy to improve overall operational excellence. Which requires knowledge in:

- Alerting and automatic remedation strategies
- Disaster recovery planning
- Monitoring and logging solutions (for example Amazon CloudWatch)
- CI/CD pipelines and deployment strategies (for example, blue/geen, all-at-once, rolling)
- Configuration management tools (for example, Systems Manager)

The skills required are:

- Determining the most appropriate logging and monitoring strategy
- Evaluating current deployment processes for improvement opportunities
- Prioritizing opportunities for automation within a solution stack
- Recommending the appropriate AWS solution to enable configuration
management automation
- Engineering failure scenario activities to support and exercise an
understanding of recovery actions

### Determing a strategy to improve security. Which requires knowledge in:

- Data retention, data sensitivity, and data regulatory requirements
- Automated monitoring and remediation strategies (for example, AWS
Config rules)
- Secrets management (for example, Systems Manager, AWS Secrets
Manager)
- Principle of least privilege access
- Security-specific AWS solutions
- Patching practices
- Backup practices and methods

The skills required are:

- Evaluating a strategy for the secure management of secrets and credentials
- Auditing an environment for least privilege access
- Reviewing implemented solutions to ensure security at every layer
- Reviewing comprehensive traceability of users and services
- Prioritizing automated responses to the detection of vulnerabilities
- Designing and implementing a patch and update process
- Designing and implementing a backup process
- Employing remediation techniques

### Determine a strategy to improve performance. Which requires knowledge in:

- High-performing systems architectures (for example, auto scaling, instance
fleets, placement groups)
- Global service offerings (for example, AWS Global Accelerator, Amazon
CloudFront, edge computing services)
- Monitoring tool sets and services (for example, CloudWatch)
- Service level agreements (SLAs) and key performance indicators (KPIs)

The skills required are:

- Translating business requirements to measurable metrics
- Testing potential remediation solutions and making recommendations
- Proposing opportunities for the adoption of new technologies and
managed services
- Assessing solutions and applying rightsizing based on requirements
- Identifying and examining performance bottlenecks

### Determine a strategy to improve reliability. Which requires knowledge in:

- AWS Global Infrastructure
- Data replication methods
- Scaling methodologies (for example, load balancing, auto scaling)
- High availability and resiliency
- Disaster recovery methods and tools
- Service quotas and limits

The skills required are:

- Understanding application growth and usage trends
- Evaluating existing architecture to determine areas that are not sufficiently
reliable
- Remediating single points of failure
- Enabling data replication, self-healing, and elastic features and services

### Identify opportunities for cost optimizations. Which requires knowledge in:

- Cost-conscious architecture choices (for example, using Spot Instances, scaling policies, and rightsizing resources)
- Price model adoptions (for example, Reserved Instances, Savings Plan)
- Networking and data transfer costs 
- Cost Management, alerting and reporting

The skills required are:

- Analyzing usage reports to identify underutilized and overutilized resources
- Using AWS solutions to identify unused resources
- Designing billing alarms based on expected usage patterns
- Investigating AWS Cost and Usage Reports at a granular level
- Using tagging for cost allocation and reporting

## Domain 4: Accelerate Workload Migration and Modernization

### Select existing workloads and process for potential migration. Which requires knowledge in:

- Migration assessment and tracking tools (for example, AWS Migration Hub)
- Portfolio assessment
- Asset planning
- Prioritization and migration of workloads (for example, wave planning)

The skills required are:

- Completeting an application migration assessment
- Evaluating applications according to the seven common migration strategies (7Rs)
- Evaluating total cost of ownership (TCO)

### Determine the optimal migration approach for existing workloads. Which requires knowledge in:

- Data migration options and tools (for example, AWS DataSync, AWS Transfer Family, AWS Snow Family, S3 Transfer Acceleration)
- Application migration tools (for example, AWS Application Discovery Service, AWS Application Migration Service)
- AWS Networking services and DNS (for example, Direct Connect, AWS Site-to-Site VPN, Route53)
- Identify services (for example, IAM Identify Center, AWS Directory Service)
- Database migration tools (for example, AWS Database Migration Service [AWS DMS], AWS Schema Convertion Tool [AWS SCT])
- Governance tools (for example, AWS Control Tower, Organizations)

The skills required are:

- Selecting the appropriate database transfer mechanism
- Selecting the appropriate application transfer mechanism
- Selecting the appropriate data transfer service and migration strategy
- Applying the appropriate security methods to migration tools
- Selecting the appropriate governance model

### Determine a new architecture for existing workloads. Which requires knowledge in:

- Computing service (for example, Amazon EC2, AWS Elastic Beanstalk)
- Containers (for example, Amazong Elastic Container Service [Amazin ECS], Amazon Elastic Kubernetes Service [Amazon EKS], AWS Fargate, Amazon Elastic Container Registry [Amazon ECR])
- AWS storage service (for example, Amazon Elastic Block Store [Amazon EBS], Amazon Elastic File System [Amazon EFS], Amazon FSx, Amazon S3), Volume Gateway
- Database (for example, Amazon DynamoDB, Amazon OpenSearch Service, Amazon RDS, self-managed databases on Amazon EC2)

The skills required are:

- Selecting the appropriate compute platform
- Selecting the appropriate container hosting platform
- Selecting the appropriate storage service
- Selecting the appropriate database platform 

### Determine opportunities for modernization and enhancements. Which requires knowledge in:

- Serverless compute offerings (for example, AWS Lambda)
- Containers (for example, Amazon ECS, Amazon EKS, Fargate)
- AWS storage services (for example, Amazon S3, Amazon EFS)
- Purpose-built database (for example, DynamoDB, Amazon Aurora Serverless, ElastiCache)
- Integration services (for example, Amazon SQS, Amazon SNS, Amazon EventBridge, Step Functions)

The skills required are:

- Identifying opportunties to decouple application components
- Identifying opportunities for serverless solutions
- Selecting the appropriate service for containers
- Identifying opportunities for purpose-built databases
- Selecting the appropriate application integration service