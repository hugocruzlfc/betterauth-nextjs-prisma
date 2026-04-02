Set up Prisma
Next, you'll add Prisma to your project to manage your database.

-Install Prisma and dependencies
Install the necessary Prisma packages. The dependencies differ slightly depending on whether you use Prisma Postgres with Accelerate or another database.

npm
pnpm
yarn
bun

pnpm add prisma tsx @types/pg --save-dev
npm
pnpm
yarn
bun

pnpm add @prisma/client @prisma/adapter-pg dotenv pg
If you are using a different database provider (MySQL, SQL Server, SQLite), install the corresponding driver adapter package instead of @prisma/adapter-pg. For more information, see Database drivers.

Once installed, initialize Prisma in your project:

npm
pnpm
yarn
bun

pnpm dlx prisma init --output ../src/generated/prisma

Generate the Prisma client
Run the following command to create the database tables and generate the Prisma Client:

npm
pnpm
yarn
bun

pnpm dlx prisma generate

Add Better Auth models to your schema
Better Auth provides a CLI command to automatically add the necessary authentication models (User, Session, Account, and Verification) to your schema.prisma file.

Run the following command:

npm
pnpm
yarn
bun

pnpm dlx auth generate

Migrate the database
With the new models in your schema, you need to update your database. Run a migration to create the corresponding tables:

npm
pnpm
yarn
bun

pnpm dlx prisma migrate dev --name add-auth-models
npm
pnpm
yarn
bun

pnpm dlx prisma generate
