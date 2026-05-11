# 🏋 SOMA — AI Fitness Coach for Beginners

> Personalized workout + diet plans in under 60 seconds. No signup. No backend. Deploys free in 5 minutes.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOURUSERNAME/soma)
![DPDPA 2023 Compliant](https://img.shields.io/badge/DPDPA%202023-Compliant-00C87A?style=flat-square)
![Zero Cost](https://img.shields.io/badge/Hosting%20Cost-₹0-00C87A?style=flat-square)
![Static](https://img.shields.io/badge/Type-Static%20HTML-blue?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)

---

## 🎯 What is SOMA?

SOMA is an AI fitness coaching MVP for beginners aged 18–35. It solves a real problem: **70% of gym beginners quit within 3 months** because they feel overwhelmed and don't know where to start.

**SOMA gives them a personalized 7-day workout + diet plan in under 60 seconds — no account, no gym knowledge required.**

### Core User Flow
```
Landing → 5-question quiz → Consent (DPDPA 2023) → Plan generated → Daily tracker → Streak
```

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| ⚡ 60-second onboarding | 5 inputs → full plan, instantly |
| 🧠 Smart personalization | 48 unique plans across goals × equipment combinations |
| 📅 7-day schedule | Rest days built in, beginner-appropriate exercises |
| 🥗 Indian meal guide | Calorie targets + desi meal examples |
| 🔥 Streak tracker | Daily check-in with gamified streak counter |
| 💾 Persistent state | localStorage saves plan + streak across sessions |
| 🔒 DPDPA 2023 compliant | Explicit consent, purpose limitation, erasure info |
| ⚠️ AI safety guardrails | Medical disclaimer always visible, no harmful advice |
| 📱 Mobile-first | Fully responsive, works on all screen sizes |
| ₹0 to deploy | Pure static HTML — no server, no database needed |

---

## 🚀 Deploy in 5 Minutes

### Option 1 — Vercel (Recommended)

1. Fork this repo
2. Go to [vercel.com](https://vercel.com) → Sign up free with GitHub
3. Click **"Add New Project"** → Import your forked `soma` repo
4. Click **Deploy** — done ✅

Your site will be live at `https://soma-yourusername.vercel.app`

### Option 2 — GitHub Pages

1. Fork this repo
2. Go to repo **Settings → Pages**
3. Source: `Deploy from a branch` → Branch: `main` → Folder: `/ (root)`
4. Save → live in ~60 seconds at `https://yourusername.github.io/soma`

### Option 3 — Netlify

1. Fork this repo
2. Go to [netlify.com](https://netlify.com) → New site from Git
3. Connect GitHub → select `soma` → Deploy
4. Live at `https://soma-xyz.netlify.app`

> **No environment variables, no build step, no npm install required.** It's a single `index.html` file.

---

## 📁 Project Structure

```
soma/
├── index.html      # Entire app — 6 screens, all logic, all styles
├── 404.html        # Redirect fallback for SPA routing
├── vercel.json     # Vercel deployment config + security headers
├── .gitignore
├── LICENSE
└── README.md
```

**Why a single file?**
This is a portfolio MVP. A single `index.html` is:
- Instantly deployable anywhere (drag & drop on Netlify)
- Easy to review in one scroll on GitHub
- Zero build pipeline — no Webpack, no npm, no CI/CD needed
- Showcases that you understand when complexity is and isn't warranted

---

## 🧠 How the Plans Work

SOMA uses a **static plan database** with 48 unique combinations:

```
4 goals × 3 equipment types × 7 days = 48 plan variants
```

| Goals | Equipment |
|-------|-----------|
| Weight loss | None (bodyweight) |
| Muscle building | Dumbbells |
| Endurance | Full gym |
| General fitness | |

Each plan includes:
- Day-by-day workout (exercise, sets, reps)
- Calorie + macro targets calibrated to goal
- Indian meal examples for breakfast/lunch/snack/dinner
- 4 beginner tips tailored to goal type

### Safety Rules Built In
- Minimum 2 rest days per 7-day plan
- Calorie targets: 1800–2400 kcal (no extreme deficits)
- All exercises are beginner-appropriate (no Olympic lifts for beginners)
- Medical disclaimer permanently visible — cannot be dismissed

---

## 🔐 Indian Legal Compliance

### Digital Personal Data Protection Act, 2023 (DPDPA)

| Requirement | How SOMA handles it |
|-------------|---------------------|
| Explicit consent | Required checkbox before plan generation — cannot be pre-checked |
| Purpose limitation | Stated clearly: "Used only to generate your plan" |
| Consent timestamp | Saved to `localStorage` with ISO timestamp |
| Right to erasure | Instructions in consent screen: clear browser data + email |
| Data minimisation | Only 5 inputs collected, nothing else |

### IT Act 2000 Compliance
- Medical disclaimer present on consent screen and plan view
- No harmful, dangerous, or misleading fitness advice
- Content is AI-informed, not AI-hallucinated (static, curated database)

### ISO 42001 (AI Governance) — Basic Alignment
- Plan source is transparent: users know it's AI-informed
- Safety rules are hard-coded and cannot be overridden by user input
- No personalization that could cause harm (no extreme caloric restriction)

---

## 📱 Screenshots

### Landing Screen
```
┌─────────────────────────────┐
│  SOMA  AI Fitness Coach     │
│                             │
│  Your body.                 │
│  Your plan.                 │
│                             │
│  [Get My Free Plan →]       │
│  No credit card. No signup. │
│                             │
│  <60s   7 days   ₹0         │
└─────────────────────────────┘
```

### Quiz (Step 2 of 5)
```
┌─────────────────────────────┐
│  ████████░░░░░░░░  2/5      │
│                             │
│  What's your main goal?     │
│                             │
│  🔥 Lose weight    ○        │
│  💪 Build muscle   ●  ✓    │
│  🏃 Endurance      ○        │
│  ⭐ General         ○        │
│                             │
│  [Next →]                   │
└─────────────────────────────┘
```

### Daily Tracker
```
┌─────────────────────────────┐
│  🔥 3-day streak             │
│  3 more days for full week  │
│                             │
│  Day 3 — Push Day           │
│  ~35 min · 4 exercises      │
│                             │
│  ☑ Push-ups        4×12    │
│  ☑ Pike push-ups   3×10    │
│  ☐ Tricep dips     3×12    │
│  ☐ Plank           3×40s   │
│                             │
│  [Mark as Complete ✓]       │
└─────────────────────────────┘
```

---

## 🗺 Roadmap (Next Version)

- [ ] **v1.1** — Exercise GIF/image descriptions
- [ ] **v1.2** — Plan adjustment ("make it harder / easier")
- [ ] **v1.3** — Print-friendly plan PDF
- [ ] **v2.0** — Real backend (Supabase) + Claude API for true AI generation
- [ ] **v2.1** — Hindi language support
- [ ] **v2.2** — Email reminders via Resend

---

## 🧪 Test It Locally

No build step needed:

```bash
git clone https://github.com/YOURUSERNAME/soma
cd soma

# Option 1: Python (installed on most systems)
python3 -m http.server 3000
# Open http://localhost:3000

# Option 2: Node
npx serve .
# Open http://localhost:3000

# Option 3: Just open the file
open index.html   # macOS
start index.html  # Windows
```

---

## 💼 Built With

| Technology | Purpose | Cost |
|-----------|---------|------|
| Vanilla HTML/CSS/JS | Entire app | Free |
| Google Fonts (Syne + DM Sans) | Typography | Free |
| localStorage API | Streak + plan persistence | Free |
| Vercel | Hosting + CDN | Free forever |

**Total monthly cost: ₹0**

---

## 📊 Technical Decisions

**Why no React/Vue?**
A 6-screen MVP with no API calls doesn't need a framework. Vanilla JS keeps the bundle at 0kb (no npm install), the repo reviewable in one file, and deployment instant anywhere.

**Why static plans instead of real AI?**
For a portfolio demo, static plans are more reliable, faster, and cost nothing. The architecture is designed to swap in a real Claude API call (see `v2.0` roadmap) when needed — the UI and UX are identical.

**Why localStorage instead of a database?**
DPDPA 2023 compliance is simpler when data stays on the user's device. No server = no data breach risk = no compliance headache for an MVP.

---

## 👤 Author

Built as a portfolio project demonstrating:
- Full product thinking (PM → UX → Engineering → Legal → Launch)
- Indian regulatory compliance (DPDPA 2023, IT Act 2000)
- AI product design with safety guardrails
- Zero-cost production deployment

---

## 📄 License

MIT — Free to use, fork, and deploy. If you build on this, a ⭐ star is appreciated!

---

## ⚠️ Medical Disclaimer

SOMA provides fitness guidance for informational purposes only. It is **not a substitute for professional medical advice**. Always consult a qualified healthcare provider before starting any exercise or diet program, especially if you have pre-existing medical conditions.

---

*Made with 💚 in India · Compliant with DPDPA 2023 · Hosted free on Vercel*
