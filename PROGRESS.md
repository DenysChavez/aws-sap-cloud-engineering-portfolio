# Learning Progress

Weekly log of study hours, hands-on work, and evidence. Updated every Sunday.

## Summary

| Metric                   | Count                                                |
| ------------------------ | ---------------------------------------------------- |
| Weeks logged             | 3                                                    |
| Total study hours        | 26                                                   |
| AWS labs documented      | 3 (account security, IAM least privilege, VPC)      |
| SAP BTP topics studied   | 2 (BTP Fundamentals Level 1 & 2)                     |
| Projects verified ✅     | 0 / 5                                                |
| Certifications           | 0                                                    |
| Badges                   | 2 (SAP Learning course-completion badges, June 2026) |
| LinkedIn posts published | 5                                                    |

## Weekly log

### Week 3 — 2026-11-21

- **Hours:** 8
- **Focus:** VPC networking: public and private subnets across two Availability Zones
- **Done:**
  - Planned the IP ranges first: `lab-vpc` 10.0.0.0/16 with two public (10.0.1.0/24, 10.0.2.0/24) and two private (10.0.11.0/24, 10.0.12.0/24) subnets in us-east-1a and us-east-1b
  - Built the whole network from the AWS CLI, saving resource IDs to an `ids.env` file
  - Internet gateway `lab-igw`; `lab-public-rt` routes `0.0.0.0/0` to it, `lab-private-rt` is local only; the main route table is local only, so a new subnet is private by default
  - Security groups: `lab-web-sg` (HTTP 80 from anywhere, no SSH) and `lab-app-sg` (TCP 8080 only from `lab-web-sg`)
  - Network ACL `lab-private-nacl` on both private subnets: allows only the VPC CIDR, inbound and outbound
  - Verified with the CLI route check and the VPC resource map; no NAT gateway and no network interfaces in the VPC ($0)
  - Architecture diagram in draw.io
- **Evidence added:** [`technical-notes/vpc-public-private-subnets.md`](technical-notes/vpc-public-private-subnets.md), 5 redacted screenshots in [`technical-notes/images/week-03/`](technical-notes/images/week-03/), diagram [`architecture-diagrams/week-03-lab-vpc.svg`](architecture-diagrams/week-03-lab-vpc.svg) (source `.drawio` alongside)
- **Blockers:** None
- **Next week:** EC2 and Linux: launch a web server into `lab-public-a` with `lab-web-sg`

### Week 2 — 2026-11-14

- **Hours:** 10
- **Focus:** IAM least privilege: policies, roles, permissions boundaries
- **Done:**
  - Customer-managed policy limited to `s3:ListBucket` + `s3:GetObject` on one lab bucket
  - Role for a person (trusted by `denys-admin`) and role for a service (trusted by `ec2.amazonaws.com`, with instance profile), sharing the same permissions policy
  - IAM Policy Simulator and real CLI calls as the assumed role agreed on all 5 tested actions (2 allowed, 3 implicit deny)
  - Permissions boundary capped the test role to `s3:ListBucket`: `GetObject` denied even though the policy allows it (policy ∩ boundary)
  - Lab bucket deleted after testing
- **Evidence added:** [`technical-notes/iam-least-privilege-s3.md`](technical-notes/iam-least-privilege-s3.md), 4 policy files in [`technical-notes/policies/week-02/`](technical-notes/policies/week-02/), 13 redacted screenshots + 4 diagrams in [`technical-notes/images/week-02/`](technical-notes/images/week-02/)
- **Blockers:** None
- **Next week:** VPC and networking: public and private subnets, route tables

### Week 1 — 2026-11-08

- **Hours:** 8
- **Focus:** AWS account security and tooling
- **Done:**
  - Root user secured with two MFA devices (passkey + authenticator app); no root access keys
  - Budget `monthly-lab-budget` ($5/month) with alerts at 85% and 100% actual, plus a forecast alert
  - `Administrators` group (AdministratorAccess) and IAM user `denys-admin` with MFA; account alias set
  - AWS CLI signs in with `aws login` (short-term credentials, no access keys stored on the laptop)
  - Audit: CloudTrail `CreateUser` event reviewed; IAM Access Analyzer (external access) shows 0 findings
  - Cleaned up leftover resources from an old project (EC2 instance, AWS Backup plan and recovery points, S3 bucket, SNS topic, CloudWatch alarm, log group, VPC, IAM roles and instance profile)
  - Deleted an old IAM user with a long-term access key; its policy review found a privilege-escalation path (`CreateRole` + `AttachRolePolicy` + `PassRole` with no conditions)
- **Evidence added:** [`technical-notes/securing-a-new-aws-account.md`](technical-notes/securing-a-new-aws-account.md), 8 redacted screenshots in [`technical-notes/images/week-01/`](technical-notes/images/week-01/)
- **Blockers:** None
- **Next week:** IAM: write a read-only S3 policy and test it in the IAM Policy Simulator; create an EC2 role and document the policy JSON

<!-- Copy the block above for each new week. -->
