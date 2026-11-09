# 01 — AWS Cloud Infrastructure

> **Status:** Planned
> **Environment:** [AWS Academy Learner Lab or personal account — to be decided]
> **Estimated cost:** $0 in a sandbox. In a personal account: stay within free tier, **no NAT Gateway**, delete public IPv4 addresses/Elastic IPs when done.
> **Last updated:** 2026-11-04

## 1. Objective
Build and document a small, secure AWS environment: a custom VPC, an EC2 web server reachable without SSH keys, an S3 bucket with least-privilege access, and CloudWatch monitoring.

## 2. Problem Being Addressed
Companies need workloads isolated in their own network, with access granted only to what each identity needs. This project shows the baseline every cloud environment starts from.

## 3. Architecture
_Diagram to be added: `diagrams/architecture.svg`_

Planned components: VPC (2 AZs) · public + private subnets · internet gateway · route tables · security groups · EC2 instance with IAM instance profile · S3 bucket (Block Public Access, encryption, versioning) · CloudWatch alarm.

## 4. Technologies Used
| Technology | Purpose in this project |
|---|---|
| Amazon VPC | Network isolation and routing |
| Amazon EC2 | Web server |
| AWS Systems Manager Session Manager | Shell access without open SSH ports |
| Amazon S3 | Private object storage |
| AWS IAM | Instance role with least-privilege S3 access |
| Amazon CloudWatch | CPU alarm and logs |

## 5. Implementation Steps
_To be written while building._

## 6. Evidence
_Screenshots to be added._

## 7. Challenges
_To be written._

## 8. What I Learned
_To be written._

## 9. Future Improvements
- Rebuild with Terraform (see [Project 05](../05-terraform-aws-environment/)).

## 10. Cleanup
- [ ] Terminate EC2 instance
- [ ] Release Elastic IPs / public IPv4 addresses
- [ ] Empty and delete S3 bucket
- [ ] Delete CloudWatch alarms
- [ ] Delete VPC (subnets, route tables, internet gateway)
