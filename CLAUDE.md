# CLAUDE.md — FlyRank FE-01

## Tech Stack

- **Framework:** Next.js 14+ (App Router)
- **Language:** TypeScript (strict mode)
- **Styling:** Tailwind CSS (utility-first)
- **State:** React Context for global state, local state with `useState`/`useReducer`
- **HTTP:** Fetch API (or Ky) with typed wrappers
- **Linting:** ESLint (flat config) + Prettier
- **Package Manager:** pnpm

## Project Structure

```
src/
  app/          # Next.js App Router pages & layouts
  components/   # Reusable UI components
  lib/          # Utilities, helpers, API clients
  hooks/        # Custom React hooks
  types/        # Shared TypeScript types
  styles/       # Global styles (if any)
```

## Coding Conventions

- **Components:** Default exports for pages; named exports for reusable components
- **File naming:** `kebab-case` for files, `PascalCase` for components
- **Types:** Prefer `interface` over `type` for object shapes; use `type` for unions/intersections
- **Async:** `async/await` over raw promises; error boundaries at route level
- **CSS:** Tailwind classes only; no CSS modules or styled-components
- **Imports:** Absolute imports via `@/` alias (e.g. `import { Button } from '@/components/Button'`)
- **Exports:** Named exports for utilities/hooks; default exports for pages

## Commands

```bash
pnpm dev          # Start dev server
pnpm build        # Production build
pnpm lint         # ESLint
pnpm typecheck    # tsc --noEmit
pnpm format       # Prettier
```

## State Management Guidelines

- Prefer **local state** (`useState`) for component-private data
- Use **React Context** for shared authenticated-user / theme / layout state
- Avoid prop drilling beyond 2 levels — extract a component or introduce context
- Side effects belong in `useEffect` or custom hooks, not in components

## API Patterns

- All external API calls go through `src/lib/api.ts` or domain-specific files in `src/lib/`
- Every API function has a typed request and response interface
- Errors are thrown as typed `ApiError` instances, caught in route error boundaries
