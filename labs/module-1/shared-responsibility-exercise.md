# Practical Exercise 1: AWS Shared Responsibility Model

## 1. Objective

Demonstrate an understanding of the AWS Shared Responsibility Model by identifying which security responsibilities belong to AWS and which belong to the customer.

## 2. Scenario

A healthcare organisation hosts a patient records application using three AWS services:

- Amazon EC2 to host its application.
- Amazon S3 to store patient records.
- AWS Lambda to execute application functions.

The organisation must understand its security responsibilities to protect patient information and maintain reliable services.

## 3. Exercise: Identify Security Responsibilities

For each responsibility below, identify whether it belongs to AWS or the customer.

| No. | Security Responsibility | Responsible Party |
|---|---|---|
| 1 | Physical security of AWS data centres | AWS |
| 2 | Managing IAM user permissions | Customer |
| 3 | Maintaining physical server hardware | AWS |
| 4 | Configuring S3 bucket permissions | Customer |
| 5 | Protecting application data | Customer |
| 6 | Maintaining the physical network infrastructure | AWS |
| 7 | Configuring EC2 security groups | Customer |
| 8 | Managing access to application resources | Customer |
| 9 | Maintaining the underlying infrastructure used by Lambda | AWS |
| 10 | Protecting application code and its dependencies | Customer |

## 4. Service-Specific Responsibility Analysis

### Amazon EC2

AWS responsibilities:
- Physical data centre security.
- Physical server and hardware maintenance.
- Underlying network infrastructure.

Customer responsibilities:
- Operating system security and patching.
- IAM permissions.
- Security group configuration.
- Application security.
- Data protection.

### Amazon S3

AWS responsibilities:
- Physical storage infrastructure.
- Underlying infrastructure availability and maintenance.
- Physical data centre security.

Customer responsibilities:
- Bucket permissions and access policies.
- Data classification.
- Encryption configuration and key management choices.
- Data protection and retention settings.

### AWS Lambda

AWS responsibilities:
- Underlying server infrastructure.
- Physical infrastructure security.
- Managed runtime infrastructure.

Customer responsibilities:
- Lambda function code.
- Function permissions and execution roles.
- Application dependencies.
- Secure handling of application data.
- Configuration of environment variables and secrets.

## 5. Security Findings

The exercise highlights several important security considerations:

1. AWS manages the security of its underlying cloud infrastructure.
2. Customers remain responsible for securing their data and access permissions.
3. EC2 customers have additional responsibilities because they manage the guest operating system.
4. Managed services such as Lambda reduce infrastructure management responsibilities but do not eliminate customer security responsibilities.
5. Misconfigured permissions can expose sensitive information even when the underlying AWS infrastructure is secure.

## 6. Recommendations

For the healthcare application, the following security measures are recommended:

- Apply least-privilege IAM permissions.
- Enable MFA for privileged accounts.
- Restrict access to S3 buckets.
- Encrypt sensitive patient information.
- Regularly patch EC2 operating systems.
- Monitor access and configuration changes.
- Review Lambda execution roles and application dependencies.

## 7. Conclusion

The AWS Shared Responsibility Model divides security responsibilities between AWS and its customers.

AWS protects the underlying cloud infrastructure, while customers are responsible for securing their data, identities, applications and service configurations according to the services they use.

Understanding this distinction helps cloud security engineers identify security gaps and apply appropriate controls.

## 8. Evidence and Validation

**Exercise type:** Scenario-based security assessment.

**Environment:** Simulated healthcare application.

**AWS resources created:** None.

**Cost incurred:** No AWS resources were deployed.

**Validation:** Responsibilities were classified for EC2, S3 and Lambda using the AWS Shared Responsibility Model.

**Status:** Completed — Practical Analysis.

## 9. References

- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
- [AWS Shared Responsibility Model Documentation](https://docs.aws.amazon.com/whitepapers/latest/aws-risk-and-compliance/shared-responsibility-model.html)