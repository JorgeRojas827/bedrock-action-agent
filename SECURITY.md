# Security Policy

## Supported Versions

We actively support and provide security updates for the following versions:

| Version | Supported          |
| ------- | ------------------ |
| 0.6.x   | :white_check_mark: |
| < 0.6.0 | :x:                |

## Reporting a Vulnerability

If you discover a security vulnerability, please **do not** open a public issue. Instead, please report it via one of the following methods:

1. **Email**: Send details to the maintainer at johnreilly.pospos@gmail.com
2. **GitHub Security Advisory**: Use GitHub's private vulnerability reporting feature if available

### What to Include

When reporting a vulnerability, please include:

- Description of the vulnerability
- Steps to reproduce
- Potential impact
- Suggested fix (if any)
- Your contact information

### Response Timeline

- **Initial Response**: Within 48 hours
- **Status Update**: Within 7 days
- **Resolution**: Depends on severity and complexity

## Security Best Practices

### For Users

1. **Use OIDC Authentication**: Prefer GitHub OIDC over storing AWS credentials as secrets
2. **Least Privilege IAM**: Grant only the minimum required permissions to the IAM role/user
3. **Regular Updates**: Keep the action version up to date
4. **Monitor Usage**: Regularly review AWS CloudWatch logs for unusual activity
5. **Secure Secrets**: Never commit AWS credentials or secrets to your repository

### For Maintainers

1. **Dependency Updates**: Regularly update dependencies to patch known vulnerabilities
2. **Code Review**: All changes are reviewed before merging
3. **Security Scanning**: Automated security scanning in CI/CD pipeline
4. **Audit Logs**: Monitor access and usage patterns

## Known Security Considerations

1. **AWS Credentials**: The action requires AWS credentials to invoke Bedrock agents. Use OIDC when possible.
2. **GitHub Token**: The action uses GITHUB_TOKEN to access repository data. This token has limited permissions.
3. **File Content**: The action reads file contents from the repository. Be aware of sensitive data in files.
4. **Prompt Content**: Prompts may contain code or sensitive information. Ensure Bedrock agents are configured appropriately.

## Security Updates

Security updates will be released as patch versions (e.g., 0.6.0 → 0.6.1) and will be documented in the CHANGELOG.md.

