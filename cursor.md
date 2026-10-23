# Cursor

## Project overview

Node.js web application built with Next.js and TypeScript. Use the App Router, server-first data fetching, and typed APIs. Keep features small, typed, and easy to extend.

## Tech stack

- **Runtime:** Node.js
- **Language:** TypeScript (strict)
- **Framework:** Next.js (App Router)
- **UI:** React
- **Styling:** CSS Modules or Tailwind CSS (pick one and stay consistent)
- **Package manager:** npm
- **Lint / format:** ESLint + Prettier

## Project structure

```
.
├── app/                  # Next.js App Router (pages, layouts, API routes)
│   ├── layout.tsx
│   ├── page.tsx
│   └── api/              # Route handlers
├── components/           # Reusable UI components
├── lib/                  # Shared utilities, clients, helpers
├── types/                # Shared TypeScript types
├── public/               # Static assets
├── cursor.md             # Project guidance for humans and AI
├── package.json
├── tsconfig.json
└── next.config.ts
```

- Put route-specific UI in `app/`.
- Put reusable UI in `components/`.
- Put business logic and helpers in `lib/`, not inside components.
- Prefer colocated files (`page.tsx`, `layout.tsx`, `loading.tsx`, `error.tsx`) for each route.

## Coding conventions

- Use TypeScript everywhere. Avoid `any`. Prefer explicit return types on exported functions.
- Use functional React components and hooks.
- Prefer Server Components by default. Add `"use client"` only when the component needs browser APIs, state, or event handlers.
- Name files and folders with kebab-case. Name React components with PascalCase.
- Keep server secrets in environment variables. Never commit `.env*` files with secrets.
- Handle errors at route or API boundaries. Do not swallow errors with empty `catch` blocks.
- Keep functions small and focused. One component, one clear responsibility.

## Common tasks

```bash
npm install
npm run dev
npm run build
npm run start
npm run lint
```

- Local development: `npm run dev`
- Production build: `npm run build` then `npm run start`
- Add a page: create `app/<route>/page.tsx`
- Add an API route: create `app/api/<name>/route.ts`
- Add a shared component: create `components/<Name>.tsx`

## Notes for AI

- Follow this file before inventing a different stack or folder layout.
- Do not add libraries unless they are required for the task.
- Match existing patterns. If the project is empty, follow the structure above.
- Prefer Next.js App Router APIs over Pages Router.
- Keep changes scoped to the requested task. Do not refactor unrelated files.
- After UI changes, verify the relevant routes still work.
- When creating files, use TypeScript (`.ts` / `.tsx`), not JavaScript.
