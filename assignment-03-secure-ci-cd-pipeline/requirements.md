# Assignment 03: Secure Supply-Chain CI/CD Pipeline

## Scenario
Implement automated security gates preventing vulnerabilities and secrets from entering production container registries.

## Requirements
1. SAST (Static Application Security Testing) scanning using Trivy or Semgrep.
2. Secret scanning step to detect leaked API tokens or credentials before merge.
3. Docker image vulnerability scanning failing builds on CRITICAL CVEs.
