---
title: Terraform
layout: default
nav_order: 3
has_children: true
---

# Terraform Overview

Owner: [@teruyukii](https://github.com/teruyukii)

{: .warning }

> This page is not completed yet. WIP//Teru Oct 12, 2026

## Infrastructure as code

Terraform is split into two layers:

- `infra/terraform/bootstrap/<product>` enables the initial services and creates the Terraform deployer identity and versioned state bucket.
- `infra/terraform/env/<environment>/<product>` manages the application infrastructure for one product in one environment.

Reusable modules are present for:

- Google API enablement
- IAM roles and service accounts
- Cloud Build triggers and Terraform plan storage
- Firebase deployment permissions
- public and private Cloud Storage buckets
- Secret Manager resources
- Artifact Registry repositories

The current environment roots use the project-services, IAM, storage, and Cloud Build modules. The Secret Manager and Artifact Registry modules are available but are not currently instantiated by those roots.

Firebase custom-domain associations are declared in Terraform, but external DNS records are outside this repository and must be configured with the DNS provider.
