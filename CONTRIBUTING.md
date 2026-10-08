# Contributing

Thank you for your interest in contributing to this project.

This repository contains AWS CloudFormation infrastructure code. Contributions are welcome, but changes to infrastructure should be reviewed carefully because they may affect AWS resources and environments.

## Before You Start

Please read the following before making changes:

- The `README.md` for project-specific documentation.
- The `SECURITY.md` file for security-related issues.
- The Code of Conduct for expected community behavior.

## Development Workflow

### 1. Create a branch

Create a feature or fix branch from `main`:

```bash
git switch main
git pull
git switch -c feature/my-change
```

Use a descriptive branch name, for example:

```text
feature/add-alb
feature/update-rds
fix/iam-policy
docs/update-readme
```

### 2. Make your changes

Keep changes focused and avoid mixing unrelated changes in the same pull request.

For CloudFormation changes:

- Follow the existing template structure and naming conventions.
- Use parameters and mappings where appropriate.
- Avoid hard-coding environment-specific values.
- Follow the principle of least privilege for IAM resources.
- Add or update outputs when they are required by dependent stacks.
- Update documentation when behavior or configuration changes.

### 3. Validate CloudFormation templates

Before opening a pull request, validate the templates locally.

For example:

```bash
cfn-lint cloudformation/**/*.yaml
```

You should also validate templates using the AWS CLI where appropriate:

```bash
aws cloudformation validate-template \
  --template-body file://path/to/template.yaml
```

If the repository provides validation scripts, use those instead.

### 4. Commit your changes

Use clear commit messages that describe the change:

```text
Add ALB security group
Update RDS parameter group
Fix IAM policy permissions
```

Avoid committing:

- AWS credentials
- Access keys
- Secret values
- Passwords
- Private keys
- `.env` files containing secrets
- Other sensitive information

### 5. Open a Pull Request

Push your branch:

```bash
git push -u origin feature/my-change
```

Then open a pull request against `main`.

The pull request should explain:

- What changed.
- Why the change was needed.
- Which CloudFormation stacks or resources are affected.
- How the change was tested or validated.
- Any potential impact or required migration steps.

## Pull Request Guidelines

Pull requests should:

- Have a clear and descriptive title.
- Contain only related changes.
- Pass automated checks.
- Include appropriate documentation updates.
- Include testing or validation information.
- Avoid unnecessary formatting or unrelated changes.

Infrastructure changes should receive appropriate review before being deployed to shared or production environments.

## Infrastructure Changes

When making changes to AWS infrastructure, consider:

- Resource replacement.
- Data loss.
- Downtime.
- Security group changes.
- IAM permission changes.
- Changes to networking.
- Changes to encryption.
- Changes to backups and retention.
- Changes to costs.

For potentially destructive changes, clearly highlight the risk in the pull request.

## Questions

If you are unsure about an implementation, open an issue or discussion before making a significant change.

Thank you for contributing!
