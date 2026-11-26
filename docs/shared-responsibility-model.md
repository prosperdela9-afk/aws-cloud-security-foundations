# AWS Shared Responsibility Model

## 1. Introduction

The AWS Shared Responsibility Model explains how security responsibilities are divided between Amazon Web Services (AWS) and its customers.

The model is based on two fundamental principles:

- **Security OF the cloud:** AWS is responsible for protecting the infrastructure that runs AWS services.
- **Security IN the cloud:** Customers are responsible for protecting their data, applications, identities, configurations and workloads within AWS.

Understanding this model is essential for designing, implementing and maintaining secure cloud environments.

## 2. AWS Responsibilities — Security OF the Cloud

AWS is responsible for securing the underlying infrastructure and facilities that provide its cloud services.

Examples include:

- Physical data centre security.
- Physical servers and storage infrastructure.
- Networking infrastructure.
- Hardware maintenance.
- Physical access controls.
- Infrastructure resilience and availability.

AWS maintains these controls to protect the underlying cloud environment.

## 3. Customer Responsibilities — Security IN the Cloud

Customers are responsible for securing the resources, workloads and data they deploy or configure in AWS.

Examples include:

- Identity and Access Management (IAM).
- User permissions and least-privilege access.
- Multi-factor authentication (MFA).
- Data encryption and protection.
- Network security configurations.
- Operating system patching on Amazon EC2.
- Application security.
- Logging, monitoring and incident response.

The exact responsibilities depend on the AWS service being used.

## 4. Responsibility by AWS Service

| AWS Service | AWS Responsibility | Customer Responsibility |
|---|---|---|
| Amazon EC2 | Physical infrastructure and virtualisation | Guest OS, patches, applications, security groups and data |
| Amazon S3 | Storage infrastructure and underlying platform | Bucket permissions, data protection, encryption configuration and access policies |
| AWS Lambda | Underlying infrastructure and managed execution environment | Function code, permissions, application security and data |
| Amazon RDS | Underlying infrastructure and managed database platform | Database access, data, user permissions and applicable configuration |

## 5. Practical Security Scenarios

### Scenario 1: Unrestricted SSH Access

A company configures its EC2 security group to allow SSH access from any IP address.

**Security responsibility:** Customer.

**Risk:** Unauthorised access attempts against the virtual server.

**Recommended control:** Restrict SSH access to approved IP addresses or use a managed access method such as AWS Systems Manager Session Manager where appropriate.

### Scenario 2: Public S3 Bucket

A company accidentally makes a storage bucket publicly accessible.

**Security responsibility:** Customer.

**Risk:** Unauthorised exposure of stored information.

**Recommended control:** Apply appropriate bucket policies, enable S3 Block Public Access where suitable, and regularly review permissions.

### Scenario 3: Unpatched EC2 Operating System

A company fails to install security updates on its Ubuntu EC2 instance.

**Security responsibility:** Customer.

**Risk:** Attackers may exploit known operating system vulnerabilities.

**Recommended control:** Establish a regular patch management process and verify that security updates are applied.

## 6. Importance to Cloud Security Engineering

A Cloud Security Engineer must understand the boundary between provider and customer responsibilities.

Key activities include:

1. Identifying security misconfigurations.
2. Applying least-privilege access controls.
3. Reviewing network exposure.
4. Protecting sensitive data.
5. Monitoring cloud activity.
6. Assessing security risks.
7. Implementing and validating security controls.

The Shared Responsibility Model helps security engineers determine which controls must be implemented and maintained by their organisation.

## 7. Key Takeaways

- AWS secures the infrastructure OF the cloud.
- Customers secure their resources and workloads IN the cloud.
- Responsibility varies depending on the AWS service.
- Managed services reduce some operational responsibilities but do not eliminate customer security responsibilities.
- Cloud security requires continuous configuration review, monitoring and risk management.

## 8. Official References

- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
- [AWS Shared Responsibility Model — Documentation](https://docs.aws.amazon.com/whitepapers/latest/introduction-aws-security/welcome.html)

---

**Project:** AWS Cloud Security Foundations  
**Module:** Cloud Security Fundamentals  
**Topic:** Shared Responsibility Model  
**Status:** Completed