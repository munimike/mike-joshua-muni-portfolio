# Portfolio Site Memory

## Project Identity
- **Owner:** Mike Joshua Muni
- **Site:** https://mike-portfolio-eight.vercel.app
- **Repo:** https://github.com/munimike/mike-joshua-muni-portfolio
- **Vercel account:** mikeatwork98-4249
- **Local root:** `/Volumes/Lexar/2026 Work/Antigravity Folder/CV - Mike Joshua Muni/Structure Update/mike-portfolio/`

## Confirmed Stack
- Vanilla HTML · Tailwind CSS CDN · Lucide Icons (MIT CDN)
- Static site — no build step, no framework
- Deploy: `vercel --prod --yes` or git push (if GitHub integration connected)

## Brand Colors (LOCKED)
- Red: `#FF0000` — accent only
- Black: `#000000` — headings, buttons
- White: `#FFFFFF` — background
- Deep Grey: `#1A1A1A` — dark surfaces
- Font: `"Helvetica Neue", Helvetica, Arial, sans-serif`

## Image Setup
- Hero banner: `img/hero.jpg` (Unsplash office photo is the onerror fallback)
- Profile photo: `img/profile.jpg` (grey user silhouette is the onerror fallback)
- Both use native HTML `onerror` for graceful degradation

## CTAs (Current)
1. Let's Collaborate → `mailto:mikeatwork98@gmail.com`
2. Download CV → `https://drive.google.com/uc?export=download&id=1w6tdXOxaj2TVMdOhSsfcf0cKH3ELYJI3`
3. View Portfolio → `https://drive.google.com/drive/folders/1wZGFG7oFiBPDEyWiJ_jWGvGS9gZXa-Ru?usp=sharing`

## Pending Updates
- [x] Replace Download CV Google Drive placeholder with real PDF link
- [x] Upload `img/hero.jpg` (custom hero banner photo)
- [x] Upload `img/profile.jpg` (headshot / profile photo)
- [ ] Connect GitHub repo to Vercel for automatic git-push deploys
- [ ] Update `README.md` with final Vercel URL alias

## Decision Log
| Date | Decision | Reason |
|---|---|---|
| 2026-03-05 | Static HTML over PHP/Laravel for Vercel | Vercel can't run PHP; static = zero-config |
| 2026-03-05 | Lucide Icons CDN | MIT license, no build step required |
| 2026-03-05 | 62/38 golden ratio column split | ui-grid-system skill: golden ratio sidebar |
| 2026-03-05 | onerror fallback on images | Allows local images without breaking live site |

## Phase Log
### Phase 1 — Initial Build (2026-03-05)
- Built `about-preview.php` with full CV copy, 8pt grid tokens, MNMK brand, Lucide icons
- Converted to static `index.html` for Vercel
- Git repo initialised at github.com/munimike/mike-joshua-muni-portfolio
- Deployed to Vercel free tier as mikeatwork98-4249

### Phase 2 — Image & CTA Updates (2026-03-05)
- Added `/img/` folder with hero + profile image support
- Added graceful onerror fallbacks on both images
- Added Portfolio CTA button (View Portfolio → mnmkstudio.com)
- Created `.agent/` system for persistent site management
