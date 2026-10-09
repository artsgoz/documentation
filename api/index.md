---
title: API Reference
layout: default
nav_order: 1
has_children: true
---

# API Reference

The API is served by Gin and is versioned at `/api/v1`. Responses use JSON and errors follow a stable envelope:

```json
{
  "error": {
    "code": "validation",
    "message": "..."
  }
}
```

## Available endpoints

| Method | Path                     | Purpose              |
| :----: | :----------------------- | :------------------- |
| `GET`  | `/healthz`               | Check process health |
| `POST` | `/api/v1/users/register` | Register a user      |

The endpoint pages document the current public contract. Internal package boundaries are covered in [Architecture](../architecture/).
