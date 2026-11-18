Might Work Group Project

**P2 Submission:** [Project Requirements](docs/requirements/P2.docx)

**P3 Submission:** [Project Plan](docs/plan/P3.docx)

**Alternative Formats Available:**
- [P2 Markdown Version](docs/requirements/P2.md)
- [P2 Detailed Requirements](docs/requirements/README.md)
- [P3 Markdown Version](docs/plan/P3.md)
- [P3 Detailed Requirements](docs/plan/P3.md)

**Project Overview:**
Rebaz is a collaborative travel planning and itinerary organizer web app.

*Key Features:*
- Trip planning with transport/lodging
- Real-time member collaboration
- Conflict detection
- Expense tracking
- Offline export capability

## Development

The app is a pnpm + Turborepo monorepo with Next.js and shadcn/ui (Radix base, RTL-ready).

- `apps/web` is the Next.js app
- `packages/ui` holds the shared shadcn/ui components, styles and utilities (`@workspace/ui`)
- `packages/eslint-config` and `packages/typescript-config` hold the shared configs

```bash
pnpm install      # install dependencies (Node >= 20.9)
pnpm dev          # start the dev server
pnpm build        # production build
pnpm lint         # lint all packages
pnpm typecheck    # type-check all packages
```

To add a shadcn component (it goes into `packages/ui/src/components`):

```bash
pnpm dlx shadcn@latest add <component> -c apps/web
```

Then import it with `import { Button } from "@workspace/ui/components/button"`.
