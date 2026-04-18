# WSU Gradschool Orgchart Editor

Org chart **builder and exporter** for WSU Graduate School. This is a **Next.js** app, split out from the former WSU Graduate School tools monorepo as its own repository.

**Repository:** [github.com/gcrouch-wsu/wsu-gradschool-orgchart-editor](https://github.com/gcrouch-wsu/wsu-gradschool-orgchart-editor)

## What it does

- Visual org chart editing with export/import flows.
- API routes under `/app/api/orgchart/` for runtime assets, samples, and downloads.

## Requirements

- **Node.js** 18+ (20+ recommended)
- **npm**

## Quick start

1. Clone this repository:

```bash
git clone https://github.com/gcrouch-wsu/wsu-gradschool-orgchart-editor.git
cd wsu-gradschool-orgchart-editor
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
wsu-gradschool-orgchart-editor/
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

### Current production

If this app is still deployed from an older Vercel project, the hostname may predate the current repository name.

### This repository

Deploy from **this** repo with the **repository root** as the app root. Target: **Railway** or any Node host that runs `npm run build` and `npm run start` with `PORT` set.

## Related WSU Graduate School tools

This repo is maintained independently from the other Graduate School tools.

## Environment variables

None required for typical operation. Document any future variables here and use `.env.local` locally (never commit secrets).
