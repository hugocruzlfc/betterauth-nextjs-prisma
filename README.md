# 🧬 Prisma + Better Auth Setup

[![Node.js](https://img.shields.io/badge/node-%3E%3D20-brightgreen)]()
[![pnpm](https://img.shields.io/badge/package%20manager-pnpm-orange)]()
[![Prisma](https://img.shields.io/badge/ORM-Prisma-blue)]()
[![Auth](https://img.shields.io/badge/Auth-BetterAuth-purple)]()

[Check out the full documentation for Better Auth](https://www.prisma.io/docs/guides/authentication/better-auth/nextjs)

## Dev Dependencies

```bash
pnpm add prisma tsx @types/pg --save-dev
pnpm add @prisma/client @prisma/adapter-pg dotenv pg
```

## Initialize Prisma

```bash
pnpm dlx prisma init --output ../src/generated/prisma
```

## Generate the Prisma client

```bash
pnpm dlx prisma generate
```

## Add Better Auth models to your schema

```bash
pnpm dlx auth generate
```

## Migrate the database

```bash
pnpm dlx prisma migrate dev --name add-auth-models
pnpm dlx prisma generate
```
