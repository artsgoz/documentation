---
title: Getting Started
layout: default
nav_order: 1
---

# Getting Started

Artsgoz Backend is a Go HTTP API backed by PostgreSQL. The service listens on port `3000` by default and exposes versioned endpoints under `/api/v1`.

## Requirements

- Go 1.22 or newer
- PostgreSQL
- Bundler and Jekyll for this documentation site

## Run the API

Create a local environment file from the backend example, then start the service:

```sh
cp ../artsgoz-backend/.env.example ../artsgoz-backend/.env.local
cd ../artsgoz-backend
go run ./cmd/api
```

Check that the server is running:

```sh
curl http://localhost:3000/healthz
# {"status":"ok"}
```

## First request

```sh
curl -i -X POST http://localhost:3000/api/v1/users/register \\
  -H 'Content-Type: application/json' \\
  -d '{"email":"artist@example.com","password":"correct-password"}'
```

A successful request returns `201 Created` and the new user ID. See [Users](api/users.md) for request validation and error responses.
