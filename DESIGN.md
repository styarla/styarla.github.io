# 🎨 Design System & Architecture Guidelines — `shrina.ux`

Welcome to the design system and architecture documentation for **`shrina.ux`** — a tactile, Y2K-inspired portfolio and research log for a multi-disciplinary **UX Researcher, AI Product Strategist, and Interaction Designer**.

---

## 1. Design Philosophy & Core Principles

1. **Tactile Editorial Aesthetics (Y2K Meets Digital Dossier)**  
   The site blends nostalgic early-2000s desktop nostalgia (pixel accents, dashed grid lines, brutalist borders, drop shadows) with modern editorial serif elegance.
2. **"Story with Receipts" Rigor**  
   Case studies prioritize process proof over superficial final screens. Every claim is backed by method details, sample sizes, quotes, or quantitative metrics.
3. **Scannable Hierarchy for Recruiters**  
   Recruiters and hiring managers spend seconds scanning. Key details (role, timeline, tools, methods, outcomes) are highlighted in upfront meta-grids and badges.
4. **Authentic, Playful Editorial Tone**  
   Headers use conversational, playful titles without sacrificing technical substance underneath.

---

## 2. Color Palette & Theming Variables

All global styles and variables are maintained in `css/style.css`:

| CSS Variable | Hex / Value | Description & Purpose |
| :--- | :--- | :--- |
| `--text-charcoal` | `#1E1E1E` | Primary high-contrast text and solid borders |
| `--bg-cream` | `#FBF8F1` | Soft off-white paper canvas background |
| `--sage-green` | `#C8D3A3` | Primary accent for UX Research tags & success states |
| `--soft-blue` | `#B8C0EC` | Secondary accent for AI Strategy & focus highlights |
| `--dusty-pink` | `#F3C5C5` | Accent color for Interaction Design & primary CTAs |
| `--muted-red` | `#D9534F` | Pixel badge highlights & numeric step counts |
| `--grid-line` | `#E2DDD1` | Subdued linear grid lines for background patterns |

---

## 3. Typography System

The website uses a distinct typographic hierarchy balancing retro digital accents, editorial editorial serifs, clean body copy, and personal handwritten accents.

### Font Families
* **Primary Editorial Headings:** `Newsreader` (Serif) — used for all `h1`, `h2`, `h3`, card titles, and large metric callouts.
* **Body Text & Navigation:** `Outfit` (Sans-Serif) — clean, highly readable font for long-form case studies and meta rows.
* **Monospace / Retro Badges:** `VT323` (Monospace / Pixel) — used for pixel badges, metadata labels (`MY ROLE`, `TIMELINE`), and section tags.
* **Pull-Quotes & Personal Asides:** `Caveat` (Handwritten Cursive) — reserved strictly for qualitative user quotes or personal commentary (**Max 1 per case study**).

---

## 4. Component Library

### Badges & Tags
* `.badge-pixel` — High-visibility star-bracketed pixel tags (`★ SELECTED CASE STUDIES ★`).
* `.tag-pill` — Category pills (`.tag-research`, `.tag-ai`, `.tag-ixd`) with distinct accent background colors.

### Cards & Container Patterns
* `.card-work` — Standard project card featuring offset solid drop-shadows (`box-shadow: 5px 5px 0px var(--text-charcoal)`).
* `.meta-dossier-grid` — Recruiter-focused metadata row displayed at the top of case studies.
* `.tldr-box` — High-priority summary card positioned above the fold in case study entries.
* `.archive-banner` — Grid-backed CTA component connecting the home page to the project archive.

### Buttons
* `.btn-primary` — Solid tactile buttons with 2px borders, custom background fills (`var(--sage-green)`, `var(--dusty-pink)`), and active hover shifts.
* `.btn-secondary` — White-backed offset button variant for low-emphasis actions.

---

## 5. Page Architecture & File Structure

```text
├── index.html              # Homepage with Hero, Featured Work, About, & Contact Teaser
├── projects.html           # Full Project Archive & Filterable Case File Index
├── case-study-template.html# Standardized "Story with Receipts" Case Study Layout
├── contact.html            # Contact Form, Direct Touchpoints & Resume Dossier Vault
├── css/
│   └── style.css           # Global stylesheet containing root variables & component rules
└── assets/
    └── resumes/            # Dedicated PDFs (UX Research, AI Strategy, Interaction Design)