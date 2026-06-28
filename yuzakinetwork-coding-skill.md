---
name: @YuzakiNetwork-coding-skill
description: "GitHub profile skill from @YuzakiNetwork. Use it when the task would benefit from mimicking this developer's repo choices, coding style, and implementation techniques."
---

## What they tend to build

- Small-to-medium web apps with a clear end-user surface, not library-style code.
- The strongest signal is an anime portal: content browsing, search, schedules, detail pages, comments, news, and an admin area.
- They seem to favor practical “feature bundles”:
  - public content pages
  - API endpoints
  - authentication/admin CRUD
  - database-backed persistence
- Most likely output is a full-stack Next.js app rather than a heavily separated frontend/backend monorepo.

## Coding patterns to mirror

- Use Next.js App Router conventions and keep page structure inside `src/app`.
- Put shared utilities in `lib/` and keep app pages/components separate from data-access helpers.
- Prefer TypeScript with strictness enabled; write code that type-checks cleanly instead of leaning on loose JS.
- Expect path aliases like `@/*` for cleaner imports.
- Favor small, direct helpers for:
  - DB access
  - auth/session checks
  - API calls to external services
- Keep API routes explicit and feature-based, especially for CRUD flows (`/api/anime`, `/api/news`, `/api/admin`, `/api/comments`).
- Use server-side logic where it makes sense: authentication, SQLite access, uploads, and session handling.
- Name things plainly and functionally; the repo signals “clear and practical” over clever abstraction.
- Since the profile is sparse and beginner-leaning, avoid over-engineering. Mirror the likely simple, readable implementation style.

## Product and UI taste

- UI appears geared toward a polished consumer portal:
  - hero sections
  - gradient accents
  - card-based content lists
  - responsive layouts
  - obvious CTAs
- Content is presented in a structured, browseable way: top items, seasonal items, schedules, detail pages, and pagination for news.
- The README suggests a preference for “feature completeness” and visible usefulness over minimalism.
- Copy is likely Indonesian-first, with practical labels and user-facing explanations.
- Admin UI should feel lightweight and usable, not enterprise-heavy.

## Tech stack clues

- Next.js 15.x with App Router
- React 19
- TypeScript
- Tailwind CSS v4
- ESLint 9
- Axios for HTTP requests
- bcryptjs for password hashing
- multer for file uploads
- sqlite3 for local persistence
- Jikan API / MyAnimeList data integration
- Session/cookie-based auth patterns
- `next dev --turbopack` indicates modern Next dev workflow

## When to inspect repos first

- Inspect first when you need to know actual folder boundaries, because the README shows a larger structure than the visible repo tree confirms.
- Inspect first before adding features that depend on:
  - auth/session flow
  - DB schema shape
  - upload handling
  - API route naming
  - whether code lives under `src/`, `app/`, or both
- Inspect first if you’re matching style closely: the public evidence is thin, and `project-01` / `database` don’t add much implementation detail.
- Inspect first when deciding whether to build with server actions, route handlers, or older API-route patterns; this repo’s docs suggest API routes, but the actual code should confirm it.

## Repo Map

- [YuzakiNetwork/AnimeHub](https://github.com/YuzakiNetwork/AnimeHub) (1 stars, TypeScript)
- [YuzakiNetwork/project-01](https://github.com/YuzakiNetwork/project-01) (0 stars)
- [YuzakiNetwork/database](https://github.com/YuzakiNetwork/database) (0 stars)

## How To Use This Skill

- Reach for this skill when the user asks for Haruka Fuyune's style, when the repo stack matches this person's ecosystem, or when studying their real code would reduce made-up output.
- Pick one or more relevant repositories from the list above based on the current task.
- Clone the most relevant repository or repositories into `/tmp` for temporary inspection.
- Study the implementation details, naming patterns, architecture, UI taste, and tooling choices there.
- Return to the main task and apply the useful patterns you observed instead of copying blindly.
- Treat the upstream repositories as reference material for style and technique, then adapt them to the current codebase responsibly.
