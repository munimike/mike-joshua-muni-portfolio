---
description: Update hero or profile image for the portfolio site
---

# Update Portfolio Images

## When to use
Run this when replacing the hero banner or identity card profile photo.

## Steps

1. Prepare your image:
   - **Hero banner** → export as `hero.jpg`, min 1400×500px, wide landscape crop
   - **Profile photo** → export as `profile.jpg`, square crop, min 200×200px

// turbo
2. Copy image to the `/img/` folder:
```bash
cp /path/to/your/image.jpg '/Volumes/Lexar/2026 Work/Antigravity Folder/CV - Mike Joshua Muni/Structure Update/mike-portfolio/img/hero.jpg'
# or for profile:
cp /path/to/your/photo.jpg '/Volumes/Lexar/2026 Work/Antigravity Folder/CV - Mike Joshua Muni/Structure Update/mike-portfolio/img/profile.jpg'
```

3. Preview locally before deploying:
```bash
open '/Volumes/Lexar/2026 Work/Antigravity Folder/CV - Mike Joshua Muni/Structure Update/mike-portfolio/index.html'
```

4. If using a **Google Drive** image instead of a local file:
   - Upload image to Google Drive
   - Get a shareable link: `https://drive.google.com/file/d/FILE_ID/view`
   - In `index.html`, replace `src="img/hero.jpg"` with:
     `src="https://drive.google.com/uc?export=view&id=FILE_ID"`
   - Do the same for `src="img/profile.jpg"` if needed

5. Run the deploy workflow: `.agent/workflows/deploy.md`
