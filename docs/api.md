---
layout: default
title: API Reference
parent: Dokumentasi
nav_order: 2
---

# API Reference

Dokumentasi lengkap API QoutaID.

{: .fs-6 .fw-300 }

---

## Authentication

Semua request API memerlukan authentication menggunakan API key.

### Header

```http
Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
```

---

## Endpoints

### Base URL

```
https://api.qouta.id/v1
```

---

## Users

### Get User Profile

```http
GET /users/me
```

**Response:**

```json
{
  "id": "user_123",
  "name": "John Doe",
  "email": "john@example.com",
  "created_at": "2024-01-01T00:00:00Z"
}
```

---

### Update User Profile

```http
PATCH /users/me
```

**Request Body:**

```json
{
  "name": "New Name",
  "avatar_url": "https://example.com/avatar.jpg"
}
```

---

## Error Handling

API menggunakan HTTP status codes standar:

| Status Code | Deskripsi |
|:------------|:----------|
| 200 | OK - Request berhasil |
| 400 | Bad Request - Request tidak valid |
| 401 | Unauthorized - API key tidak valid |
| 404 | Not Found - Resource tidak ditemukan |
| 500 | Internal Server Error - Kesalahan server |

---

## Rate Limiting

API memiliki rate limit sebesar:

- 100 requests per menit untuk free tier
- 1000 requests per menit untuk pro tier

Header response akan menyertakan informasi rate limit:

```http
X-RateLimit-Limit: 100
X-RateLimit-Remaining: 95
X-RateLimit-Reset: 1640000000
```
