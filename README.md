# aws-tf-examples
A collection of Terraform examples for AWS resources.

## Structure

- `tf/{infra-name}/`: Main Terraform configuration files for each infrastructure component.
- `{env}/{region}/{infra-name}/`: Environment and region-specific variable files.

## Workflows

GitHub Actions workflows are configured to run Terraform plans using the main configurations and environment-specific variables.
