# Terraform Multi-Environment Infrastructure

This repository demonstrates how to manage **multiple environments (Dev, Staging, Production)** using Terraform.

It focuses on structuring Infrastructure as Code (IaC) to support scalable, reusable, and environment-specific deployments.

---

## Project Overview

In real-world applications, infrastructure must be deployed across multiple environments:

**Development (Dev)** → Testing and experimentation
**Staging (Pre-Prod)** → Validation before release
**Production (Prod)** → Live environment

This project implements a structured approach to manage all environments using Terraform while maintaining consistency and flexibility.

---

## Tech Stack

- Terraform
- AWS / Cloud Platform
- HCL (HashiCorp Configuration Language)
- Linux
- Git & GitHub

---

## Key Concepts

This project demonstrates:

- Multi-environment infrastructure design
- Environment-specific configurations
- Reusable Terraform modules
- State isolation per environment
- Infrastructure scalability

---

## Architecture

- Shared Terraform modules define common infrastructure
- Each environment has its own configuration
- Environment-specific values are passed using variables

Example environments:

- `dev` → minimal resources
- `staging` → moderate setup
- `prod` → highly available, scalable setup

---

## Key Features

- Multi-environment support (Dev, Staging, Prod)
- Reusable Terraform modules
- Clean separation of environments
- Scalable and maintainable IaC design
- Production-like infrastructure setup

---

## Setup & Execution

### Navigate to Environment

```bash
cd environments/dev
```

---

### Initialize Terraform

```bash
terraform init
```

---

### Plan Infrastructure

```bash
terraform plan
```

---

### Apply Changes

```bash
terraform apply
```

---

## Example Configuration

```
module "vpc" {
  source = "../../modules/vpc"

  cidr_block = var.cidr_block
}
```

---

## Learning Outcomes

Through this project, I gained:

- Managing multiple environments using Terraform
- Structuring scalable infrastructure code
- Isolating environments safely
- Applying real-world DevOps practices

---

## Future Enhancements

- Add remote backend (S3 + DynamoDB)
- Integrate CI/CD pipelines
- Use Terraform workspaces
- Add environment-specific secrets management

---

## Note

This repository is part of my DevOps learning journey, focusing on managing real-world multi-environment infrastructure using Terraform.

