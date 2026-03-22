# Terraform Quickstart

This guide covers common Terraform CLI commands for managing infrastructure as code.

## Prerequisites
- Terraform installed (download from [terraform.io](https://www.terraform.io/downloads))
- AWS credentials configured (via AWS CLI or environment variables)

## Common Commands

### Initialize Workspace
Initialize a Terraform working directory by downloading providers and modules.
```bash
terraform init
```

### Validate Configuration
Check the syntax and configuration of your Terraform files.
```bash
terraform validate
```

### Format Code
Automatically format your Terraform configuration files.
```bash
terraform fmt
```

### Plan Changes
Preview the changes Terraform will make to your infrastructure.
```bash
terraform plan
```

To save the plan to a file:
```bash
terraform plan -out=tfplan
```

### Apply Changes
Apply the planned changes to create, update, or destroy infrastructure.
```bash
terraform apply
```

To apply from a saved plan:
```bash
terraform apply tfplan
```

### Show State
Display the current state of your infrastructure.
```bash
terraform show
```

### Destroy Infrastructure
Remove all resources managed by the current configuration.
```bash
terraform destroy
```

### State Management
List resources in state:
```bash
terraform state list
```

Show details of a specific resource:
```bash
terraform state show aws_s3_bucket.example
```

### Workspace Management
Create a new workspace:
```bash
terraform workspace new dev
```

Switch workspaces:
```bash
terraform workspace select dev
```

List workspaces:
```bash
terraform workspace list
```

### Import Existing Resources
Import existing infrastructure into Terraform state:
```bash
terraform import aws_s3_bucket.example my-existing-bucket
```

### Refresh State
Update the state file with the current status of resources:
```bash
terraform refresh
```

## Tips
- Always run `terraform plan` before `terraform apply` to review changes
- Use `terraform fmt` to keep your code consistently formatted
- Store sensitive values in environment variables or use a secrets manager
- Use workspaces for managing multiple environments