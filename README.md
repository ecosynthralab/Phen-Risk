# PHEN-RISK Dashboard 🌾

**Phenological Risk Intelligence System** - A multi-satellite early warning system for agricultural risk assessment in West Africa.

![PHEN-RISK Dashboard](https://img.shields.io/badge/Status-Live-success)
![License](https://img.shields.io/badge/License-MIT-blue)
![Platform](https://img.shields.io/badge/Platform-Vercel-black)

---

## 📖 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [How It Works](#how-it-works)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Data Sources](#data-sources)
- [Workflow](#workflow)
- [Installation & Deployment](#installation--deployment)
- [Usage Guide](#usage-guide)
- [API Integration](#api-integration)
- [Contributing](#contributing)
- [License](#license)

---

## 🌍 Overview

PHEN-RISK is an advanced agricultural risk monitoring dashboard that combines satellite imagery analysis with food price data to provide early warning signals for food security risks in West Africa. The system monitors vegetation health through NDVI (Normalized Difference Vegetation Index) anomalies and correlates them with market prices to predict potential food crises weeks in advance.

### Problem Statement

Traditional food security monitoring systems:
- React to crises after they occur (2-3 weeks response time)
- Lack integration between environmental and economic indicators
- Limited satellite data coverage
- Manual analysis is slow and resource-intensive

### Our Solution

PHEN-RISK provides:
- ⏱️ **35 weeks lead time** for early intervention
- 📡 **Multi-satellite integration** (Sentinel-2, Landsat 8/9, MODIS)
- 📊 **Real-time visualization** of risk indicators
- 🗺️ **Interactive mapping** of affected regions
- 📥 **Exportable data** for further analysis

---

## ✨ Features

### 🗺️ Interactive Regional Risk Map
- Click-to-explore district details
- Color-coded risk levels (red/orange/green)
- Real-time marker updates
- OpenStreetMap integration

### 📊 Data Visualization
- **Dual-axis charts** showing NDVI anomalies vs food prices
- **Monthly risk assessment** with visual risk bars
- **Time-series analysis** spanning full year
- **Multi-source satellite** data integration

### 🚨 Smart Risk Alerts
- Real-time alerts for high-risk periods
- Historical risk tracking
- Severity classification (High/Moderate/Low)
- Month-by-month breakdown

### 📈 Key Metrics Dashboard
- Average Risk Score with year-over-year comparison
- High Risk Months counter
- Active Satellites status
- Lead Time indicator

### 🎨 User Experience
- 🌓 **Dark/Light mode** toggle
- 📱 **Responsive design** (mobile, tablet, desktop)
- 📥 **Export capabilities** (CSV, JSON)
- ⚡ **Fast loading** with CDN-hosted libraries

### 🌍 Multi-District Coverage
Currently monitoring:
- **Bamako, Mali**
- **Niamey, Niger**
- **Ouagadougou, Burkina Faso**

---

## 🔬 How It Works

### 1. Data Collection

```
┌─────────────────────────────────────────┐
│         SATELLITE SOURCES               │
├─────────────────────────────────────────┤
│  🛰️ Sentinel-2   (10m resolution)      │
│  🛰️ Landsat 8/9  (30m resolution)      │
│  🛰️ MODIS        (250m resolution)     │
└─────────────────────────────────────────┘
           │
           ▼
┌─────────────────────────────────────────┐
│       NDVI CALCULATION                  │
│  (Normalized Difference Vegetation)     │
│                                         │
│  NDVI = (NIR - Red) / (NIR + Red)      │
└─────────────────────────────────────────┘
           │
           ▼
┌─────────────────────────────────────────┐
│      ANOMALY DETECTION                  │
│  Z-Score = (NDVI - Mean) / StdDev      │
│                                         │
│  Negative Z-score = Vegetation stress   │
└─────────────────────────────────────────┘
```

### 2. Risk Assessment Algorithm

The system calculates risk scores based on multiple factors:

```javascript
Risk Score = f(
  NDVI_zscore,      // Vegetation health (-6 to +2)
  Food_prices,       // Market price (XOF/kg)
  Historical_trend,  // Comparison with previous years
  Seasonal_pattern   // Expected vs actual vegetation
)

Risk Levels:
- HIGH RISK:     Score ≥ 70  (Immediate intervention needed)
- MODERATE RISK: Score 50-69 (Monitor closely)
- LOW RISK:      Score < 50  (Normal conditions)
```

### 3. Data Pipeline

```
Raw Satellite Data
       ↓
  Cloud Removal
       ↓
  NDVI Calculation
       ↓
  Z-Score Normalization
       ↓
  Price Data Integration
       ↓
  Risk Score Computation
       ↓
  Dashboard Visualization
       ↓
  Alert Generation
```

### 4. Interpretation

| NDVI Z-Score | Vegetation Status | Meaning |
|--------------|-------------------|---------|
| < -3.0 | Severe stress | Drought/crop failure likely |
| -3.0 to -1.5 | Moderate stress | Below-average vegetation |
| -1.5 to +1.5 | Normal | Healthy vegetation |
| > +1.5 | Above average | Excellent conditions |

---

## 🛠️ Technology Stack

### Frontend
- **React 18** - UI framework (via CDN)
- **Chart.js 4.4.0** - Data visualization
- **Leaflet 1.9.4** - Interactive maps
- **HTML5/CSS3** - Modern web standards
- **Babel Standalone** - JSX transformation

### Backend & Data
- **Static Site** - No server required
- **JSON Data** - Structured time-series data
- **REST API Ready** - Designed for future API integration

### Deployment
- **Vercel** - Hosting and CDN
- **GitHub** - Version control
- **Git** - Source management

### Development Tools
- **VSCode** - Code editor
- **Git CLI** - Version control
- **Chrome DevTools** - Debugging

---

## 📁 Project Structure

```
phen-risk-dashboard/
├── index.html              # Main dashboard file
├── logo.png                # Application logo
├── README.md               # This file
├── LICENSE                 # MIT License
│
├── docs/                   # Documentation
│   ├── DEPLOYMENT.md       # Deployment guide
│   ├── API.md             # API documentation (future)
│   └── CONTRIBUTING.md     # Contribution guidelines
│
└── data/                   # Data structure (embedded in HTML)
    └── districts/
        ├── bamako.json
        ├── niamey.json
        └── ouagadougou.json
```

### Key Files

**index.html** (Main Application)
- Complete single-page application
- Embedded data and logic
- Self-contained (no external JS files)
- Size: ~45KB (gzipped: ~12KB)

**logo.png** (Brand Identity)
- PNG format for reliability
- Size: 30KB
- Dimensions: 277x271px

---

## 📊 Data Sources

### Satellite Data

1. **Sentinel-2** (Primary Source)
   - Provider: European Space Agency (ESA)
   - Resolution: 10m
   - Revisit: 5 days
   - Bands: Multispectral (13 bands)
   - Free access via Copernicus

2. **Landsat 8/9** (Secondary Source)
   - Provider: NASA/USGS
   - Resolution: 30m
   - Revisit: 16 days
   - Bands: Multispectral (11 bands)
   - Free access via USGS Earth Explorer

3. **MODIS** (Gap Filling)
   - Provider: NASA
   - Resolution: 250m
   - Revisit: Daily
   - Use case: Cloud-covered periods
   - Free access via NASA EOSDIS

### Price Data

- **Source**: World Food Programme (WFP) Price Database
- **Frequency**: Monthly
- **Commodity**: Staple grains (millet, sorghum, rice)
- **Currency**: West African CFA Franc (XOF)
- **Markets**: Major urban markets in capital cities

### Data Format

```json
{
  "district": "Bamako",
  "country": "Mali",
  "coordinates": [12.65, -8.0],
  "timeseries": [
    {
      "date": "2024-01-01",
      "month": 1,
      "ndvi_zscore": -2.87,
      "price": 204,
      "risk_score": 56,
      "risk_level": "MODERATE RISK",
      "source": "Sentinel-2"
    }
  ]
}
```

---

## 🔄 Workflow

### Development Workflow

```
┌─────────────────────────────────────────────┐
│  STEP 1: LOCAL DEVELOPMENT (VSCode)        │
├─────────────────────────────────────────────┤
│  • Edit index.html                          │
│  • Preview with Live Server                 │
│  • Test functionality                       │
│  • Verify responsive design                 │
└─────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────┐
│  STEP 2: VERSION CONTROL (Git)             │
├─────────────────────────────────────────────┤
│  $ git add .                                │
│  $ git commit -m "Update description"       │
│  $ git push origin main                     │
└─────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────┐
│  STEP 3: SOURCE HOSTING (GitHub)           │
├─────────────────────────────────────────────┤
│  • Repository: phen-risk-dashboard          │
│  • Branch: main                             │
│  • Visibility: Public                       │
└─────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────┐
│  STEP 4: AUTO-DEPLOYMENT (Vercel)          │
├─────────────────────────────────────────────┤
│  • Detects push to main                     │
│  • Builds (instant for static)              │
│  • Deploys to global CDN                    │
│  • Live in ~30 seconds                      │
└─────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────┐
│  STEP 5: PRODUCTION (Live Site)            │
├─────────────────────────────────────────────┤
│  🌐 https://phen-risk.vercel.app           │
│  ✅ HTTPS enabled                           │
│  ✅ Global CDN                              │
│  ✅ Auto-scaling                            │
└─────────────────────────────────────────────┘
```

### Data Update Workflow

```
New Satellite Data Available
       ↓
Download & Process NDVI
       ↓
Calculate Z-Scores
       ↓
Fetch Latest Prices
       ↓
Update JSON Data in HTML
       ↓
Git Commit & Push
       ↓
Vercel Auto-Deploy
       ↓
Live Dashboard Updated
```

### User Interaction Flow

```
User Visits Site
       ↓
Dashboard Loads (index.html)
       ↓
React Initializes
       ↓
Data Renders (Charts, Map, Stats)
       ↓
User Interactions:
├─ Select District → Update All Views
├─ Toggle Theme → Dark/Light Mode
├─ Click Map Marker → Zoom to District
├─ Hover Chart → Show Tooltips
└─ Click Export → Download CSV/JSON
```

---

## 🚀 Installation & Deployment

### Prerequisites

- Git installed
- GitHub account
- Vercel account
- VSCode (recommended)

### Quick Start

```bash
# 1. Clone or download the repository
git clone https://github.com/YOUR_USERNAME/phen-risk-dashboard.git
cd phen-risk-dashboard

# 2. Preview locally (optional)
# Open index.html in browser or use Live Server in VSCode

# 3. Deploy to Vercel
# Option A: Via CLI
npm install -g vercel
vercel

# Option B: Via GitHub integration
# - Push to GitHub
# - Import in Vercel dashboard
# - Auto-deploys on every push
```

### Detailed Deployment Guide

See [DEPLOYMENT_VSCODE_GITHUB_VERCEL.md](./DEPLOYMENT_VSCODE_GITHUB_VERCEL.md) for complete step-by-step instructions.

---

## 📖 Usage Guide

### For End Users

1. **View Regional Overview**
   - Map shows all monitored districts
   - Color indicates risk level (red = high, green = low)

2. **Select a District**
   - Click map marker OR
   - Click district card below map
   - All visualizations update automatically

3. **Analyze Risk Trends**
   - **Chart**: Shows NDVI anomalies (green line) vs prices (red line)
   - **Table**: Monthly breakdown with risk scores
   - **Alerts**: High-priority months highlighted

4. **Export Data**
   - Click "Export Data" button
   - Choose CSV (spreadsheet) or JSON (programmatic)
   - File downloads automatically

5. **Toggle Theme**
   - Click moon 🌙 icon for dark mode
   - Click sun ☀️ icon for light mode

### For Analysts

**Interpreting the Dashboard:**

- **NDVI Z-Score < -3**: Severe vegetation stress
  - Action: Immediate food security assessment
  - Timeline: Crisis likely within 4-8 weeks

- **Price spike + Negative NDVI**: High-risk scenario
  - Action: Activate emergency response
  - Priority: Food distribution planning

- **Risk Score > 70**: Critical threshold
  - Action: Alert decision-makers
  - Response: Deploy resources

### For Developers

**Customizing the Dashboard:**

1. **Add New Districts**
```javascript
// In index.html, add to districtData object:
'new_district': {
  name: 'New District',
  country: 'Country',
  coordinates: [lat, lon],
  timeseries: [/* data array */]
}
```

2. **Modify Risk Algorithm**
```javascript
// Find the risk calculation section
// Adjust weights or thresholds
const risk_score = calculateRisk(ndvi, price, historical);
```

3. **Change Color Scheme**
```css
/* In <style> section */
:root {
  --primary-green: #4A7C59;  /* Change colors */
  --primary-orange: #F5A623;
  /* ... */
}
```

---

## 🔌 API Integration (Future)

The dashboard is designed to integrate with a REST API:

### Planned Endpoints

```
GET /api/districts
GET /api/districts/{id}
GET /api/districts/{id}/timeseries
GET /api/alerts
POST /api/export
```

### Current Implementation

Data is embedded in HTML. To migrate to API:

```javascript
// Replace embedded districtData with:
const fetchDistrictData = async () => {
  const response = await fetch('/api/districts');
  const data = await response.json();
  return data;
};
```

---

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](./CONTRIBUTING.md) for guidelines.

### Development Setup

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

### Areas for Contribution

- 🗺️ Add more districts/countries
- 📊 New visualization types
- 🔍 Advanced analytics features
- 🌐 Internationalization (i18n)
- 📱 Mobile app version
- 🤖 ML-powered predictions

---

## 📄 License

MIT License - see [LICENSE](./LICENSE) file

---

## 🙏 Acknowledgments

- **European Space Agency (ESA)** - Sentinel-2 data
- **NASA** - Landsat and MODIS data
- **USGS** - Earth observation infrastructure
- **World Food Programme** - Price data
- **OpenStreetMap** - Base map tiles

---

## 📞 Contact & Support

- **Live Demo**: https://phen-risk.vercel.app
- **Issues**: GitHub Issues
- **Email**: your-email@example.com
- **Documentation**: [Full Docs](./docs/)

---

## 🎯 Roadmap

### Version 2.0 (Planned)
- [ ] Real-time API integration
- [ ] User authentication
- [ ] Custom alert thresholds
- [ ] Historical data archive (5+ years)
- [ ] Predictive modeling with ML
- [ ] Mobile app (iOS/Android)

### Version 1.1 (In Progress)
- [x] PNG logo implementation
- [x] Vercel deployment
- [ ] Additional districts (10+ regions)
- [ ] Weekly data updates
- [ ] Email alert system

---

<div align="center">

**Built with ❤️ for food security in West Africa**

⭐ Star this repo if you find it useful!

</div>
