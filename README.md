# IPOVista 
### Indian IPO Analytics Dashboard

> Search any IPO from 2010–2022 and instantly see subscription data, listing gains, investor sentiment scores, peer comparisons, and market-wide trends — all in one dark-mode dashboard.


[![Dataset](https://img.shields.io/badge/Dataset-319%20IPOs-c8f03c?style=for-the-badge)](https://github.com/Ayushd172005/IPOVista)

---

## Repository Structure

This project is split across two repositories:

| Repo | Purpose | Link |
|---|---|---|
| `IPOVista` | Source code — logic, data, styles | [github.com/Ayushd172005/IPOVista](https://github.com/Ayushd172005/IPOVista) |
| `IPOVista_Deployment` | Production build hosted on Vercel | [github.com/Ayushd172005/IPOVista_Deployment](https://github.com/Ayushd172005/IPOVista_Deployment) |

The source repo (`IPOVista`) holds everything you develop and edit. When changes are ready, the updated files are pushed to `IPOVista_Deployment`, which Vercel watches and auto-deploys.

---

## Features

- **Company Search** — Type any company name for a full IPO breakdown
- **Subscription Analysis** — QIB, HNI, and RII subscription charts side by side
- **Listing Gain Benchmark** — Compare a stock's listing gain vs. its year's average and the all-time average
- **Investor Sentiment Score** — Composite 0–100 score derived from subscription strength and listing performance
- **Peer IPOs** — Other companies that listed within 90 days, clickable for instant comparison
- **Analyst Summary** — Auto-generated narrative verdict (Buy / Hold / Avoid) for each IPO
- **Market Overview** — Year-by-year average gains, IPO count per year, gain distribution histogram
- **Leaderboard** — Top 50 IPOs ranked by best gainers, worst performers, most subscribed, or largest issue size

---

## Dataset

- **319 Indian IPOs** spanning 2010–2022
- Source: `Indian_IPO_Market_Data.csv` (compiled into `data.js` for browser use)
- Fields: IPO name, listing date, issue size (₹ Cr), QIB / HNI / RII subscription multiples, total subscription, issue price, listing day gain %

---

## File Structure

```
IPOVista/                  ← this repo (source)
├── index.html             # Main HTML — 3 views: Search, Market, Leaderboard
├── style.css              # Dark theme — lime accent, Syne + DM Mono fonts
├── app.js                 # All logic — search, Chart.js rendering, sentiment
├── data.js                # 319 IPO records compiled from CSV
├── vercel.json            # Static deployment config
└── README.md

```

---

## Tech Stack

- **Vanilla HTML / CSS / JS** — zero frameworks, zero build step
- **[Chart.js 4](https://www.chartjs.org/)** — bar charts, histograms, benchmark comparisons
- **Google Fonts** — Syne (display) + DM Mono (data) + Inter (body)
- **Vercel** — static hosting with automatic deploys from `IPOVista_Deployment`

---

## Local Development

No installation needed. Just clone and open:

```bash
git clone https://github.com/Ayushd172005/IPOVista.git
cd IPOVista

# Option 1 — open directly
open index.html

# Option 2 — local server (avoids any CORS edge cases)
npx serve .
# or
python3 -m http.server 8080
```



---

## Screenshots

> Search View 
<img width="1280" height="800" alt="Screenshot 2026-05-16 at 12 18 07 PM" src="https://github.com/user-attachments/assets/7241d254-75fd-45f7-bd70-8f09ecc2215d" />
> Example Company(Zomato)
<img width="1280" height="800" alt="Screenshot 2026-05-16 at 12 20 11 PM" src="https://github.com/user-attachments/assets/75150dee-380d-4430-9020-513b25df0463" />
<img width="1280" height="800" alt="Screenshot 2026-05-16 at 12 21 50 PM" src="https://github.com/user-attachments/assets/4b4b71fa-8f0a-40fe-9373-0a2b653e3083" />

> Market Overview 
<img width="1280" height="800" alt="Screenshot 2026-05-16 at 12 22 40 PM" src="https://github.com/user-attachments/assets/d889a5af-8140-4c2f-94db-3d6ac4a94fd2" />

> Leaderboard
<img width="1280" height="800" alt="Screenshot 2026-05-16 at 12 23 11 PM" src="https://github.com/user-attachments/assets/8af4cce0-3bf7-4576-ab52-49c1aed32ddb" />


---

## Author

**Ayush D** — [@Ayushd172005](https://github.com/Ayushd172005)

---

*Built with vanilla JS and a lot of IPO data.*
