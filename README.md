# CipherAura MVP Blueprint 🚀

## Overview
CipherAura is a cloud-native, AI-driven language learning platform designed for web and mobile users.  
This document outlines the MVP roadmap, tech stack, and deployment plan.

---

## System Architecture
- **Client Layer**: React SPA, React Native (future)
- **API Layer**: Node.js/Express or Laravel
- **ML Microservice**: FastAPI (Python), Hugging Face models
- **Data Layer**: PostgreSQL, Redis
- **DevOps**: Vercel, Netlify, Heroku/Railway, GitHub Actions, Docker

---

## Tech Stack
- **Frontend**: React, Tailwind CSS, React Query
- **Backend**: Node.js + Express / Laravel PHP
- **Database**: PostgreSQL
- **Cache/Queue**: Redis
- **ML/AI**: Hugging Face Transformers, PyTorch, TensorFlow, FastAPI
- **Auth & Payments**: Auth0 / Firebase Auth, Stripe
- **Analytics**: Google Analytics, Plausible
- **CI/CD**: GitHub Actions
- **Deployment**: Vercel, Netlify, Heroku, Railway

---

## Database Schema
- **users**: id, email, password_hash, name, locale, plan
- **lessons**: id, language, level, title, content
- **quizzes**: id, lesson_id, questions
- **progress**: id, user_id, lesson_id, status, score, spaced_rep_queue
- **billing**: id, user_id, stripe_subscription_id, plan, status, amount

---

## API Endpoints
- **Auth**: `/api/register`, `/api/login`, `/api/me`
- **Lessons**: `/api/lessons`, `/api/lessons/:id`
- **Progress**: `/api/progress`
- **Quizzes**: `/api/quizzes/:lesson_id`, `/api/quizzes/:id/submit`
- **Billing**: `/api/subscribe`, `/api/webhook/stripe`

---

## ML Pipeline
- Data collection → preprocessing → training (T5, wav2vec2) → evaluation → deployment
- Endpoints: `/translate`, `/analyze_pronunciation`, `/recommend_review`

---

## Deployment Roadmap (1 Week Sprint)
- **Day 1**: Project scaffolding, CI/CD setup
- **Day 2**: Auth module & APIs
- **Day 3**: Lessons schema & endpoints
- **Day 4**: Quiz engine
- **Day 5**: Progress tracking, spaced repetition
- **Day 6**: Billing integration (Stripe test mode)
- **Day 7**: ML microservice stub, deploy & test

---

## Pricing Plans
- **Free**: Basic lessons (levels 1–2)
- **Monthly**: $9.99/month
- **Quarterly**: $24.99/quarter
- **Yearly**: $79.99/year (discount + test vouchers)
- **Test Packs**: $14.99 one-time (4 mock tests)

---

## UI/UX Flows
- **Onboarding**: Select goals, languages
- **Dashboard**: Progress bar, next lesson, score chart
- **Lesson Player**: Text/audio toggle, pronunciation feedback
- **Quiz Interface**: MCQs, fill-in, audio recording
- **Subscription Page**: Plan comparison, checkout

---

## Open-Source & Free Hosting Tools
- **UI/Frontend**: React, Tailwind, React Query
- **Backend**: Laravel Breeze, Node.js
- **ML**: Hugging Face, SpeechBrain
- **Hosting**: Vercel, Netlify, Heroku, Railway, Render
- **Analytics**: Google Analytics, Plausible, Sentry
- **Utilities**: Redis, PostgreSQL

---

## Getting Started
1. Clone the repo  
2. Setup `.env` with DB, Redis, Stripe keys  
3. Run with Docker Compose:  
   ```bash
   docker-compose up --build
   ```
4. Deploy via GitHub Actions to Vercel/Heroku

---

## License
MIT License © CipherAura


Phase 0: Foundation & Discovery (Diwali 2025 - Dec 2025) - "The
Blueprint Phase"
Objective: Finalize planning, design, and setup before a single line of code is written.
• Competitive Analysis & Feature Benchmarking
• Define Core Technical Principles (Microservices, API-First, Privacy)
• Finalize 'Week to Conversational' Curriculum
• High-Fidelity UI/UX Prototyping with Figma/Adobe XD