---
okf_version: "0.1"
---

# cf-hono-supabase-api-template

OKF knowledge bundle for the out-of-the-box worker API surface.

## Documentation

* [README.md](README.md) - quick start and environment
* [INSTRUCTIONS.md](INSTRUCTIONS.md) - maintainer and adopter guide

## Features

* [01 — Purpose](specs/features/01-purpose.md) - worker goals and pairing
* [02 — Health endpoint](specs/features/02-health-endpoint.md) - `GET /health`
* [03 — Me endpoint](specs/features/03-me-endpoint.md) - `GET /me` with JWT
* [04 — Middleware](specs/features/04-middleware.md) - logger, CORS, auth, errors
* [05 — Supabase integration](specs/features/05-supabase-integration.md) - client helpers
* [06 — Frontend pairing](specs/features/06-frontend-pairing.md) - react-supabase-auth-template contract
* [07 — Extension guidelines](specs/features/07-extension-guidelines.md) - new routes and docs

## Skills

* [.agents/skills/index.md](.agents/skills/index.md) — OKF modules + shared concepts
* [.agents/skills/README.md](.agents/skills/README.md) — Cursor `SKILL.md` catalog
* [.agents/skills/shared/](.agents/skills/shared/) — synced auth and Supabase skills

## History

* [specs/log.md](specs/log.md)
