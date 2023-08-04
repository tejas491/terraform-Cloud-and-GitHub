# terraform-Cloud-and-GitHub
Guide for infrastructure automation, CI/CD on Terraform usage for GCP with  (https://console.cloud.google.GitHub as VCS

Other resources
* [Terraform Provider for Google Cloud](https://registry.terraform.io/providers/hashicorp/google/latest/docs)
* [google_storage_bucket](https://registry.terraform.io/providers/hashicorp/google/latest/docs/resources/storage_bucket)

Pre-requisites
* A GCP Project with Admin privileges
* A GitHub account for storing the Terraform scripts
* A Terraform Cloud free account

Setup
> Google Cloud
 1. Create a Service Account in [Google Cloud Console](https://console.cloud.google.com/welcome?pli=1&project=speedy-bonsai-391310)
 2. Assign role roles/storage.admin
 3. Create a key and download the key as JSON locally
> GitHub Fork this repository into your own GitHub account
> Terraform Cloud
 1. Create a free account in [Terraform Cloud](https://app.terraform.io/session)
 2. Create a new Organization and Workspace
 3. Choose a Version control workflow with the GitHub repository
 4. Create a new environment variable with the name [GOOGLE_CREDENTIALS](https://registry.terraform.io/providers/hashicorp/google/latest/docs/guides/getting_started#using-terraform-cloud-as-the-backend) with the Service Account JSON file
> [!WARNING]
> Newline characters from the JSON key file must be removed. In Visual Studio Code, type Ctrl + Shift + p for the Join Lines command.
