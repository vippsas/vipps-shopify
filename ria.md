<!-- START_METADATA
---
unlisted: true
---
END_METADATA -->

# Security and Privacy Risk Identification

|                                 |                                |
|---------------------------------|--------------------------------|
| **Service Owner(s)**            | Plugins team                   |
| **Risk Owner**                  | Vivi Thi Nguyen                |
| **Service Data Classification** | `PUBLIC`                       |
| **Last Reviewed**               | 03/02/26                       |


## Service description

This is a documentation-only repository containing user guides and installation instructions for the Vipps/MobilePay Shopify plugins. The repository is publicly accessible and contains markdown files, images (screenshots), and setup instructions for merchants. It does not contain any runtime code, API credentials, or customer data. The documentation is maintained as part of the Vipps MobilePay developer documentation ecosystem.

### Data Flow Diagram (DFD)

No data flows through this repository. It is a static documentation site/repository. Content is maintained via git commits and published to the Vipps MobilePay developer portal.


## Data dictionary

| Data | Classification | Comments |
|------|----------------|----------|
| Documentation and repository content | PUBLIC | README, installation guides, screenshots, and setup instructions; no secrets or personal data. |


## Risk scenarios / Impact Analysis

| Risk scenario | Risk Driver | Impact – What may happen if we don't implement the controls? | Security Controls |
|---------------|-------------|--------------------------------------------------------------|-------------------|
| Sensitive information accidentally committed to repo | Confidentiality | API keys, credentials, or internal info exposed publicly; potential security breach, reputational damage. | Pre-commit hooks to scan for secrets; review process for all changes; clear contribution guidelines. |
