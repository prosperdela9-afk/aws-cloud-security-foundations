# Cloud Security Risk Assessment

## 1. Lab Overview

**Project:** AWS Cloud Security Foundations  
**Module:** Cloud Security Fundamentals  
**Lesson:** Practical Cloud Security Risk Assessment  
**Environment:** Simulated AWS healthcare application  
**Assessment type:** Security risk identification and analysis

### Objective

Identify security weaknesses in a simulated cloud environment, evaluate their potential impact, prioritise risks and recommend appropriate security controls.

This exercise uses hypothetical findings. No live AWS resources were inspected or modified.

## 2. Simulated Environment

The organisation operates a healthcare application using:

| Component | Purpose |
|---|---|
| Amazon S3 | Patient record storage |
| Amazon EC2 | Application hosting |
| AWS IAM | Identity and access management |
| Amazon CloudWatch | Monitoring and logging |
| Backup and recovery | Data and service recovery |

## 3. Risk Scoring Method

Risk is calculated using:

**Risk Score = Likelihood × Impact**

Likelihood and impact are each scored from 1 to 5.

| Score | Risk Level |
|---|---|
| 1–4 | Low |
| 5–9 | Medium |
| 10–16 | High |
| 17–25 | Critical |

These scores are illustrative estimates for this training exercise.

## 4. Identified Security Risks

### R01 — Public S3 Bucket

**Finding:** An S3 bucket containing patient records is publicly accessible.

- Asset: Patient records.
- Vulnerability: Incorrect public access configuration.
- Threat: Unauthorised access or data exposure.
- CIA principle: Confidentiality.
- Likelihood: 4/5.
- Impact: 5/5.
- Risk score: 20/25.
- Risk level: Critical.

**Recommended controls:**
- Enable S3 Block Public Access where appropriate.
- Review bucket policies and access control settings.
- Apply least-privilege IAM permissions.
- Enable appropriate data encryption.
- Monitor access activity.

### R02 — Shared Administrator Account

**Finding:** Multiple employees use the same administrator account.

- Asset: Administrative identities.
- Vulnerability: Shared credentials and excessive privileges.
- Threat: Unauthorised access and inability to attribute actions.
- CIA principles: Confidentiality, Integrity and Availability.
- Likelihood: 4/5.
- Impact: 5/5.
- Risk score: 20/25.
- Risk level: Critical.

**Recommended controls:**
- Provide individual identities.
- Apply least-privilege permissions.
- Require MFA.
- Use IAM roles where appropriate.
- Monitor administrative activity.

### R03 — Unrestricted SSH Access

**Finding:** An EC2 security group allows SSH access from 0.0.0.0/0.

- Asset: EC2 application server.
- Vulnerability: Unrestricted inbound SSH access.
- Threat: Unauthorised connection attempts and potential compromise.
- CIA principles: Confidentiality, Integrity and Availability.
- Likelihood: 4/5.
- Impact: 4/5.
- Risk score: 16/25.
- Risk level: High.

**Recommended controls:**
- Restrict SSH access to approved IP addresses.
- Consider Systems Manager Session Manager.
- Review security group rules regularly.
- Monitor authentication activity.

### R04 — No Tested Backup and Recovery Process

**Finding:** The organisation has no tested backup and recovery process.

- Asset: Patient records and application services.
- Vulnerability: Lack of validated recovery procedures.
- Threat: Prolonged outage or permanent data loss.
- CIA principle: Availability, with potential impact on integrity.
- Likelihood: 3/5.
- Impact: 5/5.
- Risk score: 15/25.
- Risk level: High.

**Recommended controls:**
- Establish regular backups.
- Define recovery objectives.
- Test restoration procedures.
- Protect backup access.
- Document disaster recovery procedures.

### R05 — Insufficient Activity Monitoring

**Finding:** Important application and account activity is not monitored.

- Asset: Cloud accounts and application infrastructure.
- Vulnerability: Insufficient logging and alerting.
- Threat: Delayed detection of malicious activity.
- CIA principles: Confidentiality, Integrity and Availability.
- Likelihood: 4/5.
- Impact: 4/5.
- Risk score: 16/25.
- Risk level: High.

**Recommended controls:**
- Enable AWS CloudTrail.
- Configure CloudWatch monitoring and alarms.
- Review security events.
- Establish alerting procedures.
- Investigate suspicious activity.

## 5. Risk Summary

| Risk ID | Finding | Score | Priority |
|---|---|---:|---|
| R01 | Public S3 bucket | 20 | Critical |
| R02 | Shared administrator account | 20 | Critical |
| R03 | Unrestricted SSH | 16 | High |
| R04 | Untested backups | 15 | High |
| R05 | Insufficient monitoring | 16 | High |

## 6. Recommended Remediation Priority

1. Restrict public access to sensitive S3 data.
2. Replace shared administrator credentials with individual identities and appropriate access controls.
3. Restrict SSH access to approved sources.
4. Establish and test backup and recovery procedures.
5. Implement centralised logging, monitoring and alerting.

The organisation should prioritise critical risks while planning remediation for all high-risk findings.

## 7. Lessons Learned

This assessment demonstrates that cloud security requires more than deploying infrastructure.

Security engineers must:

- Identify and protect critical assets.
- Understand threats and vulnerabilities.
- Evaluate likelihood and business impact.
- Prioritise remediation.
- Apply preventive, detective and corrective controls.
- Verify that security improvements are effective.

## 8. Limitations

This is a simulated risk assessment based on hypothetical findings. It is not a penetration test, compliance audit or assessment of a live AWS environment.

The risk scores are illustrative and should be recalculated using actual business and technical evidence in a real engagement.

## 9. References

- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
- [AWS Security Best Practices](https://docs.aws.amazon.com/security/)
- [AWS Well-Architected Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)

---

**Project:** AWS Cloud Security Foundations  
**Module:** Cloud Security Fundamentals  
**Lesson:** Practical Cloud Security Risk Assessment  
**Status:** Completed — Simulated Assessment