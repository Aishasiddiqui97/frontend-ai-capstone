# FlyRank FE-01 — Frontend Assignment

A Next.js frontend application built for the FlyRank engineering assessment, demonstrating modern React patterns, component architecture, and API integration.

## Status

<!-- TODO: update once deployed -->
Proof-of-concept / In development.

## Prerequisites

- **Node.js** >= 18.17
- **pnpm** >= 8 (install via `npm install -g pnpm`)

## Tech Stack

| Category          | Choice                    |
| ----------------- | ------------------------- |
| Framework         | Next.js 14+ (App Router)  |
| Language          | TypeScript (strict mode)  |
| Styling           | Tailwind CSS (utility-first) |
| State Management  | React Context, local state |
| HTTP Client       | Fetch API (typed wrappers) |
| Linting / Format  | ESLint (flat config), Prettier |

## Getting Started

```bash
pnpm install
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## Scripts

| Command            | Description                |
| ------------------ | -------------------------- |
| `pnpm dev`         | Start development server   |
| `pnpm build`       | Production build           |
| `pnpm start`       | Start production server    |
| `pnpm lint`        | Run ESLint                 |
| `pnpm typecheck`   | Run TypeScript checks      |
| `pnpm format`      | Format with Prettier       |

## Project Structure

```
src/
├── app/          # App Router pages & layouts (Route Groups, layouts)
├── components/   # Reusable UI components (PascalCase, named exports)
├── hooks/        # Custom React hooks
├── lib/          # Utilities, API clients, helpers
├── types/        # Shared TypeScript interfaces & types
└── styles/       # Global CSS (minimal, Tailwind-driven)
```

## Features

Planned areas of focus:

- [ ] Responsive page layout with App Router
- [ ] Type-safe API integration layer
- [ ] Component composition & reusability
- [ ] Accessible UI (keyboard nav, ARIA)
- [ ] Error & loading states

## Assignment Goals

- Demonstrate clean component architecture and separation of concerns
- Follow TypeScript strict mode conventions
- Use Tailwind for all styling (no CSS modules)
- Keep state management lightweight and intentional
- Handle API errors with typed error boundaries

## License

MIT — see [LICENSE](LICENSE) for details.
