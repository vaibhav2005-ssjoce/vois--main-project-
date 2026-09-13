# 🌾 Seasonal Agriculture Performance Analysis

A data analytics project investigating how agricultural performance — yield, profitability, water-use efficiency, and disease/pest risk — varies across seasons, crops, irrigation methods, and states in India.

> **VOIS × AICTE Major Project** | Batch 2026–2027

---

## 📌 Overview

Agricultural performance is shaped by seasonal variation in environmental conditions, farming practices, resource availability, and market conditions — but raw data alone doesn't reveal *how* or *why* it changes. This project analyzes **4,000 farm records** across **3 seasons** (Kharif, Rabi, Zaid), **8 Indian states**, and **8 crops** to uncover meaningful seasonal patterns, statistically validate them, and turn them into evidence-based recommendations.

## ❓ Key Questions Answered

- How does yield vary across seasons, and is the difference statistically significant?
- How do environmental conditions (rainfall, temperature) differ by season?
- How do cost, revenue and profit vary by season — are farms actually profitable?
- Do specific crops perform consistently well or poorly across all seasons?
- Does irrigation method affect water-use efficiency, and does this vary by season?
- Is disease/pest risk related to seasonal environmental conditions?
- Which variables correlate most strongly with yield and profit?
- Are seasonal patterns consistent across different states?

## 🔑 Key Findings

| Season | Avg Yield (t/ha) | Avg Profit (₹) | Loss-Making Farms |
|--------|:---:|:---:|:---:|
| **Kharif** | 2.26 | +1,79,000 | 42.2% |
| **Rabi** | 2.04 | ~0 | 51.1% |
| **Zaid** | 1.81 | −24,800 | 64.5% |

- **Kharif is the strongest season** overall — highest yield and profit, driven by monsoon rainfall (852mm avg) — but also carries the highest disease/pest risk (54.5%).
- **Most farms are loss-making, and it worsens through the season cycle** — this pattern is invisible if you only look at average profit.
- **Crop choice matters as much as season**: Sugarcane stays stable and profitable in every season (~5.45 t/ha, 8–15% loss rate); Wheat is the highest-risk crop everywhere (68–92% loss-making farms) — a cost/pricing issue, not a yield issue.
- **Irrigation method beats season as a driver of water efficiency** — Rainfed farming (5.19 t/1000m³) is nearly 2× more efficient than Flood irrigation (2.67 t/1000m³), the most commonly used method.
- **Disease/pest risk correlates with rainfall (r=0.62) and humidity (r=0.55)**, explaining Kharif's elevated risk.
- All seasonal differences in yield and profit are statistically validated with **one-way ANOVA (p < 0.001)**.

## 🛠️ Tech Stack

- **Python 3**
- **Pandas & NumPy** — data cleaning, transformation, aggregation
- **Matplotlib & Seaborn** — box plots, heatmaps, scatter plots, bar charts
- **SciPy** — statistical hypothesis testing (one-way ANOVA)
- **Jupyter Notebook** — end-to-end documented analysis

## 📂 Repository Structure

```
├── Seasonal_Agriculture_Performance_Analysis.ipynb   # Full analysis notebook
├── seasonal_agriculture_performance_dataset.csv      # Dataset (4,000 farm records)
├── Seasonal_Agriculture_Performance_Analysis_Report.docx  # Written project report
├── VOIS_Major_Project_PPT_Submission.pptx            # Presentation deck
└── README.md
```

## 🧹 Methodology

1. **Data Cleaning** — Missing values in Rainfall, Soil Moisture and Yield imputed using the median for each Season + Crop combination (preserves seasonal/crop patterns instead of flattening them).
2. **Outlier Treatment** — Yield and Water-Use Efficiency capped using the IQR method to remove unrealistic extreme values while retaining all records.
3. **Exploratory Data Analysis** — Seasonal, crop-level, state-level and irrigation-level comparisons via box plots, heatmaps and bar charts.
4. **Statistical Testing** — One-way ANOVA to confirm seasonal differences in yield and profit are statistically significant, not random noise.
5. **Correlation Analysis** — Examined relationships between environmental factors, inputs, and outcomes.

## 🚀 Getting Started

```bash
# Clone the repo
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# Install dependencies
pip install pandas numpy matplotlib seaborn scipy jupyter

# Launch the notebook
jupyter notebook Seasonal_Agriculture_Performance_Analysis.ipynb
```

## 💡 Recommendations

- Protect Kharif-season returns with stronger disease/pest management.
- Re-evaluate Zaid-season cultivation choices given its negative average profit.
- Investigate Wheat's cost structure separately — its losses stem from cost/price, not yield.
- Promote diversification toward stable, low-risk crops like Sugarcane where conditions allow.
- Shift irrigation investment from Flood toward Drip or well-managed Rainfed systems.
- Target disease/pest advisories to high-humidity, high-rainfall periods, especially Kharif.
- Use state-specific benchmarks alongside seasonal ones.

## 🔭 Future Scope

- Extend the analysis to real-time weather and IoT soil-sensor data.
- Build a machine learning model to forecast yield and profit ahead of each season.
- Develop an interactive dashboard for farmers and planners.
- Add a crop-and-season recommendation engine based on location and soil profile.
- Incorporate market-price forecasting.

## 📄 License

This project is for educational purposes as part of the VOIS × AICTE program.

## 🙋 Author
  MR Vaibhav Deepak Mane 

**[Your Name]**
[Your College Name]
[Your LinkedIn / Portfolio Link]
