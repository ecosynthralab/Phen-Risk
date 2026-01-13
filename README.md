# PHEN-RISK Dashboard - Simple Deployment

## Quick Fix for Your Current Vercel Issue

### Problem
- Logo showing as "ERR_FILE_NOT_FOUND"
- Files not loading correctly

### Solution

This folder contains ONLY the essential files:
- `index.html` (with relative logo path `./logo.svg`)
- `logo.svg`

## 🚀 Deploy to Vercel (3 Methods)

### Method 1: CLI Redeploy
```bash
cd phen-risk-simple
vercel --prod
```

### Method 2: Drag & Drop
1. Go to https://vercel.com/dashboard
2. Delete your old project (or create new one)
3. Click "Add New" → "Project"  
4. Drag THIS folder (`phen-risk-simple`)
5. Click "Deploy"

### Method 3: GitHub
1. Delete old repository (or create new one)
2. Push these 2 files to GitHub:
   ```bash
   git init
   git add index.html logo.svg
   git commit -m "PHEN-RISK Dashboard"
   git push
   ```
3. Import to Vercel from https://vercel.com/new

## ✅ What's Different

**Old setup** (causing issues):
- Had unnecessary `vercel.json` config
- Had empty `public/` folder
- Used absolute path `/logo.svg`

**New setup** (works perfectly):
- Just 2 files: `index.html` + `logo.svg`
- No configuration needed
- Uses relative path `./logo.svg`

## 🔍 Verification

After deploying, check:
1. Logo appears in header ✅
2. No console errors ✅
3. All emojis display correctly ✅

## 💡 Tips

- Vercel automatically detects this as a static site
- No build process needed
- Deploy takes ~30 seconds
- Your URL: `https://your-project.vercel.app`

## 🆘 Still Having Issues?

Try clearing Vercel cache:
1. Go to your project settings
2. "Advanced" → "Clear Cache"
3. Redeploy

Or contact me for help!
