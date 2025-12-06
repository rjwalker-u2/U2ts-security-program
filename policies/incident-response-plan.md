Company: U2 Technology Solutions (U2TS)
Policy Owner: Chief Information Security Officer (CISO)
Approval Date: [Insert date]
Version: 1.0

1. Purpose

The purpose of this Incident Response Plan (IRP) is to ensure U2TS can detect, contain, eradicate, and recover from cybersecurity incidents in a structured, efficient, and compliant manner.
This plan aligns with:

NIST SP 800-61r2 (Computer Security Incident Handling Guide)

SOC 2 Trust Services Criteria (Security, Availability, Confidentiality)

ISO 27035

2. Scope

This policy applies to:

All information systems, applications, networks, and cloud services

All U2TS employees, contractors, and service providers

All security events that may impact confidentiality, integrity, or availability

3. Incident Response Objectives

Rapidly detect and confirm incidents

Contain threats to limit damage

Eradicate malicious artifacts

Recover operations safely

Preserve forensic evidence

Ensure clear communication internally and externally

Improve security posture through lessons learned

4. Definitions
Security Event

Any observable occurrence within a system or network.

Security Incident

A confirmed event that jeopardizes confidentiality, integrity, or availability.

Data Breach

Unauthorized access, disclosure, or acquisition of protected or sensitive data.

5. Roles & Responsibilities
5.1 Incident Response Team (IRT)
Role	Responsibilities
CISO (Lead)	Declare incidents, coordinate response, approve communications
Security Analyst	Investigate alerts, run triage, gather evidence
IT Operations	Perform containment actions (isolations, resets, patches)
Legal	Interpret legal obligations, breach notification requirements
Communications	Prepare internal & external messaging
HR	Handle insider threat implications
Third-Party IR Firm	Called when escalation exceeds internal capabilities
6. Incident Severity Classification

U2TS categorizes incidents using the following matrix:

Severity 1 – Critical

Ransomware

Active compromise of production systems

Confirmed data breach

Outage affecting customers

Regulatory reporting required

Severity 2 – High

Malware infection

Lateral movement detected

Privilege escalation

Unauthorized access

Severity 3 – Medium

Suspicious activity requiring investigation

Policy violations

Failed login brute force attempts

Severity 4 – Low

Minor issues with no impact

Routine alerts requiring monitoring

Severity determines escalation, reporting, and documentation requirements.

7. Incident Response Lifecycle (NIST Framework)
7.1 Preparation

Train IR team annually

Maintain asset inventory

Ensure logging & monitoring is enabled (SIEM, EDR, Sysmon)

Establish secure communication channels (Teams/Slack IR channel)

Validate backups

7.2 Identification

The Security Analyst performs:

Alert validation

Log analysis (EDR, SIEM, Sysmon, CloudTrail)

Endpoint triage

Correlation of events

Determination: incident or false positive

Documentation Required:

Analyst notes

Timeline of events

Initial incident category7.3 Containment
Short-Term Containment

Isolate affected endpoints

Disable compromised accounts

Block malicious IPs/domains

Stop data exfiltration

Long-Term Containment

Apply patches

Change credentials

Implement network segmentation

Modify firewall rules

7.4 Eradication

Remove malware

Clean registry/services

Reset passwords

Remove unauthorized applications

Patch vulnerabilities

Evidence must be preserved before eradication begins.

7.5 Recovery

Restore systems from clean backups

Validate applications and services

Monitor endpoints for recurrence

Gradually reintroduce systems to production

7.6 Lessons Learned

Conduct a lessons-learned meeting within 10 business days.

Document:

What happened

Root cause

Successes

Failures

Required remediations

Updates to policies, controls, or training

Store all documentation in governance/IR-lessons-learned.

8. Incident Communication Plan
Internal Communications

Use pre-established IR channels

Share only factual, confirmed information

Maintain least-privilege awareness

External Communications

Prepared and approved by:

CISO

Legal

Communications

Never communicate externally without formal approval.

9. Evidence Handling (Chain of Custody)

Document who collected evidence, when, and how

Store evidence in a read-only, secure location

Avoid altering timestamps or metadata

Use imaging tools for disk/endpoint captures

This section aligns with digital forensics best practices.

10. Incident Reporting Requirements
Regulatory

If customer data or PII is affected:

Notify legal counsel immediately

Determine breach notification laws (e.g., state privacy laws, GDPR if applicable)

Report to customers within mandated timelines

Internal

A full incident report must be created within 5 business days.

11. Testing & Review

Perform IR tabletop exercises twice per year

Review this IRP annually

Update based on lessons learned and new threats

12. Approval

Approved by:
Chief Information Security Officer (CISO)
Date: ___________________
