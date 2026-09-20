# AeeWizard Repository Policy

This repository follows the AeeWizard/Aeelato portability and infrastructure policy.

## Core rule
The repository must remain operationally portable and must not become dependent on GitHub Actions or another hosted CI system for normal development, deployment, repository transfer, GitHub-account migration, or project migration.

## GitHub Actions guardrail
- Automatic runner-consuming triggers are prohibited by default.
- Do not add `push`, `pull_request`, `schedule`, `workflow_run`, `repository_dispatch`, or automatic matrix fan-out unless an explicit architecture decision deliberately changes this policy.
- Manual diagnostics are allowed when intentionally requested.
- Normal application operation and deployment must not require a GitHub Actions runner.

## Portability
This policy must travel with the repository during forks, transfers, ownership changes, and GitHub-account migrations. Preserve it when moving the repository.

## Provider/infrastructure
Use replaceable provider adapters, configuration-driven switching, infrastructure abstraction, and portable data wherever practical.

Changes that materially weaken this policy are infrastructure/architecture changes and should be reviewed explicitly.
