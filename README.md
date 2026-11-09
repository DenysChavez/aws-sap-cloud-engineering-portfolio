# AWS & SAP Cloud Engineering Portfolio

Hands-on projects, architecture diagrams, and technical notes from my journey as a Cloud Computing student working toward a career as a **Junior SAP BTP Administrator / Junior SAP Cloud Engineer**.

**Denys Chavez Fuentes** · AAS Cloud Computing, Delaware County Community College (expected Spring 2027)
[LinkedIn](https://www.linkedin.com/in/denyschavez-fuentes/) · [GitHub](https://github.com/DenysChavez)

---

## Why this repository exists

I learn by building. Every project here documents what I set out to do, how I built it, what broke, and what I learned. Nothing is marked as complete until it works and the evidence is in the folder.

## Projects

| # | Project | Area | Status |
|---|---|---|---|
| 00 | [AWS coursework labs: redo map](aws-projects/00-coursework-labs/) | AWS | Being redone with evidence |
| 01 | [AWS Cloud Infrastructure](aws-projects/01-aws-cloud-infrastructure/) | IAM · VPC · EC2 · S3 · CloudWatch | Planned |
| 02 | [SAP BTP Environment Administration](sap-btp-projects/02-btp-environment-administration/) | Accounts · Entitlements · Roles · Cloud Foundry | Planned |
| 03 | [SAP Integration Suite API Flow](sap-integration-projects/03-integration-suite-api-flow/) | Cloud Integration · API Management | Planned |
| 04 | [AWS + SAP Hybrid API](hybrid-cloud-projects/04-aws-sap-hybrid-api/) | API Gateway · Lambda · SAP Integration Suite | Planned |
| 05 | [Terraform AWS Environment](aws-projects/05-terraform-aws-environment/) | Infrastructure as Code · Security | Planned |

**Status key:** Planned → In progress → Built, awaiting verification → Verified ✅

## Repository structure

```
aws-projects/              AWS labs and infrastructure projects (incl. Terraform)
sap-btp-projects/          SAP BTP administration and Cloud Foundry
sap-integration-projects/  SAP Integration Suite and API Management
hybrid-cloud-projects/     Projects connecting AWS and SAP technologies
technical-notes/           Short explainers on concepts I've studied
architecture-diagrams/     Diagram sources (.drawio) and exports (.svg)
blog-posts/                Drafts of longer learning write-ups
templates/                 README template every project follows
```

## Skills in focus

**AWS:** IAM · VPC & networking · EC2 · S3 · Lambda · KMS · CloudWatch
**SAP:** SAP BTP account model · entitlements & quotas · role collections · Cloud Foundry · Integration Suite · API Management
**Supporting:** Linux · Bash · Python · Git · REST APIs & JSON · Terraform · Docker · CI/CD

## Learning progress

See [PROGRESS.md](PROGRESS.md) for the weekly log.

## Security practices

- No credentials, keys, or tokens are committed — see [.gitignore](.gitignore).
- Screenshots are redacted (account IDs, emails, tenant/subaccount IDs).
- Every AWS project includes a cleanup checklist to avoid unexpected charges.
