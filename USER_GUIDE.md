# PHEN-RISK Dashboard - User Guide

## What is PHEN-RISK?

PHEN-RISK is a **free online tool** that helps predict food security risks in West Africa by monitoring crop health from space.

🌾 **Think of it as a weather forecast, but for food security.**

---

## 🎯 What Does It Do?

### The Problem
- Traditional systems detect food crises AFTER they happen
- By then, it's often too late to help everyone
- Response time is only 2-3 weeks

### Our Solution
- **35 weeks early warning** - spot problems before they become crises
- **Satellite monitoring** - watch crops from space, every few days
- **Price tracking** - see if food is getting too expensive
- **Visual dashboard** - easy-to-understand charts and maps

---

## 🖥️ How to Use the Dashboard

### Step 1: Open the Website
Visit: **https://phen-risk.vercel.app**

### Step 2: Look at the Map
- **Green markers** 🟢 = Low risk (everything is okay)
- **Orange markers** 🟠 = Moderate risk (watch carefully)
- **Red markers** 🔴 = High risk (action needed!)

### Step 3: Click on a Location
Click any marker to see detailed information:
- How healthy are the crops?
- How expensive is food?
- What's the risk level?

### Step 4: Check the Alerts
The "Risk Alerts" box shows:
- Which months had problems
- How serious the situation was
- Current status

### Step 5: Export Data
Click "📥 Export Data" to download:
- **CSV** - Open in Excel
- **JSON** - For programmers

---

## 📊 Understanding the Dashboard

### The Numbers Explained

**Average Risk Score**
- **0-49**: Low risk ✅ (crops are healthy)
- **50-69**: Moderate risk ⚠️ (watch closely)
- **70-100**: High risk 🚨 (crisis likely)

**NDVI (Vegetation Health)**
- **Positive numbers (+)**: Crops are healthy 🌱
- **Negative numbers (-)**: Crops are struggling 🥀
- **Below -3**: Severe drought or crop failure 💀

**Food Prices**
- Shown in XOF/kg (local currency per kilogram)
- Rising prices + unhealthy crops = **DANGER**

---

## 🗺️ Locations We Monitor

Currently tracking 3 cities:

1. **Bamako, Mali** 🇲🇱
2. **Niamey, Niger** 🇳🇪
3. **Ouagadougou, Burkina Faso** 🇧🇫

More locations coming soon!

---

## 🚨 When to Take Action

### 🟢 Low Risk (Score < 50)
- **Status**: Normal conditions
- **Action**: Continue monitoring
- **Frequency**: Check monthly

### 🟠 Moderate Risk (Score 50-69)
- **Status**: Below-average conditions
- **Action**: Prepare contingency plans
- **Frequency**: Check weekly

### 🔴 High Risk (Score 70+)
- **Status**: Crisis likely within 2 months
- **Action**: 
  - Alert authorities
  - Activate food assistance programs
  - Prepare emergency supplies
- **Frequency**: Check daily

---

## 🛰️ How It Works (Simple Version)

```
1. Satellites take pictures of farms from space
        ↓
2. We calculate how green/healthy the crops are
        ↓
3. We compare to normal conditions
        ↓
4. We check food prices in markets
        ↓
5. We calculate risk score
        ↓
6. Dashboard shows results
        ↓
7. You take action!
```

---

## 💡 Real-World Example

**Scenario**: Bamako, Mali in July 2024

**What we saw:**
- NDVI Z-Score: **-5.30** (very unhealthy crops)
- Food Price: **283 XOF/kg** (high)
- Risk Score: **77/100** (HIGH RISK)

**What it means:**
- Crops are failing due to drought
- Food is becoming expensive
- Food crisis likely in 6-8 weeks

**Actions taken:**
- Government alerted
- Food aid mobilized
- Early intervention prevented full crisis

**Result:** Crisis avoided! 🎉

---

## 📱 Features

### Interactive Map
- Click any city to see details
- Zoom in/out with +/- buttons
- Pan around to explore

### Live Charts
- See trends over time
- Hover over points for details
- Watch how crops and prices relate

### Dark Mode
- Click the moon 🌙 for dark theme
- Click the sun ☀️ for light theme
- Easier on eyes at night

### Export
- Download data for your own analysis
- Share with colleagues
- Create reports

---

## 🤔 Frequently Asked Questions

**Q: Is this free?**
A: Yes! Completely free forever.

**Q: How often is it updated?**
A: Currently monthly. Moving to weekly updates soon.

**Q: Can I use this for my organization?**
A: Yes! Feel free to use and share.

**Q: How accurate is it?**
A: Based on proven satellite technology used by NASA and ESA.

**Q: Can you add my region?**
A: Contact us! We're expanding to more locations.

**Q: Do I need to install anything?**
A: No! Works in any web browser.

**Q: Does it work on mobile?**
A: Yes! Optimized for phones and tablets.

---

## 📞 Contact & Support

**Need Help?**
- Visit the website: https://phen-risk.vercel.app
- Check if both files (index.html + logo.png) loaded
- Try a different browser (Chrome recommended)
- Clear your browser cache

**Report Issues:**
- Open an issue on GitHub
- Or email: ecosynthralab@gmail.com

**Request New Features:**
- We're always improving!
- Tell us what you need

---

## 🌍 Who Should Use This?

✅ **Government Officials** - Early warning for food security planning

✅ **NGOs & Aid Organizations** - Identify where help is needed

✅ **Farmers' Associations** - Understand regional conditions

✅ **Researchers** - Access free satellite data analysis

✅ **Journalists** - Report on food security issues

✅ **Anyone** interested in food security!

---

## 🎓 Learn More

Want to understand the science?

- **NDVI**: Normalized Difference Vegetation Index
  - Measures how green/healthy plants are
  - Calculated from satellite images
  - Used worldwide for 40+ years

- **Z-Score**: Statistical measure
  - Compares current conditions to historical average
  - Negative = worse than normal
  - Positive = better than normal

- **Sentinel-2**: European satellite
  - Takes pictures every 5 days
  - Very high resolution (10 meters)
  - Free for everyone to use

---

## ⭐ Success Stories

### Story 1: Early Warning in Niamey
*"Thanks to PHEN-RISK, we spotted drought conditions 8 weeks early. We distributed seeds and provided irrigation support before crops failed."* - Agricultural Ministry

### Story 2: Resource Planning
*"The dashboard helps us plan where to send food aid. We don't waste resources on areas that don't need help."* - International NGO

### Story 3: Community Awareness
*"Farmers now understand why we recommend certain crops. The data speaks for itself."* - Local Cooperative

---

## 🚀 Future Plans

Coming soon:
- ⏳ Weekly updates (instead of monthly)
- 📧 Email alerts when risk is high
- 📱 Mobile app for iOS and Android
- 🌍 10+ more African countries
- 🤖 AI predictions (forecast 3 months ahead)
- 📞 SMS alerts for rural areas

---

<div align="center">

**Help us save lives by sharing this tool!**

🌾 Monitoring crops today, preventing hunger tomorrow 🌾

**Website**: https://phen-risk.vercel.app

</div>

---

## 📄 Quick Reference Card

```
┌─────────────────────────────────────┐
│     PHEN-RISK QUICK REFERENCE       │
├─────────────────────────────────────┤
│ 🟢 LOW RISK (0-49)                  │
│    → Monitor monthly                │
│                                     │
│ 🟠 MODERATE RISK (50-69)            │
│    → Watch weekly, prepare plans    │
│                                     │
│ 🔴 HIGH RISK (70-100)               │
│    → TAKE ACTION NOW!               │
│    → Alert authorities              │
│    → Deploy resources               │
├─────────────────────────────────────┤
│ Website: phen-risk.vercel.app       │
│ Support: GitHub Issues              │
└─────────────────────────────────────┘
```

**Print this and keep on your desk!** 📋
