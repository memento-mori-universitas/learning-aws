# Deployment and Operations Management

- Undestand IAC
- CI / CD
- AWS Systems Manager

## Types of Deployments

![deploy-and-ops-mgmt](../assets/deployment-types.png)

### Rolling Deployments

![deploy-and-ops-mgmt](../assets/deployment-rolling.png)

### A/B Testing

![deploy-and-ops-mgmt](../assets/deployment-ab-testing.png)

### Canary Release

![deploy-and-ops-mgmt](../assets/deployment-canary.png)

### Blue / Green Deployment

![deploy-and-ops-mgmt](../assets/deployment-blue-green.png)

- Update DNS with Route53 to point to a new ELB or instances
- Swap Auto-scaling Group already primed with new version instances behind the ELB
- Change Auto-Scaling Group Launch Configuration to use new AMI version and terminate old instances
- Swap environment URL of Elastic Beanstalk
- Cline stack in AWS OpsWorks and update DNS
- Blue Green Contraindication (Anti-patterns)
  - Data store schema is too tightly coupled to the code change
  - Update requires special upgrade routines to be run during deployment
  - Off-the-shelf products might not be blue-green deployment

## Deploying Infrastructure

- CI: Merge code changes back to main branch as frequently as possible
- CD: Automate your release process with the click of a button
- Continuous Deployment: Each code change triggers a series of automated release stages
- AWS Services

![deploy-and-ops-mgmt](../assets/deploying-infra-options.png)

## Example Pipeline

![deploy-and-ops-mgmt](../assets/deployment-example-pipeline.png)

## Multi-Account Pipeline

![deploy-and-ops-mgmt](../assets/deployment-multi-account-pipeline.png)

## Other CI/CD Services

![deploy-and-ops-mgmt](../assets/deployment-other-services.png)

### Up next [Deployment Management Services](../deployment-and-operations-mgmt/deploy-services/README.md)...