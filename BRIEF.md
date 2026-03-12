# Build Brief: Antonio Ernesto Knowledge Hub

## What to Build
A single-file `index.html` knowledge hub page for Antonio Ernesto (CEO, IBOPE Media Tech / Kantar).
This is NOT a consulting page — it's an intelligence dashboard / knowledge map displaying everything we know about Antonio, organized visually with a neural mindmap.

## Design System (MUST match exactly)
Copy the EXACT same design tokens, fonts, and visual language from the reference file at `/tmp/culturabusiness/index.html`:
- Dark theme: `--bg: #06080f`, `--s1: #0b1120`, etc.
- Fonts: Syne (headers), IBM Plex Mono (labels/mono), Inter (body)
- Grid overlay on body::before
- Fixed nav with backdrop blur
- Accent blue: `#3b82f6`, green: `#10b981`, gold: `#f59e0b`, red: `#ef4444`
- Same button styles, card styles, section spacing

## Icons: Lucide ONLY
- Load from CDN: `<script src="https://unpkg.com/lucide@latest"></script>`
- Call `lucide.createIcons()` after DOM load
- ZERO emojis anywhere. Use `<i data-lucide="icon-name"></i>` for ALL icons
- Example icons: activity, brain, briefcase, calendar, heart, shield, users, target, trending-up, swords, pill, moon, sun, map-pin, plane, book-open, crown, dumbbell, zap, eye, clock, alert-triangle, check-circle, x-circle, chevron-right, layers, network, git-branch

## Content Sections

### 1. Hero
- Name: Antonio Wanderley
- Title: CEO — IBOPE Media Tech / Kantar (WPP) | HIG Capital
- Stats: ~4,100 employees | ~$500M revenue | LATAM, Spain, South Africa, Turkey, Vietnam, Chile
- Age 47 | ENTP | Miami, FL

### 2. Neural Mindmap (MAIN FEATURE)
A full-width interactive canvas/SVG mindmap showing ALL knowledge domains and their connections:

**Central Node:** Antonio Wanderley

**Primary Clusters (connected to center):**
1. **Health OS** (green accent) — connects to: Sleep, BJJ, TRT Protocol, Supplements, Biomarcadores, Lesões, Gut Health, Farmacogenômica
2. **Business OS** (blue accent) — connects to: 5.15 Framework, MBR, AP2026, EXCO, Talent Review, Pay Grid, Korn Ferry
3. **Executive Team** (gold accent) — connects to: Marcio Costa, Fernando Oliveira, Iván Galvis, Oscar Padilla, Adriana Favaro
4. **Sovereign Architecture** (purple/violet accent) — connects to: Prime Objective, Barbell Strategy, Positive Paranoia, Taleb/Sutherland Axis, 4 Epochs, 7 Nodes
5. **Personal** (warm accent) — connects to: Family, Faith, BJJ, Travel, Bible Reading Plan

**Cross-connections (dotted lines between clusters):**
- BJJ ↔ Lesões ↔ Sleep (health feedback loops)
- Talent Review ↔ Executive Team (people intelligence)
- Sovereign Architecture ↔ Business OS (strategic layer)
- TRT Protocol ↔ Biomarcadores ↔ Supplements (clinical chain)

**Mindmap behavior:**
- Nodes should gently float/breathe (subtle CSS animation)
- Hovering a node highlights its connections
- Clicking a node scrolls to the relevant section below
- Lines between nodes should animate on load (draw-in effect)
- Use SVG for lines, HTML elements for nodes (positioned absolutely)

### 3. Health Profile (BioRack)
Cards showing:
- **Latest Blood Work** (Mar 10, 2026): Testosterone 966, Hematocrit 48.8%, SHBG 31, Estradiol <30, PSA 2.06, Albumin 4.7
- **Trend indicators** (up/down arrows vs previous)
- **Supplement Stacks** (3 stacks: Morning, Afternoon, Night) — collapsible
- **Board of Specialists** — 15 names with scores: Walker, Huberman, Jamieson, Poliquin, Pavel, Cobb, Myers, McGill, Maffetone, Gironda, Noakes, Galpin, Cabral, Attia, Lyon
- **Injury Map** — Left ankle (2002), Right fibula (2022), L5 bulge, Labrum surgery, Tennis elbow
- **Sleep Baseline** — Wake ~06:15, onset ~23:03, Deep ~61min, HRV ~30ms

### 4. Business OS
- **Frameworks Grid** — 5.15, MBR, AP2026, EXCO, Talent Review KIM, Pay Grid, Korn Ferry, Growth Mindset
- **Financial Snapshot** — LATAM EBITDA +€202.9M vs budget, but Brazil carrying region. Miami -45.1%, Chile -70.2%
- **Documents Ingested** — list of all docs with type badges

### 5. Executive Intelligence
- Cards for each direct report: Marcio, Fernando, Iván, Oscar, Adriana
- Each with: Role, Profile Summary, Flight Risk indicator (low/med/high), Key trait
- Power dynamics section: Patrick, Giles, Nicole+Zuber, Rainer, Budget 2026

### 6. Sovereign Architecture
- Visual of Barbell Strategy (90/10 split)
- 4 Epochs timeline (Radio Owner → Montenegro → PLC → AI-First)
- 7 Nodes grid (LinkedIn, IG, X, YouTube, Pinterest, Substack x2)
- Key concepts: Prime Objective, Positive Paranoia, Taleb/Sutherland Axis

### 7. Personal Profile
- Family, Faith (Reality Church), BJJ schedule
- Upcoming travel timeline (visual): Miami → SP → Rio → Miami → Orlando → Miami
- Bible reading plan tracker

### 8. Kitchen/Dining Room Architecture
- Visual showing the two-group workflow
- Kitchen (input/processing) → Dining Room (clean output)

## Technical Requirements
- Single file: index.html (everything inline — CSS + JS)
- Mobile responsive
- Smooth scroll between sections
- Intersection Observer for fade-in animations
- All content hardcoded (not fetched from API)
- Mindmap must work without external JS libraries (vanilla JS + SVG)
- Total file should be self-contained

## What NOT to include
- No emojis (use Lucide icons)
- No contact forms
- No external API calls
- No login/auth
- No sensitive data (no passwords, no API keys, no full executive chat transcripts)
- No Anastrozole dosage warnings or medical disclaimers beyond factual data

## File Output
Write ONLY `/tmp/antonio-ernesto-site/index.html`
