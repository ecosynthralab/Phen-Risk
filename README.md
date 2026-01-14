# PHEN-RISK Dashboard 🌾

**Phenological Risk Intelligence System** - Early warning system for agricultural risk in West Africa using satellite data.

---

## 🌍 What It Does

PHEN-RISK monitors crop health from space and predicts food security risks **35 weeks in advance** by combining:
- 🛰️ Satellite vegetation data (NDVI)
- 💰 Market food prices
- 📊 Historical patterns

---

## 🚀 How to Use

1. **Open**: [https://phen-risk.vercel.app](https://phen-risk.vercel.app)
2. **Select District**: Click a location on the map or district card
3. **View Risk Level**: Check the risk score and alerts
4. **Export Data**: Download CSV or JSON for further analysis

---

## 📊 Risk Score Interpretation

### Risk Levels

| Score | Level | Status | Action Required |
|-------|-------|--------|-----------------|
| **0-49** | 🟢 **LOW RISK** | Normal conditions | Monitor monthly |
| **50-69** | 🟠 **MODERATE RISK** | Below-average vegetation | Prepare contingency plans, check weekly |
| **70-100** | 🔴 **HIGH RISK** | Crisis likely in 6-8 weeks | **Take immediate action**, alert authorities |

### NDVI Z-Score (Vegetation Health)

| Z-Score | Meaning | Crop Status |
|---------|---------|-------------|
| **< -3.0** | Severe stress | Drought/crop failure likely |
| **-3.0 to -1.5** | Moderate stress | Below-average vegetation |
| **-1.5 to +1.5** | Normal | Healthy vegetation |
| **> +1.5** | Excellent | Above-average conditions |

### Combined Interpretation

- **Negative NDVI + Rising Prices** = 🚨 **High Risk** (Food crisis warning)
- **Negative NDVI + Stable Prices** = ⚠️ **Watch closely** (Potential risk)
- **Positive NDVI + Any Price** = ✅ **Low Risk** (Normal conditions)

---

## 📍 Monitored Locations

- **Bamako, Mali** 🇲🇱
- **Niamey, Niger** 🇳🇪
- **Ouagadougou, Burkina Faso** 🇧🇫

---

## 🛰️ Data Sources

- **Sentinel-2** (10m resolution, 5-day revisit)
- **Landsat 8/9** (30m resolution, 16-day revisit)
- **MODIS** (250m resolution, daily)
- **Price Data**: World Food Programme markets

---

## 📥 Features

- ✅ Interactive risk map
- ✅ Time-series charts (NDVI vs Prices)
- ✅ Monthly risk assessment table
- ✅ Real-time alerts
- ✅ Export data (CSV/JSON)
- ✅ Dark/Light theme
- ✅ Mobile responsive

---

## 🎯 Who Should Use This

- Government agencies (food security planning)
- NGOs & humanitarian organizations
- Agricultural researchers
- Early warning system operators
- Policy makers

---

## 🔄 Updates

Data is updated **monthly** with the latest satellite observations and market prices.

---

## 📞 Support

- **Live Dashboard**: [https://phen-risk.vercel.app](https://phen-risk.vercel.app)
- **Issues**: [GitHub Issues](https://github.com/ecosynthralab/Phen-Risk/issues)
- **Documentation**: See repository docs folder

---

## 📄 License

MIT License - Free to use and modify

---

<div align="center">

**Built for food security in West Africa** 🌍

*Monitoring crops today, preventing hunger tomorrow*

</div>
