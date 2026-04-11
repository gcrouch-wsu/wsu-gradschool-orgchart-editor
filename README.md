# WSU Org Chart Editor

Org chart **builder and exporter** for WSU Graduate School. This is a **Next.js** app, split out from the former [WSU Graduate School Tools](https://github.com/gcrouch-wsu/WSU-Mail-Editor) monorepo as its own repository.

**Repository:** [github.com/gcrouch-wsu/WP-org-chart-editor](https://github.com/gcrouch-wsu/WP-org-chart-editor)

## What it does

- Visual org chart editing with export/import flows.
- API routes under `/app/api/orgchart/` for runtime assets, samples, and downloads.

## Requirements

- **Node.js** 18+ (20+ recommended)
- **npm**

## Quick start

1. Clone this repository:

```bash
git clone https://github.com/gcrouch-wsu/WP-org-chart-editor.git
cd wp-org-chart-editor
```

2. Install dependencies:

```bash
npm install
```

3. Run the development server:

```bash
npm run dev
```

The dev script uses **port 3002** by default. Change the `dev` script in `package.json` if that port is in use.

4. Production build (local smoke test):

```bash
npm run build
npm run start
```

For production hosting (e.g. Railway), use a **`start`** script that runs **`next start`** without a fixed `-p` so the host’s **`PORT`** is used.

## Project structure

```
wp-org-chart-editor/
|-- app/                 # Next.js App Router (pages + API routes)
|-- components/        # React components
|-- public/            # Static assets (e.g. Wordpress.js, admin.js)
|-- package.json
|-- next.config.js
|-- tailwind.config.ts
|-- tsconfig.json
```

## Available scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Development server (`next dev`, port 3002) |
| `npm run build` | Production build |
| `npm run start` | Production server |
| `npm run lint` | ESLint |
| `npm run format` | Prettier write |
| `npm run checkfmt` | Prettier check |

## Deployment

### Current production (legacy Vercel)

Originally deployed from the monorepo with root directory `apps/org-chart-editor`:

**https://wsu-mail-editor-org-chart-editor.vercel.app/**

### This repository

Deploy from **this** repo with the **repository root** as the app root. Target: **Railway** or any Node host that runs `npm run build` and `npm run start` with `PORT` set.

## Related WSU Graduate School tools

Other tools remain in the monorepo ([WSU-Mail-Editor](https://github.com/gcrouch-wsu/WSU-Mail-Editor)) until split out separately. See that repository’s README for links to the platform, newsletter editor, translation tables, validate, and factsheet apps.

## Environment variables

None required for typical operation. Document any future variables here and use `.env.local` locally (never commit secrets).
