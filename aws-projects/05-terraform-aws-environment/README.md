# 05 — Terraform AWS Environment

> **Status:** Planned
> **Environment:** [AWS sandbox or personal account]
> **Estimated cost:** $0 when created and destroyed in the same session; `terraform destroy` is part of every run
> **Last updated:** 2026-11-04

## 1. Objective
Rebuild the Project 01 environment with Terraform, document the configuration, and explain its security decisions.

## 2. Problem Being Addressed
Infrastructure built by hand in the console is hard to review, repeat, or audit. Infrastructure as code makes environments reproducible and lets changes go through code review.

## 3. Architecture
_Same as Project 01, defined in code. Diagram to be added._

## 4. Technologies Used
| Technology | Purpose in this project |
|---|---|
| Terraform | Infrastructure as code |
| AWS provider | VPC, EC2, S3, IAM resources |
| tfsec / Checkov | Static security scanning |
| GitHub Actions | `terraform fmt` and `validate` on every push (no `apply` in CI) |

## 5. Implementation Steps
_To be written._

## 6. Evidence
_`terraform plan` output (redacted) and scan results to be added._

## 7. Challenges
_To be written._

## 8. What I Learned
_To be written._

## 9. Future Improvements
- Remote state with locking.
- Move the website hosting to S3 + CloudFront through Terraform.

## 10. Cleanup
- [ ] `terraform destroy` completed and verified in the console
