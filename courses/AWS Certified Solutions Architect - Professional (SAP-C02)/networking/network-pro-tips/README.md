# Networking Pro Tips

## Exam Tips

- Know the pros and cons of each on-prem to AWS connection mode
- Know the functions of the different VPC components (Customer Gateway, Virtual Private Gateway)
- Know that Direct Connect is not inherently redundant, so know how to architect a network that is (VPN, secondary direct connect)
- Know what is meant by “Stateless”, “stateful”, “connectionless” and “Connection-based” in terms of IP protocols
- Know what ephemeral ports are and why they might need to be in NACLs or SGs.

Routing

- Understand BGP and how to use weighting to shift network traffic.
- Know how routes in a route table are prioritized (most specific first)
- What other routing protocols does AWS support (none…only BGP)

VPC Peering

- CIDR ranges cannot overlap
- After VPC owner accepts a peering request, routes must be added to respective route tables
- Transitive peering id not supported, but mesh or hub-and-spoke architectures are…with proper NACLs and routes
- A Transit VPC is supported

Internet Gateways

- Different between a NAT instance and NAT Gateway
- Internet Gateway is horizontally scaled, redundant, with no bandwidth constraints
- NATs do have bandwidth contraints but
- VPCs can have multiple NATs across AZs and subnets for scale - so long as routes are defined properly
- Use Egress-Only Gateway for IPVs

Route 53:

- Understand different types of routing policies and use cases
- Know the Weighted Routing Formula
- Route 53 is a global service

CloudFront:

- Understand what must happen to use a custom domain with CloudFront
- Understand what SNI enables and the necessary alternative

Elastic Load Balancer:

- Know the three different types of Load Balancers and at which OSI Layer they work
- Understand which major features each deliver (protocol, SNI, Sticky Sessions)
- Know what sticky sessions are and when they come into play.

## Pro Tips

- Direct Connect may be a more complex and costlier option to setup, but it could save big on bandwidth cost.
- Explicit denies with NACLs. With SGs, you allow the traffic you want, and the final implicit deny rule takes care of the rest.
- Thinking through your VPC Layout.
- You can use Route 53 for your domain even if AWS isn’t your registrar.
- ELBs provide a useful layer of abstractions (Route53 as well).

[![AWS re:Invent 2017: Networking Many VPCs: Transit and Shared Architectures (NET404) ](https://www.youtube.com/watch?v=KGKrVO9xlqI)](https://www.youtube.com/watch?v=KGKrVO9xlqI)

### Up next [Network Challenge](../network-challenge/README.md)...
