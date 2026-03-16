# Copilot Code Review Instructions

## Do NOT Report

- Code formatting (indentation, whitespace, line length, trailing commas)
- Import ordering or grouping
- Missing or extra semicolons
- Unused variables or unused imports
- Type annotation issues or missing type hints
- Shell script quoting or syntax that shellcheck would flag
- YAML/JSON syntax issues
- Known security patterns that scanners detect (hardcoded secrets, CVEs in dependencies)

These are handled by automated tools. Focus on what requires human judgment.

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
