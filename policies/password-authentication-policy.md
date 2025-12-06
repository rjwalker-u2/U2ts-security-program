PASSWORD & AUTHENTICATION POLICY

Company: U2 Technology Solutions (U2TS)
Policy Owner: Chief Information Security Officer (CISO)
Approval Date: [Insert date]
Version: 1.0

Framework Alignment:

NIST SP 800-63B (Digital Identity Guidelines)

SOC 2 (CC6.x)

ISO 27001 Annex A.9

NIST 800-53 (IA controls)

CIS Controls 6 & 16

1. Purpose

The purpose of this policy is to define secure authentication requirements for all U2TS systems, including password creation, MFA usage, account management, and authentication of privileged and service accounts.

This policy replaces outdated "complexity" rules with modern, evidence-based authentication controls.

2. Scope

This policy applies to:

All U2TS employees, contractors, and vendors

All internal and external systems

Cloud services (Azure, AWS, GCP, Google Workspace, etc.)

Production & non-production environments

Service accounts and API keys

3. Authentication Principles (NIST 800-63B)
3.1 Length Over Complexity

Passwords MUST prioritize length over forced complexity.

3.2 No Periodic Password Expiration

U2TS does not require passwords to expire unless there is evidence of compromise.

3.3 Mandatory MFA

Multi-factor authentication is required for all systems storing or processing data above "Internal" classification.

3.4 Breach Password Screening

All passwords must be checked against known breached password lists (e.g., HaveIBeenPwned).

3.5 Usability Awareness

Authentication requirements must consider user experience while maintaining security.

4. Password Requirements (Per NIST 800-63B)
4.1 User Password Requirements

All user passwords must:

Be at least 14 characters

Allow all characters (spaces, symbols, passphrases)

Not require complexity rules (no forced uppercase/symbols)

Not be similar to previous passwords

Not contain the user’s name or email

Not be reused from breach databases

Recommended:

Passphrases such as “CoffeeCloudGuitarRain!”

5. Multi-Factor Authentication (MFA)
5.1 MFA is Required For:

Email accounts

VPN access

Production systems

Admin or privileged accounts

Any system containing Confidential or Highly Sensitive data

Access to GitHub, CI/CD, cloud consoles

5.2 Approved MFA Methods

Authenticator apps (Microsoft Authenticator, Duo, Google Authenticator)

FIDO2 hardware keys (YubiKey)

SMS MFA is allowed only as backup, not primary

6. Password Storage Requirements

All passwords must be stored using:

Salted hashing

Strong hashing algorithms (Argon2id preferred, or bcrypt/scrypt)

Never plaintext

This applies to internal applications AND vendor systems.

7. Privileged Account Authentication Requirements
Privileged users MUST:

Use separate admin accounts

Use MFA at all times

Use long, unique passphrases

Avoid shared accounts

Privileged accounts must NOT:

Be used for day-to-day activities

Log into email or SaaS platforms

This aligns with NIST IA family and SOC 2 security criteria.

8. Service Accounts & API Keys
8.1 Requirements

Must NOT use passwords

Must use long, random secrets or certificates

Must be rotated at least every 90 days

Must be stored in a secrets manager

Must not be hardcoded in scripts or code

Must have least-privilege access

8.2 Prohibited:

Putting API keys in GitHub

Storing secrets in config files

Using personal accounts as service accounts

9. Failed Login & Lockout Policy

To limit brute force attacks:

10 failed attempts → temporary lockout

Lockout duration: 10 minutes

Logging required for all failed login attempts

Alerts required for privileged accounts

10. Password Reset Requirements

Self-service password resets are allowed only with MFA verification.

Helpdesk resets require:

Identity verification

Temporary password expiration upon first login

11. Shared Passwords
Shared passwords are strictly prohibited except for break-glass accounts

and must follow:

Password stored in a PAM vault

Access logged

Rotation after every use

12. Enforcement

Violations may result in:

Removal of access

Disciplinary action

Termination

Legal consequences for misuse of privileged access

13. Review Cycle

Policy must be reviewed annually or after authentication-related incidents.
