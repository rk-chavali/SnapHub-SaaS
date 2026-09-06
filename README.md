# SnapHub

A self-hostable documentation workspace, in the spirit of Notion and Confluence.

[![Next.js](https://img.shields.io/badge/Next.js_16-000000?logo=nextdotjs&logoColor=white)](https://nextjs.org/)
[![React](https://img.shields.io/badge/React_19-61DAFB?logo=react&logoColor=black)](https://react.dev/)
[![Drizzle](https://img.shields.io/badge/Drizzle_ORM-C5F74F?logo=drizzle&logoColor=black)](https://orm.drizzle.team/)
[![Postgres](https://img.shields.io/badge/Postgres-4169E1?logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Status](https://img.shields.io/badge/status-early_scaffold-F59E0B)](https://github.com/rk-chavali/SnapHub-SaaS)
[![License: MIT](https://img.shields.io/badge/License-MIT-22C55E.svg)](LICENSE)

> **Status: early scaffold.** The toolchain is chosen and installed. The
> homepage is still the `create-next-app` default and no schema or document
> features exist yet.

## What exists today

| Piece | State |
|-------|-------|
| Next.js 16 App Router + React 19 | Scaffolded |
| Tailwind CSS v4 | Configured |
| Drizzle ORM + `postgres` driver | Installed, no schema written |
| Document model, editor, auth, billing | Not started |

## Intended shape

Postgres for storage with Drizzle for schema and migrations, Supabase for
managed Postgres and auth, and Stripe for billing. The environment variables in
`.env.example` sketch that target:

```
DATABASE_URL=
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SERVICE_ROLE_KEY=
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=
```

None of these are consumed by code yet.

## Run it

```bash
npm install
cp .env.example .env
npm run dev
```

Opens on http://localhost:3000. It runs without any env values set, since
nothing reads them so far.

## License

MIT, see [LICENSE](LICENSE).
