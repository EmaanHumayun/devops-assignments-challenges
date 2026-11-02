# DevOps & Systems Architecture Assignments

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Assignments](https://img.shields.io/badge/Assignments-Complete-success)](#assignments-overview)
[![Level](https://img.shields.io/badge/Level-Mid--to--Senior-purple)](#)

A repository of production-oriented architectural assignments, case-study problem statements, code challenges, and infrastructure design submissions.

---

## 📌 Assignments Overview

| Assignment | Topic & Domain | Architectural Pattern | Deliverable |
| :--- | :--- | :--- | :--- |
| **[Assignment 01](./assignment-01-high-availability-vpc/)** | Resilient Multi-AZ VPC | High Availability Network Design | Terraform IaC + CIDR calculation |
| **[Assignment 02](./assignment-02-zero-downtime-k8s-rollout/)** | Zero-Downtime Rollouts | Kubernetes Blue/Green & Canary | K8s Manifests + Envoy Ingress |
| **[Assignment 03](./assignment-03-secure-ci-cd-pipeline/)** | Supply Chain Security | DevSecOps & Image Signing | GitHub Actions + Trivy + Cosign |
| **[Assignment 04](./assignment-04-observability-prometheus-grafana/)** | SRE & Observability | RED Method Telemetry | Prometheus Rules + Grafana JSON |

---

## 🏗️ Assignment 01: High-Availability VPC Architecture

```mermaid
flowchart TD
    IGW["Internet Gateway"] --> ALB["Application Load Balancer (Public Subnets)"]
    subgraph VPC ["AWS VPC 10.0.0.0/16"]
        subgraph AZ1 ["Availability Zone us-east-1a"]
            Pub1["Public Subnet 10.0.1.0/24\nNAT Gateway 1"]
            Priv1["Private Subnet 10.0.10.0/24\nEKS Worker Node 1"]
        end
        subgraph AZ2 ["Availability Zone us-east-1b"]
            Pub2["Public Subnet 10.0.2.0/24\nNAT Gateway 2"]
            Priv2["Private Subnet 10.0.20.0/24\nEKS Worker Node 2"]
        end
    end
    ALB --> Priv1
    ALB --> Priv2
```

---

## 👤 Author

**Emaan Humayun**
- GitHub: [@EmaanHumayun](https://github.com/EmaanHumayun)
- LinkedIn: [Emaan Humayun](https://linkedin.com/in/www.linkedin.com/in/emaanmuhammadhumayun)
- Email: [emaanhumayun23072@gmail.com](mailto:emaanhumayun23072@gmail.com)
