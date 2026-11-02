# Assignment 02: Zero-Downtime Kubernetes Canary & Blue/Green Deployments

## Scenario
A critical payment transaction microservice cannot tolerate any dropped requests during production releases.

## Requirements
1. Configure Kubernetes RollingUpdate strategy with `maxSurge: 25%` and `maxUnavailable: 0`.
2. Implement rigorous HTTP Readiness probes targeting `/healthz` to ensure pods receive traffic only after warm-up.
3. Configure preStop lifecycle hooks allowing in-flight requests 15 seconds to drain before SIGKILL.
