# Quick Deployment Guide for PHEN-RISK Dashboard

## 🚀 Fastest Method: Vercel CLI

### Step 1: Install Vercel CLI
```bash
npm install -g vercel
```

### Step 2: Navigate to folder
```bash
cd phen-risk-vercel
```

### Step 3: Deploy
```bash
vercel
```

### Step 4: Production deploy
```bash
vercel --prod
```

**Done!** Your site will be live at: `https://your-project-name.vercel.app`

---

## 🌐 Alternative: Vercel Web (No CLI needed)

### Method A: Drag & Drop
1. Go to https://vercel.com
2. Sign up/Login
3. Click "Add New" → "Project"
4. Drag the `phen-risk-vercel` folder into the upload area
5. Click "Deploy"

### Method B: GitHub (Best for updates)
1. Create GitHub account (if needed)
2. Create new repository
3. Upload the `phen-risk-vercel` folder
4. Go to https://vercel.com/new
5. Import your repository
6. Click "Deploy"

**Benefit**: Every time you push changes to GitHub, Vercel automatically redeploys!

---

## 📝 What You Get

After deployment:
- ✅ Live URL: `https://your-project.vercel.app`
- ✅ HTTPS enabled automatically
- ✅ Global CDN
- ✅ Instant updates
- ✅ Free hosting!

---

## ⚙️ Optional: Custom Domain

After deployment:
1. Go to your project in Vercel
2. Settings → Domains
3. Add your domain (e.g., `phen-risk.com`)
4. Update DNS records as instructed

---

## 🆘 Troubleshooting

**Issue**: Site shows blank page
- **Solution**: Make sure `index.html` and `logo.svg` are in the root folder

**Issue**: Logo not showing
- **Solution**: Both files must be uploaded together

**Issue**: Vercel CLI not found
- **Solution**: Install Node.js first from https://nodejs.org

---

## 📞 Need Help?

- Vercel Docs: https://vercel.com/docs
- Vercel Support: https://vercel.com/support
