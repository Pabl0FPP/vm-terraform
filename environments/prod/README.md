# Production Environment

This directory contains the configuration for the production environment.

## Usage

```bash
# Initialize Terraform (run from project root)
terraform init

# Plan with production configuration
terraform plan -var-file="environments/prod/terraform.tfvars"

# Apply with production configuration (use with caution!)
terraform apply -var-file="environments/prod/terraform.tfvars"

# Destroy production environment (DANGEROUS!)
terraform destroy -var-file="environments/prod/terraform.tfvars"
```