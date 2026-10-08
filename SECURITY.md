# Security Policy

## Supported Versions

Security fixes are generally applied to the latest version of the project.

| Version | Supported |
|---------|-----------|
| Latest | Yes |
| Older versions | No |

## Reporting a Security Vulnerability

Please do **not** report security vulnerabilities through public GitHub issues, discussions, or pull requests.

Instead, report security vulnerabilities privately to the project maintainers.

When reporting a vulnerability, please include:

- A description of the vulnerability.
- The affected CloudFormation template, resource, or component.
- Steps to reproduce the issue, where possible.
- The potential security impact.
- Any suggested remediation.
- Relevant logs or screenshots, provided they do not contain credentials or other sensitive information.

Please do not include:

- AWS access keys.
- Secret keys.
- Passwords.
- Private keys.
- Tokens.
- Customer or personal data.
- Other sensitive credentials.

If credentials may have been exposed, rotate or revoke them immediately through the appropriate AWS account controls.

## AWS Credentials

AWS credentials and secrets must never be committed to this repository.

Use appropriate AWS mechanisms such as:

- IAM roles.
- GitHub Actions OIDC.
- AWS Secrets Manager.
- AWS Systems Manager Parameter Store.
- Environment-specific secret management.

Avoid storing secrets directly in CloudFormation templates or parameter files committed to Git.

## Security Best Practices

When contributing CloudFormation code:

- Follow the principle of least privilege.
- Avoid wildcard IAM permissions where possible.
- Encrypt sensitive data at rest.
- Enable logging and monitoring where appropriate.
- Use secure network configurations.
- Avoid publicly exposing AWS resources unless explicitly required.
- Keep dependencies and tooling up to date.
- Review CloudFormation changes for unintended resource exposure.

## Disclosure

The project maintainers will assess reported vulnerabilities and determine appropriate remediation and disclosure steps.

Thank you for helping keep this project secure.
