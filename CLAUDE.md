# CLAUDE.md — Botora AI Website Project

> This file tells Claude Code everything it needs to know about this project.
> Keep this file in the root of your project folder at all times.

---

## Project Overview

**Business:** Botora AI — an AI Automation Agency
**Goal:** A professional website that generates leads, lists services, and books strategy calls
**Stack:** Plain HTML/CSS/JS (single file, no framework needed)
**Hosting:** Vercel (free tier)
**Domain:** botoraai.com (or botora.ai)

---

## Project File Structure

```
botora-ai/
├── CLAUDE.md          ← This file (always keep in root)
├── index.html         ← Main homepage (the website)
├── README.md          ← Setup notes
└── assets/            ← If adding images or icons later
    └── (empty for now)
```

---

## Brand Guidelines

**Company Name:** Botora AI
**Tagline:** "Stop doing work your business can do itself"
**Contact Email:** hello@botoraai.com ← REPLACE WITH YOUR REAL EMAIL
**Booking Link:** https://calendly.com/botoraai ← REPLACE WITH YOUR CALENDLY LINK

**Brand Colors:**
- Background: `#06060a` (near black)
- Accent Green: `#00e5a0` (primary CTA color)
- Accent Blue: `#0062ff`
- Text: `#f0f0f5`
- Muted: `#7a7a90`

**Fonts:** Syne (headings) + DM Sans (body) — loaded from Google Fonts

**Tone of Voice:** Confident, direct, no fluff. Talk to small business owners who are busy and skeptical.

---

## Pages Needed (Build Order)

| Priority | Page | Status |
|----------|------|--------|
| 1 | Homepage (`index.html`) | ✅ Done |
| 2 | Contact / Booking section | ✅ In homepage |
| 3 | Services detail page | 🔲 TODO |
| 4 | Case Studies / Results | 🔲 TODO |
| 5 | About page | 🔲 TODO |

---

## Services Botora AI Offers

1. **AI Lead Follow-Up** — Auto SMS/email to new leads within minutes
2. **Appointment Automation** — Booking, reminders, rescheduling
3. **Review Generation** — Automated Google review requests post-service
4. **CRM & Pipeline Sync** — Auto-log leads, calls, and deals
5. **AI Chat Assistant** — Website/WhatsApp chatbot, 24/7
6. **Custom Workflow Design** — Any bespoke automation pipeline

---

## Target Customers

Small and medium businesses in the US, especially:
- Restaurants & Cafes
- Salons & Spas
- Medical / Dental Clinics
- Real Estate Agencies
- Home Services (cleaners, plumbers, etc.)
- Gyms & Fitness Studios

**Pain point they share:** Too busy to set up automation themselves, losing leads and wasting hours on repetitive tasks.

---

## What Claude Code Should Know

### When editing the homepage:
- Never remove the scroll-reveal animations (`.reveal` class + IntersectionObserver)
- Never change the cursor behavior — it's intentional branding
- All CTAs should point to either `#contact` (anchor) or the Calendly booking link
- Keep the dark theme — do not switch to light mode
- Stats in the hero (10+ hrs saved, 48hr setup, $0 risk) can be updated as real data comes in

### When adding new sections:
- Follow the existing pattern: `section-label` → `section-title` → content
- Use `class="reveal"` on all new elements that should animate in on scroll
- Stick to the existing color variables defined in `:root`

### When adding a contact form:
- Use Tally.co embed (free) — do NOT build a backend
- Embed code goes inside the `#contact` section
- Replace the current email link CTA with the Tally form

### When adding a blog or case studies:
- Keep it as simple HTML cards in a new `blog.html` or `cases.html`
- Link from the main nav

---

## Prompts to Use With Claude Code

### Fix or improve a section:
```
In index.html, update the [SECTION NAME] section. 
Keep the same dark theme, color variables, and animation style.
Here's what I want changed: [DESCRIBE CHANGE]
```

### Add a new page:
```
Create a new file called [PAGE NAME].html for the Botora AI website.
Match the exact design style, fonts, colors, and nav from index.html.
The page should contain: [DESCRIBE CONTENT]
```

### Add a contact form:
```
In index.html, replace the email CTA button in the #contact section
with a Tally.co embedded form. The embed code is: [PASTE TALLY CODE]
Keep the same section styling and heading.
```

### Update copy/text:
```
In index.html, update the following text:
- Hero headline: [NEW HEADLINE]
- Hero subtext: [NEW SUBTEXT]
- Keep all styling, classes, and structure identical.
```

---

## Deployment Instructions (Vercel)

1. Go to https://vercel.com and sign up (free)
2. Click "Add New Project" → "Deploy from GitHub" or drag-drop folder
3. If using GitHub: push your `botora-ai/` folder to a GitHub repo first
4. Vercel auto-detects the HTML — no config needed
5. Add your custom domain in Vercel's "Domains" settings

**To update the site:** Edit `index.html`, push to GitHub → Vercel auto-deploys.

---

## DO NOTs

- ❌ Do not add WordPress or any CMS (overkill for now)
- ❌ Do not add a backend server (use Tally/Typeform for forms)
- ❌ Do not use Bootstrap or Tailwind (custom CSS is already written)
- ❌ Do not change the font families without updating both heading and body
- ❌ Do not use `localStorage` — not needed for this project

---

## Future Upgrades (Later)

- Add Calendly inline booking widget to replace the CTA button
- Add a blog section for SEO (target keywords: "AI automation for small business")
- Add Google Analytics tracking
- Add a case study page once first 2–3 clients are done
- Consider moving to Next.js if site grows beyond 5 pages
