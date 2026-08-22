---
title: Architecture
layout: default
nav_order: 3
---

# Architecture

Artsgoz is organized as flat feature packages. Each feature owns its model, repository, service, handler, and route registration.

```text
Gin handler -> Service -> Repository interface <- GORM repository
```

## Package map

| Package                      | Responsibility                                             |
| :--------------------------- | :--------------------------------------------------------- |
| `cmd/api`                    | Composition root and HTTP server lifecycle                 |
| `internal/server`            | Gin engine, middleware, and health check                   |
| `internal/user`              | User model, registration behavior, persistence, and routes |
| `internal/platform/config`   | Environment loading and validation                         |
| `internal/platform/postgres` | Database connection and pool lifecycle                     |

## Request lifecycle

1. The handler binds the JSON request.
2. The service validates, normalizes, and hashes input.
3. The repository writes the user through GORM.
4. PostgreSQL uniqueness errors become `ErrEmailAlreadyExists`.
5. The handler maps expected errors to stable HTTP responses.

The composition root registers the versioned API group and wires dependencies explicitly. Feature packages do not create database connections or read environment variables.
