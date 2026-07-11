# PoultryOne — Workspace Overview

A pnpm monorepo for **PoultryOne**, a poultry-industry management platform consisting of a marketing website and an API backend.

## Structure

```
artifacts/
  poultryone-website/   # Vite static marketing site ("The Poultry Industry's OS")
  api-server/           # Express + TypeScript API server
  mockup-sandbox/       # Design/canvas component preview server
lib/
  db/                   # Drizzle ORM + PostgreSQL schema
  api-spec/             # Shared API specification
  api-zod/              # Shared Zod validation schemas
  api-client-react/     # React API client hooks
scripts/                # Workspace utility scripts
```

## Stack

- **Package manager:** pnpm (workspace)
- **Frontend:** Vite (static HTML/JS)
- **Backend:** Express 5, TypeScript, Drizzle ORM, PostgreSQL (`pg`)
- **Validation:** Zod

## Running the apps

### Website
```bash
pnpm --filter @workspace/poultryone-website run dev
```

### API Server
Requires environment variables:
- `DATABASE_URL` — PostgreSQL connection string
- `PORT` — port to listen on

```bash
pnpm --filter @workspace/api-server run dev
```

## Installing dependencies
```bash
pnpm install
```

## User preferences
