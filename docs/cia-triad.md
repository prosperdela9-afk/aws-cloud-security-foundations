# The CIA Triad — Information Security Fundamentals

## 1. Introduction

The CIA Triad is a foundational information security model consisting of three principles:

1. Confidentiality
2. Integrity
3. Availability

These principles help security professionals protect information systems, applications and data against security threats.

## 2. Confidentiality

### Definition

Confidentiality ensures that information is accessible only to authorised individuals, systems and processes.

### Potential Threats

- Unauthorised access to sensitive information.
- Stolen user credentials.
- Data breaches.
- Excessive user permissions.
- Accidental exposure of confidential files.

### Security Controls

- Identity and Access Management (IAM).
- Least-privilege permissions.
- Multi-factor authentication (MFA).
- Encryption at rest and in transit.
- Strong authentication policies.
- Access monitoring.

### AWS Example

An organisation stores confidential customer records in Amazon S3.

The organisation configures appropriate IAM permissions and S3 bucket policies to ensure that only authorised users and applications can access the records.

**Security objective:** Prevent unauthorised access and disclosure.

## 3. Integrity

### Definition

Integrity ensures that information remains accurate, complete and protected against unauthorised modification or destruction.

### Potential Threats

- Unauthorised modification of records.
- Malware and malicious code.
- Accidental deletion or alteration.
- Database manipulation.
- Compromised user accounts.

### Security Controls

- Cryptographic hashing.
- Digital signatures.
- File integrity monitoring.
- Database access controls.
- Audit logging.
- Version control and recovery mechanisms.

### AWS Example

An organisation enables Amazon S3 Versioning to preserve previous versions of stored objects.

If an object is accidentally overwritten, an earlier version may be recoverable.

Cryptographic hashes can also help verify whether files have changed.

**Security objective:** Maintain trustworthy and accurate information.

## 4. Availability

### Definition

Availability ensures that information, applications and systems remain accessible to authorised users when required.

### Potential Threats

- Distributed Denial-of-Service (DDoS) attacks.
- Hardware failures.
- Network outages.
- Application failures.
- Accidental data deletion.
- Infrastructure disruptions.

### Security Controls

- Regular backups.
- Disaster recovery planning.
- Load balancing.
- Auto Scaling.
- Fault-tolerant architecture.
- Monitoring and alerting.
- DDoS protection.

### AWS Example

An organisation deploys an application across multiple Availability Zones and uses a load balancer to distribute incoming traffic.

This architecture can improve resilience when an individual instance or Availability Zone experiences a failure.

**Security objective:** Keep systems and information accessible when needed.

## 5. CIA Triad Comparison

| Principle | Main Objective | Example Security Threat |
|---|---|---|
| Confidentiality | Prevent unauthorised access | Data breach |
| Integrity | Prevent unauthorised modification | Data tampering |
| Availability | Maintain access to systems and data | Service outage |

## 6. Practical Security Scenario

### Scenario: Healthcare Application Hosted in AWS

An organisation operates a healthcare application that stores sensitive patient records.

**Confidentiality**

Only authorised healthcare personnel should access patient records. IAM permissions, authentication controls and encryption help protect the information.

**Integrity**

Patient records must remain accurate and protected against unauthorised changes. Access controls, audit logs and integrity verification mechanisms help maintain trust.

**Availability**

Healthcare personnel must be able to access the application when required. Backups, monitoring and resilient infrastructure support availability and recovery.

## 7. Importance to Cloud Security Engineering

Cloud Security Engineers use the CIA Triad to evaluate security risks and select appropriate controls.

Their responsibilities include:

1. Protecting sensitive information from unauthorised access.
2. Preventing and detecting unauthorised changes.
3. Designing resilient systems.
4. Implementing appropriate access controls.
5. Monitoring security events.
6. Supporting backup and disaster recovery.
7. Evaluating whether security controls are effective.

## 8. Key Takeaways

- Confidentiality protects information from unauthorised access.
- Integrity protects information against unauthorised modification.
- Availability ensures authorised users can access systems and information when needed.
- Effective security requires balancing all three principles.
- Cloud security controls should be selected based on the risks they address.

## 9. Official References

- [AWS Security Documentation](https://docs.aws.amazon.com/security/)
- [AWS Well-Architected Framework — Security Pillar](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html)
- [AWS Well-Architected Framework — Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html)

---

**Project:** AWS Cloud Security Foundations  
**Module:** Cloud Security Fundamentals  
**Topic:** CIA Triad  
**Status:** Completed