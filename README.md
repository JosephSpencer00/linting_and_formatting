# Pre-Commit Hooks and Linting Demo
## Purpose
This repository demonstrates the use of pre-commit hooks and linting tools to write secure, clean, and formatted Python code. By leveraging automated tools, developers can ensure code quality and security while minimizing manual review efforts.

## Overview
Pre-commit hooks: These are scripts that run automatically before a commit is finalized, ensuring that the code adheres to defined standards and practices.
Linting: Using tools like Black, Ruff, Mypy, and Bandit to enforce code style, catch errors, and identify security vulnerabilities.
## Files
original.py
This file contains the initial version of the code, which has not been formatted or linted.
It serves as a baseline to compare against the formatted version.
formatted.py
This file is a reformatted version of original.py, created using the pre-commit hooks.
The formatting tools automatically adjust whitespace, code structure, and style according to defined standards.
## Pre-Commit Hook Configuration
A .pre-commit-config.yaml file was created to set up pre-commit hooks that only affect the formatted.py file.
The hooks are configured to run only when changes are made to formatted.py, ensuring efficient use of resources.
## Hook Setup
### Black: 
Automatically formats code to adhere to PEP 8 standards.
### Ruff: 
Lints the code, catching various coding issues and style violations.
### Mypy: 
Type checks the code for correctness.
### Bandit: 
Analyzes code for security vulnerabilities.
## Initial Run Results
Upon the first run of the pre-commit hooks:
Black: Passed (formatting changes made).
Ruff: Passed (no issues found).
Mypy: Passed (no type errors detected).
Bandit: Failed with a warning for a hardcoded password.
Warning: Detected a possible hardcoded password: 123456.
## Bandit Warning Handling
To temporarily bypass the Bandit warning for testing purposes, the following comment was added to formatted.py:
\# nosec
This instructs Bandit to ignore the warning related to the hardcoded password in the code.
## Final Code Differences
Key Changes in formatted.py:
Whitespace Removal: Excess whitespace was eliminated to enhance readability.
Code Formatting: Code structure and style were adjusted according to PEP 8 standards.
Security Comment: The # nosec comment was added to suppress Bandit warnings for the hardcoded password.
