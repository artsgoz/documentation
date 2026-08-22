---
title: Artsgoz API
layout: home
---

# Artsgoz API

Documentation for the Artsgoz backend: a Go API built with Gin, GORM, and PostgreSQL.

## Explore the API

- [Getting Started](getting-started/) — run the service and make your first request.
- [API Reference](api/) — browse the available endpoints.
- [Users](api/users/) — register users and handle validation errors.

## Understand the service

- [Architecture](architecture/) — follow a request from Gin to PostgreSQL.
- [Configuration](configuration/) — configure the API and database connection.
- [Development](development/) — run checks and build this documentation locally.

## Quick check

Once the API is running, verify its health:

```sh
curl http://localhost:3000/healthz
```

```json
{ "status": "ok" }
```
