---
type: Feature
title: Middleware
description: Logger, CORS, error handler, and JWT auth middleware stack.
tags: [hono, middleware, cors, jwt]
timestamp: 2026-07-15T00:00:00Z
---

# Stack

1. **Logger** — request logging
2. **CORS** — respects `ALLOWED_ORIGINS` when set
3. **Error handler** — standardized JSON errors
4. **Auth** — all routes except `/health`; extracts JWT `sub`, rejects invalid tokens

See [.agents/skills/shared/auth/jwt-api-passthrough.md](../../.agents/skills/shared/auth/jwt-api-passthrough.md).
