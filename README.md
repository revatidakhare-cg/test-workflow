# CI/CD Pipeline Setup

## Overview

This repository contains a production-grade CI/CD pipeline using GitHub Actions for deploying infrastructure on Azure using Terraform.

## Setup Instructions

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/yourrepository.git
   cd yourrepository
   ```

2. **Configure Azure credentials:**

   Go to your GitHub repository settings and add the following secrets:

   - `AZURE_CLIENT_ID`
   - `AZURE_TENANT_ID`
   - `AZURE_SUBSCRIPTION_ID`

   These secrets are needed for authentication with Azure.

3. **Modify the infrastructure configuration:**

   Update the `infra/main.tf` file to match your infrastructure requirements.

4. **Run the pipeline:**

   Push changes to the `main` branch to trigger the pipeline:

   ```bash
   git add .
   git commit -m "Update infrastructure"
   git push origin main
   ```

## Deployment Instructions

The pipeline is configured to:

- Validate the Terraform configuration.
- Create a Terraform plan.
- Apply the plan to deploy resources on Azure.

Ensure that any changes to the infrastructure are pushed to the `main` branch to automatically trigger the deployment process.