# Development Environment Setup

## 1. Project Information

| Item | Details |
|---|---|
| Project | AWS Cloud Security Foundations |
| Developer | Prosper Dela |
| Development Machine | MacBook Pro |
| Operating System | macOS |
| Architecture | Apple Silicon (ARM64) |
| Main Editor | Visual Studio Code |

## 2. Installed Tools

| Tool | Version / Configuration |
|---|---|
| AWS CLI | 2.39.3 |
| Python | 3.14.8 |
| AWS CLI Profile | default |
| AWS Region | eu-north-1 |
| Cloud Provider | Amazon Web Services |

## 3. AWS Authentication

AWS CLI authentication was completed using the browser-based `aws login` workflow.

The configured AWS CLI profile was updated to use the new AWS account session.

The AWS identity was subsequently verified using:

```bash
aws sts get-caller-identity
```

No account ID or temporary credentials are recorded in this document.

## 4. AWS Region

Configured region:

```text
eu-north-1
```

Region name: Europe (Stockholm).

The region was verified using:

```bash
aws configure get region
```

## 5. Security Precautions

- Enable MFA on the AWS root account.
- Avoid using the root account for everyday administration.
- Never commit AWS credentials to GitHub.
- Use least-privilege permissions.
- Review AWS pricing before deploying resources.
- Monitor AWS billing and usage.
- Remove unnecessary resources after practical exercises.

## 6. Verification Status

- [x] AWS CLI installed.
- [x] AWS CLI version verified.
- [x] Browser-based authentication completed.
- [x] AWS account identity verified.
- [x] AWS region confirmed.
- [x] Project directory created.
- [ ] Git repository initialized.
- [ ] GitHub repository created.

## 7. Notes

This environment will be used for practical cloud security exercises, AWS CLI operations, technical documentation, and portfolio development.