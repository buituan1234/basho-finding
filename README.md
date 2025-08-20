# Basho-finding
for travel and training code
basho-finding/
├── README.md
├── .env                   # env chung (ghi chú: lưu keys dev ở từng service nếu cần)
├── docker-compose.yml     # (tuỳ chọn) docker cho DB, redis, v.v.
├── frontend/              # ─────────────────── Next.js + TypeScript (App Router)
│   ├── package.json
│   ├── tsconfig.json
│   ├── next.config.js
│   ├── tailwind.config.js
│   ├── postcss.config.js
│   ├── public/            # assets tĩnh: images, favicon...
│   │   └── ...
│   └── src/
│       ├── app/
│       │   ├── layout.tsx
│       │   ├── page.tsx           # / (home)
│       │   ├── introduction/
│       │   │   └── page.tsx       # /introduction
│       │   ├── login/
│       │   │   ├── page.tsx       # /login
│       │   │   └── loading.tsx
│       │   ├── register/
│       │   │   └── page.tsx       # /register
│       │   ├── search/
│       │   │   └── page.tsx       # /search
│       │   ├── admin/
│       │   │   └── page.tsx       # /admin
│       │   └── (other routes...)
│       ├── components/            # reusable UI components
│       │   ├── Navbar.tsx
│       │   ├── Card.tsx
│       │   └── ...
│       ├── features/              # domain-specific components (e.g., auth, booking)
│       ├── hooks/                 # custom hooks
│       ├── services/              # http clients, api wrappers (call backend)
│       │   └── api.ts
│       ├── styles/                # globals.css (Tailwind entry), modules
│       │   └── globals.css
│       └── types/                 # shared TS types/interfaces
│           └── index.d.ts
│
├── backend/               # ─────────────────── NestJS + TypeScript (API server)
│   ├── package.json
│   ├── tsconfig.json
│   ├── nest-cli.json
│   ├── prisma/              # (nếu dùng Prisma)
│   │   └── schema.prisma
│   └── src/
│       ├── main.ts
│       ├── app.module.ts
│       ├── config/
│       │   └── app.config.ts
│       ├── common/          # guards, pipes, interceptors, filters, utils
│       │   ├── guards/
│       │   ├── pipes/
│       │   └── interceptors/
│       ├── modules/         # domain modules
│       │   ├── auth/
│       │   │   ├── auth.controller.ts
│       │   │   ├── auth.service.ts
│       │   │   ├── dto/
│       │   │   │   └── login.dto.ts
│       │   │   └── auth.module.ts
│       │   ├── users/
│       │   │   ├── users.controller.ts
│       │   │   ├── users.service.ts
│       │   │   └── users.module.ts
│       │   ├── hotels/
│       │   │   ├── hotels.controller.ts
│       │   │   ├── hotels.service.ts
│       │   │   └── hotels.module.ts
│       │   ├── bookings/
│       │   └── ai/           # AI integration (calls to OpenAI/HuggingFace, vector DB)
│       │       ├── ai.controller.ts
│       │       ├── ai.service.ts
│       │       └── ai.module.ts
│       └── database/        # ORM client setup, migrations, seeds
│           └── index.ts
│
└── infra/                 # (tuỳ chọn) scripts infra, k8s, CI, deploy
    ├── ci/
    └── k8s/

