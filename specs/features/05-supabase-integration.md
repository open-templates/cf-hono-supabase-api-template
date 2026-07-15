---
type: Feature
title: Supabase integration
description: JWT, anon, and service-role Supabase clients in the worker.
tags: [supabase, cloudflare]
timestamp: 2026-07-15T00:00:00Z
resource: src/lib/supabase.ts
---

# Client helpers

| Helper | When to use |
|--------|-------------|
| `getSupabaseClientWithJWT(env, token)` | User-scoped reads/writes (`/me`, RLS tables) |
| `getSupabaseUserClient(env)` | Anonymous public reads |
| `getSupabaseAdminClient(env)` | Service-role (use sparingly) |

No custom database tables required for the default template.

See [.agents/skills/shared/supabase/worker-client-helpers.md](../../.agents/skills/shared/supabase/worker-client-helpers.md).
