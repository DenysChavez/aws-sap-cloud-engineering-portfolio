# 02 — SAP BTP Environment Administration

> **Status:** Planned
> **Environment:** SAP BTP trial account (free, time-limited — not yet created)
> **Estimated cost:** $0
> **Last updated:** 2026-11-04

## 1. Objective
Explore and document the administration tasks a Junior SAP BTP Administrator performs: navigating the account model, assigning entitlements, managing role collections, and working with the Cloud Foundry environment.

## 2. Problem Being Addressed
Organizations running SAP BTP need administrators who can structure accounts, control which services each team can use, and grant access safely. Misconfigured roles or entitlements are a common source of security and cost problems.

## 3. Architecture
_Diagram to be added: global account → directories → subaccounts → Cloud Foundry orgs/spaces, with role collections and entitlements mapped._

## 4. Technologies Used
| Technology | Purpose in this project |
|---|---|
| SAP BTP cockpit | Account and access administration |
| SAP BTP CLI (`btp`) | Scripted administration |
| Cloud Foundry CLI (`cf`) | Orgs, spaces, app deployment |
| Cloud Foundry environment | Runtime for a small test app |

## 5. Implementation Steps
_To be written while building. Trial limitations will be noted wherever a feature is unavailable._

## 6. Evidence
_Screenshots to be added (redact subaccount IDs and email addresses)._

## 7. Challenges
_To be written._

## 8. What I Learned
_To be written._

## 9. Future Improvements
- Manage the subaccount setup with the Terraform provider for SAP BTP.

## 10. Cleanup
- [ ] Delete test apps and service instances
- [ ] Note trial expiry date
