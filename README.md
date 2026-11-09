# Scarlet Oath

Coming-soon landing site for Scarlet Oath (scarletoath.be).

## Stack

React 19, TypeScript 7, Vite 8, Tailwind CSS v4, Biome. Deployed to GitHub Pages.

No memoization (`memo`/`useMemo`/`useCallback`) — intentional: the render tree is small and static, so referential-equality optimizations add noise without measurable benefit.

## Commands

| Command                | Description                          |
| ---------------------- | ------------------------------------ |
| `npm run dev`          | Start the local dev server           |
| `npm run build`        | Build the production bundle          |
| `npm run preview`      | Preview the production build locally |
| `npm run lint`         | Run Biome linting                    |
| `npm run lint:fix`     | Run Biome linting with safe fixes    |
| `npm run format`       | Format files with Biome              |
| `npm run format:check` | Check formatting with Biome          |
| `npm run typecheck`    | Run the TypeScript compiler checks   |
| `npm test`             | Run the test suite                   |

## Deployment

GitHub Pages via `.github/workflows/deploy.yml` (manually triggered with workflow_dispatch). CI (lint, typecheck, test, build) runs on pushes to `core` and on pull requests via `.github/workflows/ci.yml`.
