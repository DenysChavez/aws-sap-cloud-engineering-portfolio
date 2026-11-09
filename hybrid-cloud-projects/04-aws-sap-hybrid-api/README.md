# 04 — AWS + SAP Hybrid API

> **Status:** Planned (design first; implementation where access permits)
> **Environment:** AWS sandbox + SAP BTP trial
> **Estimated cost:** $0 in sandbox; API Gateway and Lambda requests are low-cost but must be cleaned up in a personal account
> **Last updated:** 2026-11-04

## 1. Objective
Design, and where feasible build, an architecture where an AWS-hosted API (API Gateway + Lambda) is consumed by SAP Integration Suite and exposed through SAP API Management.

## 2. Problem Being Addressed
Many companies run SAP alongside workloads on AWS. Connecting them securely through authentication, managed APIs, and monitoring is a core hybrid-cloud skill.

## 3. Architecture
_Diagram to be added: client → SAP API Management → Cloud Integration iFlow → Amazon API Gateway → AWS Lambda → (optional) DynamoDB/S3._

## 4. Technologies Used
| Technology | Purpose in this project |
|---|---|
| Amazon API Gateway | Public HTTPS API on AWS |
| AWS Lambda (Python) | Business logic |
| SAP Integration Suite | Orchestration and transformation |
| SAP API Management | Governance in front of the integration |

## 5. Implementation Steps
_To be written._

## 6. Evidence
_To be added._

## 7. Challenges
_To be written._

## 8. What I Learned
_To be written._

## 9. Future Improvements
- Replace API keys with OAuth 2.0 client credentials.

## 10. Cleanup
- [ ] Delete API Gateway stage and API
- [ ] Delete Lambda function and log groups
- [ ] Undeploy iFlow and API proxy
