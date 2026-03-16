# Copilot Code Review Instructions

## Do NOT Report

Issues that static analysis tools catch. Linters, formatters, type checkers,
and other automated tools already run in CI. Copilot should not duplicate
their work. Examples:

- Linting violations (ESLint, Ruff, actionlint, shellcheck, etc.)
- Formatting issues (Prettier, Black, gofmt, etc.)
- Type errors (TypeScript, mypy, etc.)
- Security scanner findings (zizmor, Trivy, gitleaks, etc.)

If a tool in CI would flag it, do not comment on it.

## Review Focus

- Bugs and logic errors
- Security vulnerabilities not caught by automated scanners
- Breaking changes not mentioned in the PR description
- Missing error handling in new code paths
- Missing tests for new functionality
- Architecture and design concerns

## Guidelines

- Only comment when you have high confidence an issue exists
- Be concise: one sentence per comment when possible
- Provide actionable suggestions, not vague observations
