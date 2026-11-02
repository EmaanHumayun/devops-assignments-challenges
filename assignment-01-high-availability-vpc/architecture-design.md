# Network Architecture Design Document

## Topology Overview
- **VPC CIDR:** `10.100.0.0/16` (65,536 total addresses)
- **Availability Zones:** `us-east-1a`, `us-east-1b`, `us-east-1c`

### Subnet Layout
| Subnet Name | CIDR Block | Usable IPs | Route Target |
| :--- | :--- | :--- | :--- |
| `public-1a` | `10.100.1.0/24` | 251 | Internet Gateway (`igw`) |
| `public-1b` | `10.100.2.0/24` | 251 | Internet Gateway (`igw`) |
| `public-1c` | `10.100.3.0/24` | 251 | Internet Gateway (`igw`) |
| `private-app-1a` | `10.100.10.0/24` | 251 | NAT Gateway A |
| `private-app-1b` | `10.100.20.0/24` | 251 | NAT Gateway B |
| `private-app-1c` | `10.100.30.0/24` | 251 | NAT Gateway A (Failover) |
