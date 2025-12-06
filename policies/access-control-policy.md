ACCESS CONTROL POLICY (ACP)

Company: U2 Technology Solutions (U2TS)
Policy Owner: Chief Information Security Officer (CISO)
Approval Date: [Insert date]
Version: 1.0

Framework Alignment:

SOC 2 Trust Services Criteria (CC6.x)

ISO/IEC 27001 Annex A.9 (Access Control)

NIST SP 800-53 Rev 5 (AC-1 to AC-17)

CIS Controls v8 (Control 6)

1. Purpose

The purpose of this Access Control Policy is to ensure that only authorized users, processes, and devices can access U2TS information assets in a manner consistent with business needs, regulatory requirements, and security best practices.

2. Scope

This policy applies to:

All U2TS employees, contractors, consultants, and vendors

All production and internal systems

Cloud services (Azure, AWS, Google Workspace)

Endpoints, servers, databases, and network infrastructure

Authentication systems (SSO, IAM, MFA providers)

3. Principles of Access Control
3.1 Least Privilege

All users must be granted the minimum access required to perform job duties.

3.2 Role-Based Access Control (RBAC)

Access assignments must be determined based on job roles, not individuals.

3.3 Need-to-Know

Users must not access data beyond what is essential for their responsibilities.

3.4 Separation of Duties

No single individual may complete high-risk processes without checks/balances
(e.g., developers cannot deploy directly to production without approval).

4. Identity & Access Management (IAM)
4.1 User Account Creation

Only HR-verified employees may be granted accounts.

Requests must go through the IT Service Desk or IAM system.

All new accounts must require MFA at first login.

4.2 Joiner-Mover-Leaver Process

Joiners: Access is provisioned based on job role.

Movers: Access must be adjusted within 24 hours of role change.

Leavers: All access must be revoked within 30 minutes of termination.

4.3 Privileged Accounts

Must be approved by the CISO or delegated authority.

Must use MFA.

Must rotate passwords at least every 90 days (or use PAM system).

Must not be used for everyday tasks.

5. Authentication Requirements
5.1 Password Requirements

Passwords must follow NIST SP 800-63B guidance:

Minimum length: 14 characters

No complexity requirements (length over complexity)

Must be checked against known breach lists

No reuse of last 10 passwords

5.2 Multi-Factor Authentication (MFA)

Required for:

Email

VPN

Cloud systems

Production systems

Administrative accounts

Access to sensitive data

5.3 Single Sign-On (SSO)

U2TS must centralize authentication using SSO where possible.

6. Access Provisioning & Deprovisioning
6.1 Provisioning

All access must be:

Approved by the user’s manager

Logged in the ticketing/IAM system

Assigned through role-based access groups

6.2 Deprovisioning

Access removal must occur:

Immediately for terminated employees

Within 24 hours for role changes

When access is no longer needed

6.3 Temporary Access

Must have an expiration date

Must be reviewed weekly

Must require approval

7. Privileged Access Management (PAM)
7.1 Requirements

Admin accounts must be separate from user accounts

Use of break-glass accounts must be logged and reviewed

Privileged sessions must be monitored

Production access must require ticket approval

8. System & Application Access Controls
8.1 Database Access

Only service accounts or authorized personnel may access production databases

All access must be logged

8.2 API Keys & Secrets

Must be stored in a secrets manager

Must not be stored in code or repositories

Must rotate every 90 days or after exposure

8.3 Third-Party Application Access

Vendors must follow least privilege and MFA requirements.

9. Logging & Monitoring
9.1 Authentication Logs

Must capture:

Successful and failed login attempts

Password resets

MFA usage

Privileged account activity

9.2 Review Frequency

Privileged account logs: daily

Standard account logs: weekly

10. Access Reviews
10.1 Quarterly Reviews

Managers must review employee access every 90 days to ensure appropriateness.

10.2 High-Sensitivity Systems

Reviewed monthly if the system processes:

Customer data

Financial records

Production configurations

11. Policy Enforcement

Violation of this policy may result in:

Removal of access

Disciplinary action up to termination

Legal action

12. Review Cycle

This policy must be reviewed annually or when major changes occur in technology, risk, or regulatory requirements.
