# MARK PRO — Business Management API (starter)
Includes Express REST API + PostgreSQL schema + JWT authentication + product, sales, account and dashboard endpoints.

## Requirements
- Node.js 18+
- PostgreSQL 14+

## Setup
1. Extract this ZIP.
2. Run `npm install`.
3. Create a PostgreSQL database named `mark_pro`.
4. Copy `.env.example` to `.env` and update `DATABASE_URL` and `JWT_SECRET`.
5. Apply schema: `psql -d mark_pro -f database/schema.sql`
6. Run `npm start`.

API base: `http://localhost:4000`
Health: `GET /api/health`

## Auth
- `POST /api/auth/register` JSON: `{ "name":"Admin", "email":"admin@example.com", "password":"change-me-123", "businessName":"My Business" }`
- `POST /api/auth/login` JSON: `{ "email":"admin@example.com", "password":"change-me-123" }`
Use returned token in `Authorization: Bearer TOKEN`.

## Protected endpoints
- `GET /api/me`
- `GET /api/dashboard`
- `GET/POST /api/products`
- `GET/POST /api/sales`
- `GET/POST /api/accounts`

## Notes
This is a development starter, not yet production hardened. Add validation, rate limiting, audit logs, migrations, HTTPS, backups, accounting double-entry, stock movement transactions, and tests before real business use. Never deploy with the example JWT secret.
