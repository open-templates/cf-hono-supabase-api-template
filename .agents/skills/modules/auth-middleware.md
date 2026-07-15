---
type: Playbook
title: Auth middleware
description: Reject unauthenticated requests except GET /health.
tags: [hono, jwt, middleware]
timestamp: 2026-07-15T00:00:00Z
resource: src/middleware/auth.ts
---

1. If path is `/health`, call `next()`.
2. Parse `Authorization: Bearer <token>`.
3. Validate JWT; set user id on context.
4. Return `401` with `UNAUTHORIZED` code on failure.

See [shared/auth/jwt-api-passthrough.md](../shared/auth/jwt-api-passthrough.md).
