# Business Continuity

- Design Solutions for Organizational Complexity and Design for New Solutions
  - Recovery time objectives (RTOs) and recovery point objects (RPOs)
  - Disaster recovery strategies (for example, using AWS Elastic Disaster Recovery [CloudEndure Disaster Recovery], pilot light, warm standby and multi-site)
  - Data backup and restoration
- Continuous Improvement for Existing Solutions
  - Disaster recovery plan
  - Backup practices and methods
  - High availability and reliability
- Accelerate Workload Migration and Modernization
  - AWS networking services and DNS ( Direct Connect, AWS Site-to-Site VPN, Route53)

## AWS S3 Incident 2017

![Business Continuity](../../assets/business-continuity-s3.png)
![Business Continuity](../../assets/bc-dr.png)

- Fault tolerant is the ability to tolerate fault.
- High availability leaves room for unplanned downtime as high available does not mean always available

![Business Continuity](../../assets/business-continuity-sla.png)
![Business Continuity](../../assets/business-continuity-rto-vs-rpo.png)
![Business Continuity](../../assets/business-continuity-timeline.png)
![Business Continuity](../../assets/business-continuity-plan.png)

## Disaster Category

![Business Continuity](../../assets/disaster-recovery.png)

## Disaster Recovery Architectures

Four basic disaster recovery architectures that AWS talks about.

![Business Continuity](../../assets/disaster-recovery-architecture.png)

### Backup and Restore

![Business Continuity](../../assets/dr-backup-and-restore.png)

### Pilot Light

![Business Continuity](../../assets/dr-pilot-light.png)

### Warm Standby

![Business Continuity](../../assets/dr-warm-standby.png)

### Multi-Site

![Business Continuity](../../assets/dr-multi-site.png)

DNS records do usually have a time to live, so there might be customer impact until the DNS entry pointing to the fail site expires.

### Up next [Storage High Availability](./storage-high-availability/README.md)...
