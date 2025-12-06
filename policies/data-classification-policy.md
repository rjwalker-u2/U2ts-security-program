DATA CLASSIFICATION, HANDLING, RETENTION & DISPOSAL POLICY

Company: U2 Technology Solutions (U2TS)
Policy Owner: Chief Information Security Officer (CISO)
Approval Date: [Insert date]
Version: 1.0

Framework Alignment:

SOC 2 (CC6, CC7, CC8)

ISO 27001 Annex A.8 (Asset Management)

NIST SP 800-53 (MP-2, MP-3, MP-4, PL-2, SC-28)

NIST Privacy Framework

CIS Controls 3 & 13

1. Purpose

The purpose of this policy is to establish a standardized system for classifying, handling, retaining, and securely disposing of data to protect U2TS information assets throughout the data lifecycle.

This ensures:

Regulatory compliance

Proper protection levels

Reduced data exposure

Standardized data governance

Secure data destruction

2. Scope

This policy applies to:

All U2TS systems, applications, and cloud platforms

All employees, contractors, vendors, and third parties

All data owned, stored, processed, or transmitted by U2TS

Includes:

Customer data

Employee data

Intellectual property

Source code

Logs & telemetry

Financial & operational records

3. Data Classification Levels

U2TS classifies data into four levels:

3.1 Level 1 — Public

Description:

Information intentionally made public

No risk if disclosed

Examples:

Marketing website content

Public blog posts

Job postings

Handling:

No special controls required

3.2 Level 2 — Internal

Description:

Non-sensitive info for internal use

Unauthorized disclosure could cause minor impact

Examples:

Internal procedural documents

Non-sensitive operational data

Internal presentations

Handling Requirements:

Store only in approved internal systems

Not for public distribution

No external sharing without approval

3.3 Level 3 — Confidential

Description:

Sensitive information requiring protection

Unauthorized access may cause operational, legal, or financial impact

Examples:

Customer contact data

Internal financial records

Source code

System configurations

Employee data

Handling Requirements:

Must be encrypted at rest & in transit

Not allowed on personal devices

Sharing requires NDA or approval

3.4 Level 4 — Highly Sensitive

Description:

Highest-risk information

Unauthorized disclosure may cause severe harm or regulatory penalties

Examples:

Credentials, API keys, and secrets

Security logs & detection telemetry

Financial transaction data

Customer PII or authentication data

Production database exports

Handling Requirements:

Strong encryption required

MFA required for all access

Store in secure locations only (Vaults, PAM, encrypted DBs)

No removable media

Access logged & monitored

Zero-trust access enforced

4. Data Handling Requirements (By Classification)
Public

May be freely shared

No encryption required

Internal

Stored in internal systems only

Encrypted in transit (HTTPS)

Confidential

Encryption in transit & at rest

No emailing outside the company without protection

Must be stored in approved systems (OneDrive, SharePoint, encrypted DBs)

Highly Sensitive

Must NEVER be stored in:

Email

Slack/Teams messages

Personal devices

Local text files

Access requires privileged authentication

All access logged and reviewed

Must not be transmitted unless encrypted end-to-end

5. Data Retention Requirements

U2TS retains data only as long as necessary for business or legal purposes.

Data Type	Retention Period	Notes
Customer Data	7 years	Unless contract defines otherwise
Security Logs	1 year minimum	Aligned with SOC 2 & incident analysis
HR/Employee Records	6 years	Legal requirement
Financial Records	7 years	IRS & regulatory requirements
Audit Evidence	3 years	SOC 2 audit retention
Source Code	Indefinite	Until product discontinued
Backups	30–90 days	Based on backup tier

No data may exceed retention limits without documented justification.

6. Data Disposal Requirements

Data must be disposed of securely and appropriately based on classification.

Approved Disposal Methods:

Cryptographic wiping

Secure deletion tools

Cloud provider secure delete

Physical destruction (for drives)

Highly Sensitive Data Disposal

Must be confirmed by Security

Dual-authorization required

Evidence of destruction logged

Prohibited Disposal Methods

Regular file delete

Formatting drives without secure wipe

Disposing of unencrypted media

7. Data Storage Requirements
Public

Any company-approved system

Internal

Internal SaaS tools (SharePoint, OneDrive)

Encrypted in transit

Confidential

Encrypted storage required

No local desktop storage

No external sharing without approval

Highly Sensitive

Must be stored ONLY within:

PAM Vault

Secret Managers (AWS Secrets Manager, Azure Key Vault)

Encrypted production databases

8. Logging & Monitoring

For Confidential and Highly Sensitive data:

Access logs must be collected

Logs reviewed monthly

Alerts configured for abnormal access patterns

9. Responsibilities
Data Owners

Assign classification

Approve access requests

Determine retention requirements

Data Custodians

Implement access controls

Ensure storage and encryption requirements are met

All Employees

Handle data per classification requirements

Report improper access

10. Enforcement

Violations may result in:

Access revocation

Disciplinary action

Termination

Legal penalties depending on data type

11. Review Cycle

This policy must be reviewed annually or after significant operational changes or data-related incidents.
