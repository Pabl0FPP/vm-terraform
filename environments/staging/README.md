# Staging Environment

This directory contains the configuration for the staging environment.

## Usage

```bash
# Initialize Terraform (run from project root)
terraform init

# Plan with staging configuration
terraform plan -var-file="environments/staging/terraform.tfvars"

# Apply with staging configuration
terraform apply -var-file="environments/staging/terraform.tfvars"

# Destroy staging environment
terraform destroy -var-file="environments/staging/terraform.tfvars"
```