# Learning Progress

Weekly log of study hours, hands-on work, and evidence. Updated every Sunday.

## Summary

| Metric                   | Count                                                |
| ------------------------ | ---------------------------------------------------- |
| Weeks logged             | 1                                                    |
| Total study hours        | 8                                                    |
| AWS labs documented      | 1 (account security)                                 |
| SAP BTP topics studied   | 2 (BTP Fundamentals Level 1 & 2)                     |
| Projects verified ✅     | 0 / 5                                                |
| Certifications           | 0                                                    |
| Badges                   | 2 (SAP Learning course-completion badges, June 2026) |
| LinkedIn posts published | 1                                                    |

## Weekly log

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
