# cf-hono-supabase-api-template

Minimal Cloudflare Worker API built with **Hono** and **Supabase**. Pairs with [react-supabase-auth-template](../react-supabase-auth-template): the React app handles auth (including Google OAuth); this worker validates JWTs and exposes a small set of API endpoints.

## Out-of-the-box features

| Endpoint | Auth | Description |
|----------|------|-------------|
| `GET /health` | Public | Liveness check for frontend online/offline indicator |
| `GET /me` | Bearer JWT | Returns the authenticated Supabase user profile |

See [`specs/FEATURES.md`](specs/FEATURES.md) for detailed behavior, request/response shapes, and extension guidance for AI agents and contributors.

## Stack

- Hono on Cloudflare Workers
- TypeScript
- Supabase Auth (JWT validation + `auth.getUser()`)
- Wrangler for local dev and deploy

## Quick start

```bash
npm install
cp .env.example .dev.vars   # local Wrangler secrets
npm run dev                 # http://localhost:8787
```

Test:

```bash
curl http://localhost:8787/health
curl -H "Authorization: Bearer <supabase-access-token>" http://localhost:8787/me
```

Full setup: [`QUICKSTART.md`](QUICKSTART.md) · Cloudflare deploy: [`CLOUDFLARE_SETUP.md`](CLOUDFLARE_SETUP.md)

## Environment variables

| Variable | Required | Purpose |
|----------|----------|---------|
| `SUPABASE_URL` | Yes | Supabase project URL |
| `SUPABASE_ANON_KEY` | Yes | Anon key (JWT-scoped client for `/me`) |
| `SUPABASE_SERVICE_ROLE_KEY` | Yes | Reserved for future admin operations |
| `ALLOWED_ORIGINS` | No | Comma-separated CORS origins (e.g. `http://localhost:5173`) |
| `ENVIRONMENT` | No | `development` / `staging` / `production` |

Set production secrets with `wrangler secret put` (see `CLOUDFLARE_SETUP.md`).

## Project layout

```
src/
├── index.ts           # App entry, route registration
├── routes/
│   ├── health.ts      # GET /health
│   └── me.ts          # GET /me
├── middleware/        # Auth, CORS, errors
├── lib/supabase.ts    # Supabase client factories
└── utils/             # JWT, auth helpers, responses
```

## Scripts

- `npm run dev` — local worker via Wrangler
- `npm run deploy` — deploy to Cloudflare
- `npm run type-check` — TypeScript check
- `npm run lint` / `npm run format` — code quality

## License

MIT
