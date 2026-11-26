# Security Controls and Defence in Depth

## 1. Introduction

Security controls are safeguards implemented to protect cloud infrastructure, applications, networks and data from security threats.

They help organisations prevent security incidents, detect suspicious activities, reduce vulnerabilities and recover from security events.

Defence in depth is a security strategy that combines multiple layers of protection instead of relying on a single security measure.

## 2. Types of Security Controls

Security controls are commonly grouped into three categories.

### 2.1 Preventive Controls

Preventive controls are designed to stop security incidents before they occur.

Examples include:

- **IAM policies:** Restrict access to cloud resources based on user permissions.
- **Multi-Factor Authentication (MFA):** Adds an additional verification step during authentication.
- **Security Groups:** Control inbound and outbound network traffic.
- **Encryption:** Protects sensitive information from unauthorised access.

### 2.2 Detective Controls

Detective controls identify suspicious activities, security incidents and weaknesses.

Examples include:

- **AWS CloudTrail:** Records account activity and API events.
- **Amazon GuardDuty:** Detects potential threats and suspicious behaviour.
- **Amazon CloudWatch:** Monitors logs, metrics and application activity.
- **AWS Security Hub:** Provides a central view of security findings across supported AWS services.

### 2.3 Corrective Controls

Corrective controls help organisations respond to incidents, fix weaknesses and restore normal operations.

Examples include:

- Revoking compromised credentials.
- Restoring information from backups.
- Patching vulnerable software.
- Removing unauthorised access permissions.
- Rebuilding compromised infrastructure.

Some controls support multiple security objectives depending on how they are implemented.

## 3. Defence in Depth

Defence in depth is the practice of implementing multiple security layers to protect systems and information.

The objective is to ensure that the failure of one security control does not automatically compromise the entire environment.

For example, an administrator account can be protected through:

1. Strong password requirements.
2. Multi-Factor Authentication.
3. Least-privilege IAM permissions.
4. Activity monitoring through CloudTrail.
5. Suspicious activity detection.
6. Incident response and recovery procedures.

Each layer contributes to the overall security of the environment.

## 4. Applying Security Controls in AWS

Consider a healthcare application hosted on AWS.

The application runs on EC2 instances and stores patient records in Amazon S3.

| Security Requirement | Example Control | Category |
|---|---|---|
| Restrict access to patient records | IAM least privilege | Preventive |
| Strengthen account authentication | MFA | Preventive |
| Restrict network connections | Security Groups | Preventive |
| Record account activity | CloudTrail | Detective |
| Identify suspicious behaviour | GuardDuty | Detective |
| Restore deleted records | S3 versioning and backups | Corrective / Recovery |
| Fix vulnerable software | Security patching | Corrective |

These controls work together to protect the application, its infrastructure and its sensitive information.

## 5. Why Defence in Depth Matters

Defence in depth is important because:

- No single security control is completely reliable.
- Multiple security layers reduce the impact of individual control failures.
- Monitoring helps organisations identify incidents earlier.
- Recovery controls support business continuity.
- Different layers protect different parts of the cloud environment.

A strong security strategy combines identity management, network security, data protection, monitoring and incident response.

## 6. Key Takeaways

- Security controls protect systems and information against threats.
- Preventive controls aim to stop incidents.
- Detective controls identify suspicious activities.
- Corrective controls help fix problems and restore operations.
- Defence in depth combines multiple security layers.
- Effective cloud security requires continuous monitoring, assessment and improvement.

## 7. Conclusion

Cloud security is not achieved by deploying a single tool or implementing one security measure.

It requires multiple coordinated controls that prevent unauthorised access, detect suspicious activity and support recovery when incidents occur.

Understanding security controls and defence in depth provides an important foundation for practical cloud security engineering.

## 8. References

- [AWS Security Best Practices](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
- [AWS Identity and Access Management](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html)
- [AWS CloudTrail Documentation](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-user-guide.html)
- [Amazon GuardDuty Documentation](https://docs.aws.amazon.com/guardduty/latest/ug/what-is-guardduty.html)
- [AWS Security Incident Response Guide](https://docs.aws.amazon.com/whitepapers/latest/aws-security-incident-response-guide/welcome.html)

**Status:** Completed — Foundational Study