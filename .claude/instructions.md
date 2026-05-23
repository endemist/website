# Endemist Website

Next.js marketing site for Endemist — drug discovery orchestration software.

## Project Structure

| Directory | Purpose |
|-----------|---------|
| `/app/` | Pages and layouts (Next.js App Router) |
| `/components/` | Shared UI components |
| `/components/ui/` | shadcn/ui primitives |
| `/lib/` | Utility functions (`cn`, etc.) |
| `/public/` | Static assets (images, SVGs) |

## Stack

| Layer | Choice |
|-------|--------|
| Framework | Next.js (App Router) |
| Styling | Tailwind CSS v4 |
| Components | shadcn/ui + Base UI |
| Icons | Lucide React |
| Language | TypeScript |

## Requirements

- **Node**: Must be installed. Stop and prompt user if missing.
- **Package Manager**: Use `pnpm` only. Never use `npm`, `yarn`, or `bun`.

## Commands

| Command | Purpose |
|---------|---------|
| `pnpm dev` | Start dev server |
| `pnpm build` | Production build |
| `pnpm lint` | ESLint check |
| `pnpm dlx shadcn@latest add <component>` | Add shadcn component |

## Brand

- **Primary font**: Apfel Grotezk (display) — not yet installed, use Inter as fallback
- **Body font**: Inter (loaded via `next/font/google` in `app/layout.tsx`)
- **Colors**: defined as CSS variables in `app/globals.css` — always use Tailwind utilities (`bg-aqua`, `text-navy`, etc.), never hardcode hex values

## Key Conventions

- All colors come from the brand palette in `globals.css` — do not use arbitrary hex values
- Images go in `/public/`, reference as `/filename.ext`
- Use `next/image` for all `<img>` tags
- Use `next/link` for internal navigation
- Components are Server Components by default — add `'use client'` only when needed
