# New HuQAS Website

This is an experiment to see if I can build a new HuQAS website using Astro and
Strapi.

## Tech Stack

- Astro
- Tailwind CSS
- Strapi
- PostgreSQL

## Getting Started

1. Clone the repository
2. Install dependencies
3. Run the development server

## Project Layout

This repository uses a monorepo setup to cleanly separate the Astro frontend and
the Strapi headless CMS.

```text
new-huqas-website/
├── .gitignore
├── README.md
├── package.json               # Root package.json (defines workspaces)
├── docker-compose.yml         # Local PostgreSQL for Strapi
│
├── frontend/                  # 🚀 Astro Application (The Website)
│   ├── src/
│   │   ├── components/        # Reusable UI/Astro components
│   │   ├── layouts/           # Shared page wrappers
│   │   ├── pages/             # Astro's file-based routing
│   │   ├── lib/               # Utility scripts (Strapi API fetch wrappers)
│   │   ├── types/             # TypeScript types
│   │   ├── styles/            # Global Tailwind CSS file
│   │   └── env.d.ts           # Astro environment types
│   ├── public/                # Static assets
│   ├── astro.config.mjs       # Astro integrations
│   ├── tailwind.config.cjs    # Tailwind configuration
│   ├── .env                   # Environment variables (STRAPI_URL)
│   └── package.json           # Astro dependencies
│
└── backend/                   # 🏗️ Strapi Application (The CMS)
    ├── config/                # Strapi settings
    ├── database/              # Migrations and seeds
    ├── public/                # Strapi uploads folder
    ├── src/
    │   ├── api/               # Content Types
    │   ├── admin/             # Admin panel customizations
    │   ├── components/        # Strapi repeatable components
    │   └── index.ts/js        # Lifecycle hooks
    ├── .env                   # DB credentials
    └── package.json           # Strapi dependencies
```
