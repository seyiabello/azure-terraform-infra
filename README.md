🌩️ Nimbus Terraform Infrastructure — Azure IaC Deployment

This repository contains a complete Infrastructure-as-Code (IaC) deployment using Terraform on Microsoft Azure. It provisions a fully automated cloud environment including AKS, ACR, Key Vault, Storage Accounts, RBAC permissions, and remote state management.

This project reflects how DevOps engineers manage production-ready cloud platforms using Terraform.

🚀 What This Project Deploys
🔹 Core Azure Resources

Azure Kubernetes Service (AKS)

Azure Container Registry (ACR)

Azure Key Vault

Azure Storage Account + Blob Container

Resource Group

Automatically generated AKS components:

VM Scale Set

Load Balancer

Public IP

Nodepool resources

NSGs

Managed Identities

🔐 RBAC & Security

The project configures essential Azure RBAC assignments so AKS can securely interact with other services:

Role	Purpose
AcrPull	Allows AKS to pull container images from ACR
Key Vault Secrets Officer	Allows AKS to read secrets from Key Vault

All permissions are assigned through Terraform, ensuring secure, automated, and repeatable deployments.

📦 Remote State Backend

Terraform state is stored in an Azure Blob Container using the backend.tf configuration.

This enables:

Team collaboration

Versioning

Disaster recovery

Consistent automation pipelines

Remote state is essential for real DevOps workflows.

📁 Repository Structure
terraform/
│
├── provider.tf
├── main.tf
├── backend.tf
├── aks.tf
├── acr.tf
├── keyvault.tf
├── storage.tf
├── rbac.tf
├── variables.tf
├── locals.tf
└── output.tf

📸 Screenshots from Deployment
1️⃣ Terraform Apply — Successful Deployment

2️⃣ Terraform Remote State Stored in Blob Container

3️⃣ Azure Storage Account → Containers View

4️⃣ Primary Resource Group — All Main IaC Resources

5️⃣ AKS Node Resource Group — Automatically Created Components

🧠 Skills Demonstrated in This Project

Terraform Provider configuration

Modular IaC (variables, locals, outputs)

AKS, ACR, Key Vault, Storage provisioning

RBAC role assignments

Remote state backend using Azure Storage

Debugging Terraform plans

Azure resource validation

Real-world DevOps infrastructure workflow

🎯 Project Outcome

This project deploys a production-style Azure environment fully automated with Terraform.
It demonstrates real DevOps competencies:

✔ IaC automation
✔ Secure, least-privilege RBAC
✔ Remote state in Azure
✔ Modular Terraform design
✔ Cloud architecture understanding