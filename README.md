# PHEN-RISK Dashboard

Phenological Risk Intelligence System - A multi-satellite early warning system for agricultural risk assessment in West Africa.

## Features

- 🗺️ Interactive regional risk map with clickable markers
- 📊 Real-time NDVI anomalies vs food prices visualization
- 🚨 Risk alerts for multiple districts (Bamako, Niamey, Ouagadougou)
- 📡 Multi-satellite data integration (Sentinel-2, Landsat 8/9, MODIS)
- 🌓 Light/Dark theme toggle
- 📥 Export data as CSV or JSON

## Deploying to Vercel

### Method 1: Vercel CLI (Recommended)

1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm install -g vercel
   ```

2. **Navigate to the project folder**:
   ```bash
   cd phen-risk-vercel
   ```

3. **Deploy**:
   ```bash
   vercel
   ```
   
4. **Follow the prompts**:
   - Set up and deploy? `Y`
   - Which scope? Select your account
   - Link to existing project? `N`
   - Project name? `phen-risk-dashboard` (or your preferred name)
   - Directory? `./` (current directory)
   - Override settings? `N`

5. **Production deployment**:
   ```bash
   vercel --prod
   ```

### Method 2: Vercel Web Dashboard

1. **Go to** [vercel.com](https://vercel.com)

2. **Sign up/Login** with GitHub, GitLab, or Bitbucket

3. **Click "Add New Project"**

4. **Choose one of these options**:

   **Option A: Import from Git**
   - Push this folder to a GitHub repository
   - Import the repository in Vercel
   - Vercel will auto-detect settings
   - Click "Deploy"

   **Option B: Manual Upload**
   - Drag and drop the entire `phen-risk-vercel` folder
   - Or click "Browse" to select the folder
   - Click "Deploy"

### Method 3: GitHub Integration (Best for updates)

1. **Create a new GitHub repository**

2. **Push this folder**:
   ```bash
   cd phen-risk-vercel
   git init
   git add .
   git commit -m "Initial commit: PHEN-RISK Dashboard"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/phen-risk-dashboard.git
   git push -u origin main
   ```

3. **Import to Vercel**:
   - Go to [vercel.com/new](https://vercel.com/new)
   - Select your repository
   - Click "Import"
   - Click "Deploy"

4. **Automatic deployments**: Every push to `main` will automatically deploy!

## Project Structure

```
phen-risk-vercel/
├── index.html          # Main dashboard file
├── logo.svg           # PHEN-RISK logo
├── vercel.json        # Vercel configuration
├── package.json       # Project metadata
└── README.md          # This file
```

## Configuration

The dashboard is a static HTML site with:
- React 18 (via CDN)
- Chart.js 4.4.0
- Leaflet 1.9.4 for maps
- No build process required

## Custom Domain (Optional)

After deployment, you can add a custom domain:

1. Go to your project in Vercel
2. Click "Settings" → "Domains"
3. Add your domain
4. Follow DNS configuration instructions

## Environment

- **Framework**: Static HTML
- **Node.js**: Not required (static site)
- **Build Command**: None
- **Output Directory**: `./`

## Data

Sample data included for three districts:
- Bamako, Mali
- Niamey, Niger
- Ouagadougou, Burkina Faso

## Support

For issues or questions, please open an issue in the repository.

## License

MIT License
