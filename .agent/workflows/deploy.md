---
description: Deploy portfolio changes to Vercel production
---

# Deploy Portfolio to Vercel

## When to use
Run this workflow whenever `index.html` or any file in `/img/` has been updated and is ready to ship.

## Steps

// turbo
1. Verify there are no broken links or placeholder values still in index.html before committing.

// turbo
2. Stage and commit all changes:
```bash
cd '/Volumes/Lexar/2026 Work/Antigravity Folder/CV - Mike Joshua Muni/Structure Update/mike-portfolio'
git add .
git commit -m "update: [describe what changed]"
```

// turbo
3. Push to GitHub:
```bash
git push origin main
```

4. Deploy to Vercel production:
```bash
vercel --prod --yes
```

5. Open the live URL to verify:
```bash
open -a '/Volumes/T7 Shield/Applications/Google Chrome.app' 'https://mike-portfolio-eight.vercel.app'
```

6. Update `.agent/memory.md` Phase Log with a summary of what changed.
