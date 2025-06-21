# Welth — AI-Powered Financial Management System

## 🎯 Core Objective  
Welth helps users **track, analyze, and optimize** their finances through AI-driven insights, spending forecasts, and budgeting assistance.

## 🛠 Tech Stack  
- **Frontend**: React 19 + Next.js (RSC & SSR for fast and dynamic UI)  
- **Database & Auth**: Supabase (PostgreSQL) with Prisma ORM  
- **Background Jobs**: Inngest for periodic sync, report generation, AI tasks  
- **Security & Edge**: Arcjet for API protection (rate limiting, bot filtering)  
- **AI Engine**: Generative AI via OpenAI (or equivalent) for personalized reports  

## ⚙️ Key Features  
1. 🔍 **Expense Tracking**: Category-based transaction logging  
2. 📊 **Budgeting**: Alerts, predictions, and trends analysis  
3. 🤖 **AI Insights**: Auto-generated tips like “reduce dining out”  
4. 📅 **Scheduled Reports**: Weekly/monthly email summaries via Inngest  
5. 🔐 **Secure API Endpoints**: Protected with Arcjet middleware  

## 🏗 Architecture Diagram  
(Following section offers diagram & explanation)

## 🚀 Getting Started  
1. Clone repo  
2. `npm install`  
3. Set `.env` variables: SUPABASE_URL, NEXT_PUBLIC_SUPABASE_ANON_KEY, DATABASE_URL, INNGEST_TOKEN, ARCJET_SECRET  
4. `npx prisma migrate dev` & `npx prisma generate`  
5. Run background jobs: Inngest worker  
6. `npm run dev` (Vercel Tutorial ready in `/vercel.json`)

## ✅ Production Setup  
Deployed on Vercel; uses Vercel Edge (RSC) + Supabase Edge Functions + Inngest cloud for scheduling.  
Arcjet edge middleware protects API routes.

This is a [Next.js](https://nextjs.org) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.js`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/app/building-your-application/optimizing/fonts) to automatically optimize and load [Geist](https://vercel.com/font), a new font family for Vercel.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
