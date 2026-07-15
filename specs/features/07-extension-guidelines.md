---
type: Playbook
title: Extension guidelines
description: Register routes, prefer JWT clients, and document new endpoints in OKF specs.
tags: [extension, maintainer]
timestamp: 2026-07-15T00:00:00Z
---

# Guidelines

1. Register new routers in `src/index.ts` **after** `authMiddleware` unless public.
2. Prefer `getSupabaseClientWithJWT` over service role for user data.
3. Keep `{ success, data }` / `{ success: false, error }` shape from `src/utils/response.ts`.
4. Add numbered concepts under `specs/features/` and link from [index.md](../../index.md).
5. Add matching `src/api/` module in the frontend and update both `specs/` bundles.
