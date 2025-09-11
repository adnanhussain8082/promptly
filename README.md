# 💡 Promptly

Promptly is an AI-powered web app that lets you generate simple websites from natural language prompts. Enter a description—Promptly creates a functional, ready-to-edit Next.js app for you in seconds.

---

## 🧰 Tech Stack

- **Framework**: Next.js 15 (App Router)
- **Frontend**: React, Tailwind CSS
- **UI Components**: Radix UI
- **Type Safety**: TypeScript
- **Authentication**: Clerk
- **Billing**: Clerk Billing
- **AI Generation**: Gemini API
- **Background Jobs**: Inngest
- **Sandboxed Code Execution**: E2B
- **Backend**: Next.js API Routes
- **Database**: PostgreSQL via Prisma ORM

---

## ⚙️ Features

- 🔐 User Authentication (via Clerk)
- 🤖 AI Website Generation from natural language prompts (via Gemini API)
- 💡 Suggested Prompts for instant inspiration
- 🖼️ Example Gallery showcasing real generated sites
- 👀 Live Preview & Code Viewer for generated sites
- 💳 Billing & Plan Management (via Clerk Billing)
- ⚡ Background Job Processing (via Inngest)
- 🛡️ Sandboxed Code Execution (via E2B)

---

## 🚀 Getting Started

1. **Clone the repository:**

```bash
git clone https://github.com/adnanhussain8082/promptly.git
cd promptly
```

2. **Install dependencies:**

```bash
npm install
```

3. **Set up environment variables:**
   Create a `.env` file using `.env.example` and fill in the required values (Clerk keys, database URL, etc).

4. **Run the dev server:**

```bash
npm run dev
```

---

## 📁 Project Structure

```
/
├── prisma/                # Prisma database schema and migrations
├── public/                # Static assets (images, icons, etc.)
├── sandbox-templates/     # Code templates for E2B sandboxes
├── src/
│   ├── app/               # Next.js App Router (routes, pages, layouts, API)
│   │   ├── (home)/        # Main site pages (e.g. pricing, sign-in)
│   │   ├── api/           # API route handlers (incl. inngest, trpc)
│   │   ├── gallery/       # Gallery page routes
│   │   └── projects/      # Project-specific routes
│   ├── components/        # Reusable React UI components
│   │   └── ui/            # UI primitives (buttons, inputs, etc.)
│   ├── generated/         # Auto-generated code (e.g. Prisma types)
│   ├── hooks/             # Custom React hooks
│   ├── inngest/           # Inngest event/workflow handlers
│   ├── lib/               # Utilities and helper functions
│   ├── modules/           # Feature modules (home, messages, projects, usage)
│   └── trpc/              # tRPC routers and API structure
├── .env.example           # Example environment variables
├── next.config.js         # Next.js config
├── package.json           # Project metadata and dependencies
├── README.md              # This file
└── tsconfig.json          # TypeScript config
```

---

## 🔒 Environment Variables

Create a `.env` file in the root directory and include:

```
DATABASE_URL=...
NEXT_PUBLIC_APP_URL=...

# gemini
GEMINI_API_KEY=..

# e2b
E2B_API_KEY=...

# clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=...
CLERK_SECRET_KEY=...
NEXT_PUBLIC_CLERK_SIGN_IN_URL="/sign-in"
NEXT_PUBLIC_CLERK_SIGN_IN_FALLBACK_REDIRECT_URL="/"
NEXT_PUBLIC_CLERK_SIGN_UP_FALLBACK_REDIRECT_URL="/"
NEXT_PUBLIC_CLERK_SIGN_UP_URL="/sign-up"
```

---

## 📝 License

MIT License. Feel free to use, modify, or contribute!

---
**Note:** Do not commit your `.env` file to GitHub. It is already included in `.gitignore` for security.
