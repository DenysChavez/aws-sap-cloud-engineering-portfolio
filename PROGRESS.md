# Learning Progress

Weekly log of study hours, hands-on work, and evidence. Updated every Sunday.

## Summary

| Metric                   | Count                                                |
| ------------------------ | ---------------------------------------------------- |
| Weeks logged             | 2                                                    |
| Total study hours        | 18                                                   |
| AWS labs documented      | 2 (account security, IAM least privilege)           |
| SAP BTP topics studied   | 2 (BTP Fundamentals Level 1 & 2)                     |
| Projects verified ✅     | 0 / 5                                                |
| Certifications           | 0                                                    |
| Badges                   | 2 (SAP Learning course-completion badges, June 2026) |
| LinkedIn posts published | 3                                                    |

## Weekly log

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
