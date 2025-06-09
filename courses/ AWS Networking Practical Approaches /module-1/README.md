# Practical Approaches - Network Design Best Practices

## Amazon VPC

"An Amazon VPC is not a data center and it shoul not be treated as one"

An Amazon VPC is a software-define network. The AWS Well-Architected Framework has six pillars that can help you follow best practices for your AWS environment, not just your network.

ON AWS, networking in virtualized and is available in a number of different types and configurations which helps to match your networking methods with your needs.

### Product Features

#### Optimizing your network

- Amazon EBS-optmized instances
- Amazon S3 Acceleration
- Amazon CloudFront

#### Reducing network distance and jitter

- Amazon Route 53 Latency routing
- Amazon VPC endpoints
- AWS Global Accelerator

### Data Layer

The data layer of your networking environment is important because it provides a data path for network traffic between applications hosted on AWS and an on-premises data center. The Hybrid Networking Lens recommends using AWS Virtual Private Network, AWS Direct Connect, and Amazon VPC to support your application team's agility and speed to market by using AWS as a data center extension.

### Monitoring Layer

AWS provides the following monitoring and config management services. 

- Amazon CloudWatch 
- AWS Personal Health Dashboard 
- VPC Reachability Analyzer 
- Transit Gateway Network Manager (Network Manager) 
- Route Analyzer, part of Transit Gateway Network Manager 
- AWS Config 

### Security Layer

The following features and services can help secure your hybrid networking environment on AWS.

- Security groups 
- Network access control lists (network ACLs) 
- AWS Network Firewall 
- AWS CloudTrail 
- Amazon GuardDuty

### Management and Governance Lens (M&G Lens)

This lens provides networking and security architects with additional guidance to configure your baseline and the design of your network.


## Operational Excellence

- Choose a CIDR block for your network design. [AWS VPC IP Address Manager](https://docs.aws.amazon.com/vpc/latest/ipam/what-it-is-ipam.html) is a feature of Amazon VPCs to help plan, track, and monitor IP addresses.
- Efficient routing: A well-defined IP address allocation scheme creates efficient routing where you can summarize routes based on a network boundary.

For example, if you are hosting workloads in Amazon VPCs in us-east-1, you can allocate CIDR ranges to these Amazon VPCs from a defined block such as 10.1.1.0/22. Then configure the Direct Connect Gateway associated with the transit gateway to advertise this CIDR block over a transit virtual interface instead of advertising individual prefixes associated with individual Amazon VPCs. 

A well-defined IP address allocation scheme reduces the risk of overlapping CIDR ranges between you Amazon VPC and on premises networks. Avoid re-using the same CIDR range between your on premises and Amazon VPC network because overlapping CIDR ranges will make host-to-host communication very difficult.

- It is best practice to keep track of the IP prefixes you currently have and allocate CIDR ranges for your deployment in a systematic manner.

- Prefix lists help to group multiple CIDR blocks into a single object, and use it as a reference to simplify network configuration.

- You can share your prefix list with other AWS accounts using Resource Access Manager (RAM) and use it to configure Amazon VPC route tables, security groups, and transit gateway route tables.

### 🔐 Real-life Analogy: The VIP Guest List at a Club

Imagine you run a high-end nightclub. You have bouncers (like firewalls/security groups) who decide who can enter.

But instead of giving the bouncers a long list of individual names every night, you say:

“Just let in everyone on the VIP list.”

Now, the VIP list is managed somewhere central. You can update it anytime, and the bouncers always check the latest version.

⸻

In AWS Terms
	•	🏢 Club = Your VPC (network environment)
	•	🚪 Bouncer = Security group or route table rule
	•	📃 VIP List = Prefix list
	•	👥 People’s names = IP address ranges (CIDR blocks)
	•	✏️ List manager = You or AWS (depending on whether it’s customer-managed or AWS-managed)

⸻

How It Helps
	•	Instead of writing dozens of IP addresses in your firewall or route rules, you just reference the VIP list (the prefix list ID).
	•	You can reuse this list across multiple clubs (VPCs or subnets).
	•	Updating the VIP list updates all rules using it — no need to change each bouncer’s list manually.

⸻

Example

Let’s say your company has 5 office IP ranges. Instead of copying those into every security rule:

You create a prefix list named CompanyOffices, and put those 5 CIDRs in there.

Then in your security groups:

You say: “Allow access from CompanyOffices”
(really, from the prefix list ID like pl-123abc)

Later, if your company adds a 6th office?

Just update the prefix list. No need to touch the security groups — they’ll automatically apply the new rule.



## Resources:

- https://docs.aws.amazon.com/pdfs/wellarchitected/latest/hybrid-networking-lens/hybrid-networking-lens.pdf#hybrid-networking-lens
- https://docs.aws.amazon.com/pdfs/wellarchitected/latest/management-and-governance-guide/management-and-governance-cloud-environment-guide.pdf#management-and-governance-cloud-environment-guide
- https://docs.aws.amazon.com/pdfs/whitepapers/latest/overview-aws-cloud-adoption-framework/overview-aws-cloud-adoption-framework.pdf#introduction
- https://docs.aws.amazon.com/whitepapers/latest/overview-aws-cloud-adoption-framework/introduction.html
- https://docs.aws.amazon.com/wellarchitected/latest/operational-excellence-pillar/welcome.html
