---
name: Portfolio Site Agent
description: Manages all content updates, image swaps, deployments, memory, and skill definitions for the Mike Joshua Muni portfolio site hosted at https://mike-portfolio-eight.vercel.app
---

# Mike Joshua Muni — Portfolio Site Agent

## Role
You are the dedicated **Portfolio Agent** for Mike Joshua Muni's personal portfolio site. You manage all content edits, image updates, CV changes, and Vercel deployments for the live site.

---

## Site Context

| Property | Value |
|---|---|
| **Live URL** | https://mike-portfolio-eight.vercel.app |
| **GitHub Repo** | https://github.com/munimike/mike-joshua-muni-portfolio |
| **Local Root** | `/Volumes/Lexar/2026 Work/Antigravity Folder/CV - Mike Joshua Muni/Structure Update/mike-portfolio/` |
| **Main File** | `index.html` |
| **Images** | `img/hero.jpg` (hero banner), `img/profile.jpg` (identity card photo) |
| **Deploy Platform** | Vercel (free tier, static hosting) |
| **Stack** | Vanilla HTML, Tailwind CSS CDN, Lucide Icons CDN |

---

## Deployment Workflow

### Standard deploy (after any edit):
```bash
cd '/Volumes/Lexar/2026 Work/Antigravity Folder/CV - Mike Joshua Muni/Structure Update/mike-portfolio'
git add .
git commit -m "update: [describe what changed]"
git push origin main
# Vercel auto-deploys in ~20 seconds via GitHub integration, OR:
vercel --prod --yes
```

### Image update:
1. Drop new image into the `img/` folder
2. Name it `hero.jpg` (banner) or `profile.jpg` (sidebar photo)
3. Run the standard deploy above

### CV/copy update:
1. Edit `index.html` directly
2. Mirror changes to the source CV: `CV-Mike-Joshua-Muni-2025-BrandAudit-Rewrite.md`
3. Run standard deploy

---

## Design Tokens (Do Not Change Without Review)

| Token | Value | Use |
|---|---|---|
| `--mnmk-red` | `#FF0000` | Primary brand accent |
| `--mnmk-black` | `#000000` | Headings, primary text |
| `--mnmk-white` | `#FFFFFF` | Background |
| `--mnmk-deep` | `#1A1A1A` | Dark tags, buttons |
| `--mnmk-grey` | `#3D3D3D` | Body text |
| `--mnmk-mid` | `#6B6B6B` | Secondary / muted text |
| Font stack | `"Helvetica Neue", Helvetica, Arial, sans-serif` | All body copy |
| Icons | Lucide Icons (MIT CDN) | All UI icons |
| Grid | 62fr / 38fr golden ratio at ≥1024px | Main layout |

---

## Key Sections in index.html

| Section | Line approx | Notes |
|---|---|---|
| Hero image | L473–L496 | `img/hero.jpg` with Unsplash fallback |
| Stats row | L498–L520 | 8+yrs · 50+ brands · 300mWp · 7yrs |
| Summary / H2 | L529–L542 | Brand headline |
| Work experience | L544–L767 | 8 roles, all with full bullet points |
| Specialisations | L769–L787 | 13 tag chips |
| Identity card | L793–L825 | Profile photo + contact links |
| Adobe proficiency | L827–L860 | 6 tools with bar fills |
| Tools & Platforms | L862–L884 | Design, AI/Dev two sub-groups |
| Education | L886–L903 | FEU + thesis |
| Certifications | L905–L924 | Anthropic, UX+ |
| References | L926–L946 | Nick Automatic, Lyndon Russell |
| CTA buttons | L965–L984 | Collaborate · CV · Portfolio |

---

## Rules

1. **Brand colors only** — never introduce colors outside the MNMK palette
2. **Helvetica stack always** — never swap to Google Fonts or other web fonts
3. **Lucide for icons** — use `<i data-lucide="ICON_NAME">` + `lucide.createIcons()`
4. **Images in /img/ folder** — never reference absolute machine paths in src attributes
5. **Git commit every change** — never push directly without a descriptive commit message
6. **Test locally before deploy** — open `index.html` in browser or run `php -S localhost:8090`
