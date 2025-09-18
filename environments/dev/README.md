# Development Environment

This directory contains the configuration for the development environment.

## Usage

```bash
# Initialize Terraform (run from project root)
terraform init

# Plan with dev configuration
terraform plan -var-file="environments/dev/terraform.tfvars"

# Apply with dev configuration
terraform apply -var-file="environments/dev/terraform.tfvars"

# Destroy dev environment
terraform destroy -var-file="environments/dev/terraform.tfvars"
```