# CalFinal

A booking and scheduling application built with Next.js, Prisma, PostgreSQL, and Tailwind CSS. This project supports event type management, availability setup, booking workflows, and integrations with Vercel deployments.

## Key Features

- Next.js 16 application with app router and server-side API routes
- Prisma ORM with PostgreSQL database support
- Event type creation, booking questions, and availability management
- Responsive dashboard experience with reusable UI components
- Built with `pnpm` and modern TypeScript tooling

## Repository Structure

- `app/` - Next.js pages, layouts, and API routes
- `components/` - UI and dashboard components
- `lib/` - shared utilities, Prisma client, and booking helpers
- `prisma/` - Prisma schema and migrations
- `public/` - static assets
- `styles/` - global styles

## Getting Started

### Prerequisites

- Node.js 20+ or compatible runtime
- `pnpm` package manager
- PostgreSQL database or Railway database

### Local setup

1. Install dependencies:

```bash
pnpm install
```

2. Copy environment variables:

```bash
cp .env.example .env
```

3. Update `.env` with your actual database connection string:

```env
DATABASE_URL="postgresql://USER:PASSWORD@HOST:PORT/DATABASE"
```

4. Approve any required pnpm build scripts (if prompted):

```bash
pnpm approve-builds
```

5. Generate Prisma client:

```bash
npx prisma generate
```

6. Push the database schema:

```bash
npx prisma db push
```

7. Run the development server:

```bash
pnpm dev
```

Open `http://localhost:3000` in your browser.

## Scripts

- `pnpm dev` - Run the development server
- `pnpm build` - Create a production build
- `pnpm start` - Start the production server
- `pnpm lint` - Run ESLint

## Deployment

This project is configured for deployment on Vercel.

- Ensure `DATABASE_URL` is configured in Vercel project environment variables.
- If using Railway or another managed PostgreSQL provider, use the provider's connection string.
- Build command: `pnpm build`
- Output directory: handled by Next.js

## Notes

- The project uses Prisma v7 and requires a PostgreSQL adapter (`@prisma/adapter-pg`).
- Keep `.env` local and do not commit secrets.
- Use `.env.example` as a template for required environment variables.

## License

This repository is provided as-is. Update the license section if you add licensing terms.
