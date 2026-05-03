# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Artifacts

### VoiceMap California (`artifacts/voicemap`) — Preview at `/`
A polished civic-tech web app: "VoiceMap California: Animal Welfare Evidence Hub."
- **Purpose**: Statewide California public-interest tool for documenting animal welfare concerns, identifying patterns, and generating responsible reports for agencies, officials, and media.
- **Tech**: React + Vite + Tailwind CSS + framer-motion + react-hook-form + zod + wouter + localStorage
- **Color Palette**: #F8E2AA (golden), #FAEDCD (cream), #FDFAE0 (ivory), #CAE7FF (sky blue), #8FBAE1 (steel blue)
- **Characters**: Kurzgesagt-style animated SVG cats and dogs with CSS keyframe animations
- **Pages**: Landing, Submit Concern, Dashboard, Report Packet Generator, Escalation Center, Resources, Responsible Reporting
- **Data**: localStorage only (no backend) — ready for future Supabase integration

### API Server (`artifacts/api-server`) — Preview at `/api`
Express 5 REST API server.

### Canvas (`artifacts/mockup-sandbox`) — Preview at `/__mockup`
Design mockup sandbox.

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
