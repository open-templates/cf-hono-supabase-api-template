---
type: Feature
title: Frontend pairing
description: Contract with react-supabase-auth-template for health and profile calls.
tags: [pairing, frontend]
timestamp: 2026-07-15T00:00:00Z
---

# Pairing

| Frontend call | Backend route |
|---------------|---------------|
| Header health indicator | `GET /health` (no auth) |
| Home profile card | `GET /me` (Bearer from `localStorage['x-auth-token']`) |

Base URL in React app: `VITE_API_BASE_URL` (default `http://localhost:8787`).

Frontend OKF spec: [react-supabase-auth-template/index.md](https://github.com/open-templates/react-supabase-auth-template/blob/main/index.md).
