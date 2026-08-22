---
title: Users
layout: default
parent: API Reference
nav_order: 1
---

# Users

## Register a user

`POST /api/v1/users/register`

Creates a user after normalizing the email and hashing the password. Password hashes are never returned in JSON.

### Request

```json
{
  "email": "artist@example.com",
  "password": "correct-password"
}
```

### Success: `201 Created`

```json
{
  "id": "9f3c...",
  "email": "artist@example.com"
}
```

### Validation rules

- Email is trimmed, lowercased, and parsed as a valid address.
- Password must contain 8 to 64 Unicode characters.
- The UTF-8 password must also fit bcrypt's 72-byte limit.

### Errors

| Status | Code              | Meaning                                          |
| :----: | :---------------- | :----------------------------------------------- |
| `400`  | `invalid_request` | Email or password is missing                     |
| `400`  | `validation`      | Email or password does not meet validation rules |
| `409`  | `conflict`        | Email is already registered                      |
