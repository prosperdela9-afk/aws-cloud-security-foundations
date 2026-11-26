# Cloud Security Threats and Vulnerabilities

## 1. Introduction

Cloud security threats and vulnerabilities are important considerations when designing, deploying and maintaining secure cloud environments.

A Cloud Security Engineer must understand how attackers exploit weaknesses, assess the potential impact and implement appropriate security controls.

This lesson introduces common cloud security threats, vulnerabilities, risks and relevant AWS security services.

## 2. Understanding Threats, Vulnerabilities and Risks

These three concepts are related but have different meanings.

### Threat

A threat is anything capable of causing harm to an information system, application or organisation.

Examples:
- Malicious attackers.
- Phishing campaigns.
- Malware.
- Ransomware.
- Distributed Denial-of-Service attacks.

### Vulnerability

A vulnerability is a weakness in a system, application or configuration that could be exploited.

Examples:
- Weak passwords.
- Unpatched operating systems.
- Publicly accessible storage buckets.
- Excessive IAM permissions.
- Unrestricted network access.
- Exposed credentials.

### Risk

Risk is the potential for harm when a threat exploits a vulnerability.

For example:

An attacker attempts to access an EC2 instance through an unrestricted SSH port.

- Threat: Malicious attacker.
- Vulnerability: SSH access exposed to the internet.
- Risk: Unauthorised access, server compromise and potential data exposure.

## 3. Common Cloud Security Threats

### 3.1 Phishing Attacks

Phishing occurs when attackers use deceptive communications to trick individuals into revealing sensitive information or performing unsafe actions.

Potential impact:
- Stolen credentials.
- Unauthorised account access.
- Data exposure.
- Compromised cloud resources.

Recommended controls:
- Multi-factor authentication.
- Phishing-resistant authentication where available.
- Employee security awareness.
- Email security controls.
- Monitoring suspicious sign-in activity.

### 3.2 Malware and Ransomware

Malware is malicious software designed to compromise systems, steal information or disrupt operations.

Ransomware is a type of malware that can encrypt files and demand payment for their recovery.

Potential impact:
- Data loss.
- Business disruption.
- Unauthorised access.
- Financial and reputational damage.

Recommended controls:
- Regular security patching.
- Endpoint protection.
- Least-privilege permissions.
- Secure backups.
- Network segmentation.
- Security monitoring.

### 3.3 Distributed Denial-of-Service (DDoS)

A DDoS attack attempts to make an application or service unavailable by overwhelming it with malicious traffic.

Potential impact:
- Service outages.
- Disrupted business operations.
- Increased infrastructure costs.
- Poor customer experience.

Recommended controls:
- AWS Shield.
- AWS WAF where appropriate.
- Traffic filtering.
- Rate limiting.
- Resilient application architecture.
- Monitoring and alerting.

### 3.4 Cloud Misconfiguration

Cloud misconfiguration occurs when cloud resources are configured insecurely.

Examples:
- Publicly accessible S3 buckets.
- Overly permissive IAM policies.
- Unrestricted security group rules.
- Inadequate encryption settings.
- Missing logging.

Potential impact:
- Data exposure.
- Unauthorised access.
- Resource compromise.
- Compliance issues.

Recommended controls:
- Secure configuration baselines.
- Least privilege.
- Regular configuration reviews.
- AWS security services.
- Infrastructure as Code validation.

### 3.5 Credential Compromise

Credential compromise occurs when passwords, access keys, tokens or other authentication information are stolen or exposed.

Potential impact:
- Account takeover.
- Unauthorised resource access.
- Data theft.
- Malicious infrastructure changes.

Recommended controls:
- MFA.
- Short-lived credentials.
- IAM roles.
- Secure credential storage.
- Regular credential reviews.
- Monitoring unusual account activity.

## 4. Common Cloud Security Vulnerabilities

| Vulnerability | Potential Impact |
|---|---|
| Public storage bucket | Unauthorised data exposure |
| Unrestricted SSH access | Increased attack surface |
| Weak passwords | Account compromise |
| Excessive IAM permissions | Unauthorised actions |
| Unpatched operating systems | Exploitation of known weaknesses |
| Exposed credentials | Unauthorised cloud access |
| Missing monitoring | Delayed incident detection |
| Inadequate backups | Data loss and recovery difficulties |

## 5. AWS Security Services

| AWS Service | Security Purpose |
|---|---|
| AWS IAM | Identity and access management |
| Amazon GuardDuty | Threat detection |
| AWS Security Hub | Centralised security findings and security posture management |
| Amazon Inspector | Vulnerability management |
| AWS CloudTrail | Account activity auditing |
| Amazon CloudWatch | Monitoring and alerting |
| AWS Shield | Distributed Denial-of-Service protection |
| Amazon Macie | Sensitive data discovery and protection in Amazon S3 |

These services provide different security capabilities and should be selected according to organisational requirements.

## 6. Threat, Vulnerability and Risk Assessment Example

### Scenario: Exposed EC2 Instance

An organisation hosts a web application on an EC2 instance.

The security group allows SSH access from any IP address.

Assessment:

- Asset: EC2 application server.
- Threat: Malicious attacker.
- Vulnerability: Unrestricted SSH access.
- Potential risk: Unauthorised server access.
- CIA principles: Confidentiality, Integrity and Availability.

Recommended remediation:

1. Restrict SSH access to approved IP addresses.
2. Consider AWS Systems Manager Session Manager.
3. Review security group rules.
4. Apply operating system security updates.
5. Monitor authentication and account activity.

## 7. Importance to Cloud Security Engineering

Cloud Security Engineers must be able to:

1. Identify common cloud security threats.
2. Recognise vulnerabilities and misconfigurations.
3. Evaluate the potential business impact of security incidents.
4. Recommend preventive and detective controls.
5. Monitor cloud environments for suspicious activity.
6. Prioritise remediation based on risk.
7. Validate that security controls are effective.

## 8. Key Takeaways

- A threat is something capable of causing harm.
- A vulnerability is a weakness that may be exploited.
- Risk represents the potential consequences of exploitation.
- Cloud misconfigurations are important sources of security exposure.
- Identity management, network controls, encryption and monitoring help reduce security risks.
- AWS provides specialised services for threat detection, vulnerability management and security monitoring.

## 9. References

- [AWS Security Documentation](https://docs.aws.amazon.com/security/)
- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
- [Amazon GuardDuty](https://docs.aws.amazon.com/guardduty/)
- [Amazon Inspector](https://docs.aws.amazon.com/inspector/)
- [AWS Security Hub](https://docs.aws.amazon.com/securityhub/)

---

**Project:** AWS Cloud Security Foundations  
**Module:** Cloud Security Fundamentals  
**Lesson:** Cloud Security Threats and Vulnerabilities  
**Status:** Completed — Foundational Study