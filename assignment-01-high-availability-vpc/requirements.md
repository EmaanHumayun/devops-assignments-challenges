# Assignment 01: High-Availability Multi-AZ Cloud Network Architecture

## Business Scenario
A high-traffic e-commerce enterprise requires a resilient AWS network architecture capable of withstanding the outage of an entire AWS Availability Zone without downtime.

## Architectural Requirements
1. **CIDR Allocation:** Allocate `10.100.0.0/16` into distinct public and private subnets across 3 Availability Zones.
2. **Egress Isolation:** Private subnets must have outbound internet connectivity via NAT Gateways for security patches, but zero direct inbound internet reachability.
3. **High Availability:** At least 2 NAT Gateways deployed across distinct AZs to avoid a single point of failure (SPOF).
4. **Tagging Standard:** Comply with corporate tagging (`Environment`, `Owner`, `CostCenter`, `IaC`).

## Submission Deliverables
- [x] Terraform Infrastructure as Code (`terraform/main.tf`)
- [x] Network topology writeup (`architecture-design.md`)
