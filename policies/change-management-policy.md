CHANGE MANAGEMENT POLICY (CMP)

Company: U2 Technology Solutions (U2TS)
Policy Owner: Chief Information Security Officer (CISO)
Approval Date: [Insert date]
Version: 1.0

Framework Alignment:

SOC 2 Trust Services Criteria CC7, CC8

NIST SP 800-53 Rev 5 (CM-1 through CM-14)

ISO/IEC 27001 Annex A.12

ITIL v4 Change Enablement Practices

1. Purpose

The purpose of this Change Management Policy is to control changes to U2TS information systems, applications, networks, and cloud environments to reduce risk, maintain security, ensure stability, and support continuous compliance.

This policy ensures all changes are:

Authorized

Documented

Tested

Reviewed

Approved

Logged

Auditable

2. Scope

This policy applies to:

All production and internal systems

Cloud services (Azure, AWS, GCP)

SaaS applications used for business operations

Infrastructure components (servers, network devices, firewalls)

Endpoints and administrative tools

Application code deployments

Includes employees, contractors, and third-party service providers.

3. Types of Changes
3.1 Standard Changes

Pre-approved, low-risk, repeatable tasks

Examples: routine patching, certificate renewal, user provisioning

Must follow an approved SOP

Approval: Automated or manager-level

3.2 Normal Changes

Moderate or unknown risk

Require full risk assessment

Require CAB (Change Advisory Board) approval

Examples: network changes, production config updates, new system deployment

3.3 Emergency Changes

Implemented to address critical outages or security threats

Require expedited approval (CISO or CTO)

Post-implementation review required within 48 hours

4. Change Request Requirements

All changes must be documented in the Change Management System (CMS) and include:

Description and business justification

Change owner

Risk and impact analysis

Rollback plan

Testing evidence

Implementation plan

Communication plan

Requested date/time

Approvals

Change requests must be submitted at least 3 business days before implementation (except emergencies).

5. Risk Assessment for Changes

Each change must undergo risk evaluation based on:

Impact on confidentiality, integrity, availability (CIA)

User disruption

System criticality

Dependencies

Compliance implications

Risk Levels:

Low: No customer impact; internal-only

Medium: Minor service interruptions, internal systems

High: Production, customer-facing, or sensitive data impact

High-risk changes must have:

Mandatory peer review

CAB approval

Extended testing

A formal rollback plan

6. Change Advisory Board (CAB)

The CAB is responsible for reviewing and approving Moderate and High risk changes.

CAB Members:

CISO

IT Director

Lead Developer

Network Engineer

Security Analyst

Business Owner (when applicable)

CAB Responsibilities:

Evaluate risks

Approve or reject changes

Ensure alignment with business needs

Verify testing evidence

Ensure rollback procedures are sound

CAB meets weekly or as needed for major changes.

7. Testing Requirements

Before approval, all changes must be tested in a non-production environment.

Testing must include:

Functional verification

Security impact assessment

Regression testing

Dependency verification

Validation that rollback plan works

No change may proceed without documented testing unless it is an emergency change.

8. Deployment Requirements

Deployments must:

Follow approved timelines

Use version control and CI/CD where applicable

Include monitoring checkpoints

Notify impacted teams

Document completion in the CMS

For production changes, engineers must remain on standby for at least 30 minutes post-release.

9. Rollback & Recovery Procedures

Every change must include:

A clearly documented rollback plan

Validation steps to confirm rollback success

Ability to restore service continuity

Backup confirmation before implementation

Rollback must be executed if:

Deployment fails

Monitoring identifies service degradation

Unexpected behavior occurs

10. Logging & Documentation

All changes must be logged and retained for at least 1 year for audit purposes.

Logs must include:

Requestor

Approver(s)

Timestamp

Implementation details

Testing results

Validation results

Rollback (if applicable)

11. Emergency Change Procedures

Emergency changes must:

Be approved by CISO, CTO, or designated delegate

Prioritize restoring service and protecting data

Undergo a post-incident review (PIR) within 48 hours

Include documentation retroactively

Emergencies may not bypass logging requirements.

12. Compliance & Enforcement

Violations of this policy may result in:

Revocation of access

Disciplinary action

Contract termination

Legal consequences in severe cases

13. Review Cycle

This policy must be reviewed annually or following major incidents, audits, or  environmental changes.
