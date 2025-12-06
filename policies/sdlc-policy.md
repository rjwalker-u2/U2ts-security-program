SECURE SOFTWARE DEVELOPMENT LIFECYCLE (SDLC) POLICY

Company: U2 Technology Solutions (U2TS)
Policy Owner: Director of Engineering & CISO
Approval Date: [Insert date]
Version: 1.0

Framework Alignment:

SOC 2 (CC7, CC8 — Change Management, Code Release Controls)

NIST SP 800-64 (Security Considerations in SDLC)

NIST 800-53 (SA, CM, SI families)

ISO 27001 Annex A.12 & A.14

OWASP SAMM & OWASP ASVS

CIS Controls 16, 18

1. Purpose

The purpose of this Secure Software Development Lifecycle (SDLC) Policy is to ensure software built and deployed by U2TS is secure, reliable, auditable, and compliant.
This policy establishes:

Security integration at every SDLC phase

Code review and CI/CD requirements

Automated security scanning

Change management controls

DevSecOps practices

Secure deployment standards

2. Scope

Applies to all:

Application development teams

DevOps and platform engineers

Code repositories (GitHub, GitLab, Bitbucket)

CI/CD pipelines

Infrastructure-as-code (IaC)

SaaS and internal applications

Production and non-production environments

Includes:

Feature development

Hotfixes

Infrastructure configurations

APIs and microservices

3. SDLC Phases & Requirements
3.1 Phase 1 — Requirements & Planning

All new features or system changes must include:

Security requirements

Compliance considerations (SOC 2, privacy, PII)

Threat modeling for high-risk features

Data classification review

Architecture diagrams

Deliverables:

Requirements document

Risk assessment summary

3.2 Phase 2 — Design

Design must incorporate:

Secure architecture principles

Zero-trust access

Encryption requirements

Network segmentation principles

Input/output validation

API authentication requirements

Security outputs:

Updated threat model

Data flow diagrams

Security acceptance criteria

3.3 Phase 3 — Development

All developers must follow secure coding practices.

Development Requirements

No secrets or credentials in code

Use environment variables or secret managers

Follow OWASP ASVS

Write unit tests for critical functions

Limit direct production access

Dependency Management

Use approved package repositories

Mandatory vulnerability scanning (SCA)

Update dependencies regularly

Prohibited

Pushing directly to main

Debug code in production

Hardcoded API keys or tokens

3.4 Phase 4 — Testing

Security testing must be included in CI/CD:

Automated Testing

Static Application Security Testing (SAST)

Dependency/Software Composition Analysis (SCA)

Linting & code quality checks

Secret scanning

Manual Testing

Required for high-risk applications:

Penetration testing

Threat model validation

Code reviews

Approval Required

No code may advance without passing:

All automated CI checks

Peer code review

Security review for high-risk changes

3.5 Phase 5 — Deployment

All deployments must:

Follow Change Management Policy

Use CI/CD, not manual deployment

Require approvals via GitHub PR or ticket

Perform pre- and post-deployment checks

Tag releases for traceability

Production deployments require:

CAB approval (for high risk)

Rollback plan

Logging and monitoring verification

3.6 Phase 6 — Maintenance

Ongoing requirements:

Patch dependencies

Conduct regular vulnerability scans

Fix critical vulns within 7 days

Fix high vulns within 30 days

Reevaluate architecture annually

4. Code Review Requirements
All code changes must be reviewed based on:

Functionality

Security concerns

Impact to existing systems

Compliance requirements

Reviewers must verify:

No exposed secrets

Safe input handling

Proper error handling

Least privilege access

Secure API usage

Minimum requirement: 1 peer reviewer
High-risk changes: 2 reviewers + security approval

5. CI/CD Requirements
Required pipeline steps:

Build validation

Unit testing

SAST scanning

Secret scanning

Dependency scanning

Container scanning (if applicable)

Deployment pipeline must:

Be version-controlled

Have audit trails

Use least-privilege access tokens

Log all pipeline activities

6. Secrets Management
All secrets MUST be stored in:

AWS Secrets Manager

Azure Key Vault

GCP Secret Manager

HashiCorp Vault

Prohibited:

.env files committed to Git

Hardcoded credentials

Storing secrets in configuration files

Rotation Requirements:

Every 90 days

Immediately after exposure

7. Infrastructure-as-Code (IaC) Requirements
IaC must:

Be stored in version control

Undergo code review

Be scanned for misconfigurations

Be deployed via CI/CD

Tools: Terraform, CloudFormation, Pulumi

8. Third-Party & Open-Source Risk Controls

Before using external libraries or APIs:

Review licensing

Validate security posture

Check for known vulnerabilities

High-risk vendors require a formal Vendor Risk Assessment.

9. Logging & Monitoring

All applications must log:

Authentication events

Authorization failures

Privileged actions

Errors and exceptions

Logs must be:

Centralized

Immutable

Retained for 1 year

10. Enforcement

Violations of this policy may result in:

Blocked deployments

Revocation of access

Disciplinary action

Security incident response engagement

11. Review Cycle

This policy must be reviewed annually or after major system or regulatory changes.
