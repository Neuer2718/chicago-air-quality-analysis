# Chicago Air Quality Analysis

This repository contains a data analysis project for **CSCI 503 – Programming Principles in Python (NIU)**.  
The goal is to explore how air pollution levels in Chicago relate to temperature and seasons.

The analysis was implemented in **Google Colab** and saved here as a Jupyter notebook.

---

## Dataset

- Source: Chicago Air Quality / Pollution dataset (historical data for Chicago) [web:62].
- File used: `chicago-air-pollution.csv`
- Main columns:
  - `city` – city name (filtered to Chicago)
  - `date` – date of observation
  - `tmpd` – daily mean temperature
  - `dptp` – dew point temperature
  - `pm25tmean2` – mean PM2.5 concentration
  - `pm10tmean2` – mean PM10 concentration
  - `o3tmean2` – mean ozone (O₃) concentration
  - `no2tmean2` – mean nitrogen dioxide (NO₂) concentration

---

## Tools

- Python (via **Google Colab**)
- Libraries:
  - `pandas`, `numpy`
  - `matplotlib`, `seaborn`
  - `scipy.stats`

---

## Notebook

- `chicago_aqi_analysis.ipynb` – main analysis notebook  
  - Can be opened directly on GitHub (static view) [web:113]  
  - Or run in Colab via the “Open in Colab” badge (if enabled when saving from Colab) [web:133][web:137]

The notebook includes:

1. Data loading and cleaning
2. A `PollutionAnalyzer` class for summary statistics and grouping
3. Exploratory plots:
   - Histograms for PM2.5, PM10, O₃, NO₂
   - Time series and 30‑day rolling mean of PM2.5
   - Seasonal bar charts by pollutant
   - Scatter plots of temperature vs each pollutant
4. Correlation matrix and Pearson correlation tests

---

## Key Findings (Summary)

- **Seasonality:** Ozone shows the strongest seasonal pattern, with much higher average levels in summer than in winter, consistent with temperature‑driven ozone formation [web:92][web:98].  
- **Temperature relationships:** Temperature is strongly positively associated with ozone (r ≈ 0.64). PM10 has a moderate positive correlation with temperature (r ≈ 0.32), while NO₂ shows almost no linear association (r ≈ −0.03).  
- **Trends over time:** Yearly averages suggest that PM10 has declined over the period studied (from low 40s to high 20s), while PM2.5 and NO₂ show mild downward trends and ozone remains relatively stable.

---

## How to Run

1. Clone the repo or download the notebook.
2. Open `chicago_aqi_analysis.ipynb` in Jupyter, VS Code, or Google Colab.
3. Ensure the CSV file `chicago-air-pollution.csv` is in the same folder.
4. Install dependencies (for local runs):

```bash
pip install pandas numpy matplotlib seaborn scipy
```

Then run all cells from top to bottom.
