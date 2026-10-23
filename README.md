# test.project

Node.js web app built with **Next.js** and **TypeScript**. Uses the App Router, server-first data fetching, and typed APIs.

## Tech stack

- Node.js
- TypeScript (strict)
- Next.js (App Router)
- React
- npm

## Getting started

**Requirements:** Node.js 20+ and npm.

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the Next.js dev server |
| `npm run build` | Create a production build |
| `npm run start` | Run the production server |
| `npm run lint` | Run ESLint |

## Project structure

```
.
├── app/            # App Router pages, layouts, and API routes
├── components/     # Reusable UI
├── lib/            # Shared utilities and helpers
├── types/          # Shared TypeScript types
├── public/         # Static assets
├── cursor.md       # Project conventions for humans and AI
└── README.md
```

- Route UI lives in `app/`.
- Reusable UI lives in `components/`.
- Business logic lives in `lib/`.

## Conventions

- TypeScript only (`.ts` / `.tsx`). Avoid `any`.
- Functional React components. Prefer Server Components; add `"use client"` only when needed.
- Kebab-case for files and folders. PascalCase for React components.
- Keep secrets in environment variables. Do not commit secret `.env` files.

## Environment

Copy environment variables into a local `.env.local` file. Do not commit secrets.

## More detail

See [cursor.md](cursor.md) for coding conventions, common tasks, and notes for AI.
