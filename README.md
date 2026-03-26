# VAYUZ Signal Engine

LinkedIn Signal Intelligence Platform — Apify + Gemini AI → Outreach Ready Leads.

## Deploy to Vercel (3 ways)

---

### Option 1 — Vercel CLI (fastest)

```bash
# 1. Install Vercel CLI
npm install -g vercel

# 2. Go into this folder
cd vayuz-signal-engine

# 3. Deploy
vercel

# Follow prompts:
# → Set up and deploy? Y
# → Which scope? (your account)
# → Link to existing project? N
# → Project name: vayuz-signal-engine
# → In which directory is your code? ./
# → Want to override settings? N

# 4. Done — Vercel gives you a live URL instantly
```

---

### Option 2 — GitHub + Vercel Dashboard (recommended for teams)

```
1. Create a GitHub repo (public or private)
2. Push this folder to it:
   git init
   git add .
   git commit -m "Initial deploy"
   git remote add origin https://github.com/YOUR_USERNAME/vayuz-signal-engine.git
   git push -u origin main

3. Go to vercel.com → New Project → Import from GitHub
4. Select your repo → click Deploy
5. Done — auto-deploys on every git push
```

---

### Option 3 — Drag & Drop (no CLI needed)

```
1. Go to vercel.com → Log in
2. Click "Add New Project"
3. Scroll down → "Deploy without Git"
4. Drag the entire vayuz-signal-engine folder into the drop zone
5. Click Deploy
6. Done
```

---

## Project Structure

```
vayuz-signal-engine/
├── public/
│   └── index.html        ← Full app (HTML + CSS + JS, single file)
├── vercel.json           ← Vercel routing config
├── package.json
└── README.md
```

## How it works

1. **Configure** — Add Apify API token + Gemini API key
2. **Run Pipeline** — Fetches LinkedIn posts via `harvestapi/linkedin-post-search` (no LinkedIn cookies needed)
3. **Gate 1** — Keyword + title rule filter (OR logic, auto-fallback)
4. **Gate 2** — Gemini AI scores each post for intent, signals, and reasoning
5. **Outreach** — Ready-to-reach leads with post URL, score, signal chips

## API Keys needed

| Key | Where to get |
|-----|-------------|
| Apify API Token | apify.com → Settings → Integrations |
| Gemini API Key | aistudio.google.com → Get API Key (free) |

## Notes

- All API keys are entered in the app UI — never hardcoded
- No backend required — pure static HTML
- Works on any static host (Vercel, Netlify, GitHub Pages)
