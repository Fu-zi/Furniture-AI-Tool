# AI Sofa Matching Demo

An open-source demo web app for uploading a living-room photo, selecting a sofa product, and submitting an AI image-editing task through a configurable backend provider.

This repository is sanitized for public release:

- Real product photos were replaced with generated placeholder SVGs.
- Real product catalog data was replaced with demo sofa data.
- API keys, local databases, uploads, addresses, phone numbers, and private PRD content were removed.
- Provider endpoints are configurable through `backend/.env` or the admin panel.

## Apps

- Customer app: `frontend` (Vite + React)
- Admin app: `admin-frontend` (Vite)
- Backend API: `backend` (Express + SQLite CLI)

## Quick Start

```bash
npm run install:all
cp backend/.env.example backend/.env
npm run start:backend
npm run start:frontend
npm run dev --prefix admin-frontend
```

Default demo accounts are seeded on first backend start:

- Store user: `test / msm2026`
- Admin user: `admin / msmadmin2026`

## Security Notes

Do not commit `backend/.env`, `backend/data/`, uploaded files, provider API keys, or real customer/product assets.
