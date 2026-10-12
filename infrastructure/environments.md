---
title: Environments
layout: default
nav_order: 1
parent: Environments & Infrastructure
---

# Environments

We maintain three distinct environments that directly correspond to our Git branches (`develop`, `staging`, and `prod`).

- **Development (`dev`)**: The playground for active development. This environment updates frequently and might occasionally be unstable.
- **Staging**: An exact replica of production used for QA testing, bug verification, and final reviews before a release.
- **Production (`prod`)**: The live, public-facing applications used by our actual users.

> {: .note }
> Please read [branch strategy](../WoW/branch-and-pr) first

## Service URLs

Below is the directory of our active services and their corresponding URLs across all three environments:

| Service            | Development (Dev)                                                        | Staging                                                                          | Production (Prod)                                                |
| ------------------ | ------------------------------------------------------------------------ | -------------------------------------------------------------------------------- | ---------------------------------------------------------------- |
| Artsgoz Web        | [dev.web.artsgoz.com](https://dev.web.artsgoz.com)                       | [staging.web.artsgoz.com](https://staging.web.artsgoz.com)                       | [www.artsgoz.com](https://www.artsgoz.com)                       |
| Artsgoz Backoffice | [dev.backoffice.artsgoz.com](https://dev.backoffice.artsgoz.com)         | [staging.backoffice.artsgoz.com](https://staging.backoffice.artsgoz.com)         | [backoffice.artsgoz.com](https://backoffice.artsgoz.com)         |
| Artsgoz Aksornsara | [dev.aksornsara.artsgoz.com](https://dev.aksornsara.artsgoz.com)         | [staging.aksornsara.artsgoz.com](https://staging.aksornsara.artsgoz.com)         | [aksornsara.artsgoz.com](https://aksornsara.artsgoz.com)         |
| Aksornsara API     | [dev.api.aksornsara.artsgoz.com](https://dev.api.aksornsara.artsgoz.com) | [staging.api.aksornsara.artsgoz.com](https://staging.api.aksornsara.artsgoz.com) | [api.aksornsara.artsgoz.com](https://api.aksornsara.artsgoz.com) |
