# Basho-finding
for travel and training code
basho-finding/
├── frontend/                # Next.js app (UI)
│   ├── app/                 # App Router pages
│   │   ├── layout.tsx
│   │   ├── page.tsx         # Home page
│   │   └── login/           
│   │       └── page.tsx     # Login page
│   ├── components/          # Reusable UI components
│   ├── styles/              # Tailwind/global CSS
│   └── package.json
│
├── backend/                 # NestJS API
│   ├── src/
│   │   ├── main.ts          # Entry point
│   │   ├── app.module.ts    # Root module
│   │   └── user/
│   │       ├── user.module.ts
│   │       ├── user.controller.ts
│   │       └── user.service.ts
│   └── package.json
│
├── prisma/                  # Database schema (if using Prisma)
│   └── schema.prisma
│
└── README.md
