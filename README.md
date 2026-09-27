# Acme Dashboard

A Next.js App Router dashboard backed by PostgreSQL. The application includes invoice management, customer reporting, search, and credential-based authentication configuration.

## Getting Started

### Requirements

- Node.js 20 or newer
- A PostgreSQL database

### Install dependencies

```bash
npm install
```

### Configure the database

Create a `.env` file in the project root and add your PostgreSQL connection string:

```env
POSTGRES_URL=postgresql://user:password@host:5432/database?sslmode=require
```

Do not commit `.env` files or database credentials. They are ignored by Git.

### Seed the database

Start the development server and visit [`/seed`](http://localhost:3000/seed) once:

```bash
npm run dev
```

The seed route creates and populates the `users`, `customers`, `invoices`, and `revenue` tables. It uses the sample data in `app/lib/placeholder-data.ts`.

## Routes

- `/` - Landing page
- `/login` - Login page
- `/dashboard` - Dashboard overview and summary cards
- `/dashboard/invoices` - Searchable invoice list
- `/dashboard/invoices/create` - Create an invoice
- `/dashboard/invoices/[id]/edit` - Edit an invoice
- `/dashboard/customers` - Searchable customer list with invoice counts and paid/pending totals
- `/seed` - Database setup and sample-data endpoint

The customer page reads customer data from PostgreSQL through `fetchFilteredCustomers`. It supports searching by customer name or email and displays a responsive table on desktop and mobile layouts.

## Available Commands

```bash
npm run dev       # Start the development server with Turbopack
npm run lint      # Run ESLint
npx tsc --noEmit  # Run TypeScript checks
npm run build     # Create a production build
npm run start     # Start the production server
```

# username and password
Email: user@nextmail.com
Password: 123456

