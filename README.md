# Terraform — GCP infrastructure

<div align="center">
  <img src="https://se.ewi.tudelft.nl/desosa2019/chapters/terraform/images/617845e3592d99b71c40470d33c1785090cc4afa.png" alt="Terraform logo" width="500">
</div>

## Overview

This repository manages Google Cloud Platform (GCP) resources for the **devops-workshop-2023** project. It follows a GitOps-style workflow for provisioning and updating:

- Google Cloud Storage (GCS)
- Google Kubernetes Engine (GKE)
- Identity and Access Management (IAM)
- Load balancing
- Virtual Private Cloud (VPC)

## Features

### Infrastructure as code

GCP resources are declared in Terraform configuration files.

### Per-directory Terraform versions

The Terraform runner uses [tfswitch](https://github.com/warrensbox/terraform-switcher). You can pin a Terraform version per directory via `tfswitch.toml`.

### GitLab CI/CD

`.gitlab-ci.yml` defines pipelines for each infrastructure area under the DevOps Workshop 2023 project.

## Contributing to GCP infrastructure

### 1. Open a merge request

1. Create a branch from `master`.
2. Apply your infrastructure changes.
3. Push the branch and open a merge request.
4. Wait for the pipeline **plan** stage to finish successfully and confirm the plan is valid.

### 2. Merge to `master`

1. Merge the MR into `master`.
2. Confirm the post-merge pipeline **plan** stage still succeeds.
3. Manually trigger the **apply** job when you are ready to deploy.
