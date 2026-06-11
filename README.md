# Zerodiet 🏋️ A Personal Training Platform — Client Intake & Plan Management

A two-sided platform for a personal trainer: clients sign up, select a plan, and complete a structured onboarding; the trainer manages all clients, delivers diet and training plans, and tracks earnings — from a single dashboard.

**Live:** https://fitness-website-snowy.vercel.app

---

## Code Architecture

- frontend (client panel) → https://github.com/Saikat-github/zerodiet-1-frontend
- admin/trainer panel → https://github.com/Saikat-github/zerodiet-1-admin

---

## Features

### Client Side
- **Auth** — sign up via email OTP or Google OAuth
- **Plan selection** — choose a training plan during onboarding
- **Structured onboarding form** — goals, weekly schedule, dietary preferences, fitness history
- **Plan delivery** — receive assigned diet and training plans from the trainer directly in dashboard

### Trainer / Admin Panel
- **Client management** — view all clients, their onboarding data, and assigned plans
- **Plan assignment** — send customized diet and training plans per client
- **Progress tracking** — monitor client progress over time
- **Earnings dashboard** — track revenue by plan and period

---

## Tech Stack

| Layer | Tech |
|---|---|
| Frontend | React, TailwindCSS, React Hook Form |
| State Management | Redux |
| Backend & Auth | Appwrite (BaaS) |
| Auth Methods | Email OTP, Google OAuth |

---

## Key Implementation Highlights

- **Appwrite BaaS** — used Appwrite for auth, database, and file storage; eliminated the need for a custom backend while maintaining full control over data structure and access rules
- **Google OAuth + Email OTP** — two auth flows handled through Appwrite's built-in providers; no custom auth logic needed on the frontend
- **Role-based access** — trainer panel and client panel are completely separate; Appwrite's permission model enforces which user can read or write which documents
- **Onboarding gate** — clients cannot access the main dashboard until onboarding form is fully completed; enforced client-side via Redux state check on protected routes

---

## Screenshots


<img width="1340" height="589" alt="zerodiet-pic-1" src="https://github.com/user-attachments/assets/0b21a6e8-465a-4ce0-a599-8ae4c7aff7ef" />
<img width="1342" height="584" alt="zerodiet-pic-2" src="https://github.com/user-attachments/assets/c50054f1-8195-494f-a966-b47fc0eff90d" />
<img width="1343" height="595" alt="zerodiet-pic-3" src="https://github.com/user-attachments/assets/6bb2a7a3-aa94-4f13-aa41-e0ed5a5ebfbf" />
<img width="1345" height="593" alt="zerodiet-pic-4" src="https://github.com/user-attachments/assets/b2f6f094-91bc-40d1-8fd0-2e4163f6dd4c" />






