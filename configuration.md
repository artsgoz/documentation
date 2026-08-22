---
title: Configuration
layout: default
nav_order: 4
---

# Configuration

The API loads `.env.local` when present. Process environment variables take precedence over values loaded from that file.

| Variable      | Required | Default   | Description                   |
| :------------ | :------: | :-------- | :---------------------------- |
| `DB_HOST`     |   yes    |           | PostgreSQL host               |
| `DB_USER`     |   yes    |           | PostgreSQL user               |
| `DB_NAME`     |   yes    |           | PostgreSQL database           |
| `DB_PASSWORD` |    no    | empty     | PostgreSQL password           |
| `DB_PORT`     |    no    | `5432`    | PostgreSQL port               |
| `DB_SSL_MODE` |    no    | `disable` | PostgreSQL SSL mode           |
| `PORT`        |    no    | `3000`    | HTTP listen port              |
| `GIN_MODE`    |    no    | `release` | `debug`, `release`, or `test` |

The service requires `DB_HOST`, `DB_USER`, and `DB_NAME` at startup. `PORT` must be between `1` and `65535`.
