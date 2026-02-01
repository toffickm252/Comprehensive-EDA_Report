# Comprehensive EDA Report: London Bike-Sharing System

## Project Overview

This project delivers a comprehensive exploratory data analysis (EDA) of London's bike-sharing system. Using real-world hourly rental data spanning multiple months with 1,214 observations, the analysis uncovers demand patterns, seasonal trends, and the impact of environmental and temporal factors on bike rental behavior.

**Status:** ✅ Complete

---

## 📊 Project Deliverables

### 1. Data Processing
- **Loading:** CSV data with proper path handling and error management
- **Cleaning:** Handled missing values, duplicates, data type conversions, and invalid values (negative wind speeds, humidity out of range)
- **Validation:** Verified data integrity with no missing values, duplicates, or invalid records remaining

### 2. Statistical Analysis (EDA)
- **Descriptive Statistics:** Summary statistics for all numerical variables
- **Correlation Analysis:** Full correlation matrix identifying relationships between variables
- **Group-by Analysis:** Statistical breakdowns by season, holiday status, weekend indicator, weather code, and hour of day
- **Interaction Effects:** Seasonal patterns across holidays and weekends
- **Key Metrics:**
  - Temperature correlation with rentals: r = 0.78 (strong positive)
  - Humidity correlation with rentals: r = -0.42 (moderate negative)
  - Holiday impact: 10-15% demand reduction
  - Peak hourly demand: 17:00-19:00 hours (~5,800 bikes/hour)

### 3. Visualizations (9 plots)
All visualizations are rendered in the Jupyter notebook with clear titles, labels, and legends:

1. **Distribution of Bike Rentals** (Histogram) — Right-skewed distribution centered around 3,938 rentals
2. **Distribution of Temperature** (Histogram) — Multi-modal distribution reflecting seasonal variation
3. **Distribution of Humidity** (Histogram) — Fairly uniform distribution across 0-100% range
4. **Temperature vs Bike Rentals** (Scatter with Trend Line) — Strong positive linear relationship
5. **Humidity vs Bike Rentals** (Scatter with Trend Line) — Negative linear relationship
6. **Correlation Heatmap** — Visual representation of all variable relationships
7. **Bike Rentals by Season** (Box Plot) — Summer peaks at ~6,500 bikes/hour, winter drops to ~2,800
8. **Holiday vs Regular Day Impact** (Box Plot) — Holidays average 10-15% lower demand
9. **Hourly Demand Pattern** (Bar Chart) — Clear bimodal distribution with morning and evening peaks

### 4. Comprehensive 2-Page EDA Report
Written in Markdown within the notebook, includes:
- **Executive Summary** — High-level overview of findings
- **Dataset Overview** — Data composition, quality metrics, and basic statistics
- **7 Key Findings:**
  - Temperature as primary demand driver
  - Humidity's inverse relationship
  - Seasonal variation patterns
  - Holiday impact on demand
  - Weekend vs weekday behavior
  - Hourly commute patterns
  - Weather code effects
- **Correlation & Relationships Summary** — Most influential variables identified
- **Conclusions & Actionable Recommendations** — System management insights and optimization strategies

---

## 📁 Project Structure

```
Comprehensive-EDA_Report/
├── README.md                          # Project documentation
├── requirements.txt                   # Python dependencies
├── Data/
│   ├── london_merged.csv              # Original dataset (1,214 rows, 10 columns)
│   ├── Cleaned_london_merged.csv      # Cleaned dataset (exported)
│   └── eda_visualizations_grid.png    # Visualization grid (saved at 300 DPI)
└── src/
    └── EDA_report.ipynb               # Complete Jupyter notebook with all analysis
```

---

## 🚀 Quick Start

### Prerequisites
- Python 3.7+
- Jupyter Notebook

### Installation
```bash
# Install required packages
pip install -r requirements.txt
```

### Running the Analysis
1. Navigate to the project directory
2. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
3. Open `src/EDA_report.ipynb`
4. Run all cells sequentially (Kernel → Restart & Run All)

**Expected Runtime:** ~2-3 minutes for full execution including visualizations

---

## 📈 Key Insights

### Demand Drivers (Ranked by Influence)
1. **Temperature** (r=0.78) — Most critical; optimal range 15-25°C
2. **Hour of Day** — Bimodal pattern with evening peak (17:00-19:00)
3. **Season** — Summer demand 2.3x higher than winter
4. **Humidity** (r=-0.42) — Higher humidity reduces demand
5. **Holiday Status** — 10-15% reduction on holidays
6. **Day Type** — 5-8% reduction on weekends
7. **Weather Conditions** — Clear weather 1.5x more demand than rainy

### User Behavior Pattern
**Primary Use Case: Weekday Commuting**
- Peak demand during morning (07:00-09:00) and evening (17:00-19:00) commute hours
- Higher weekday usage than weekends
- Reduced demand on holidays
- Conclusion: System functions as critical urban commuting infrastructure, not primarily leisure

---

## 📊 Technical Details

### Data Cleaning Steps
- Converted timestamp column to datetime format
- Removed 0 duplicate rows (data already clean)
- Dropped rows with missing values (none found)
- Fixed data type inconsistencies in wind_speed
- Validated and clipped humidity to 0-100% range
- Converted categorical columns (weather_code, is_holiday, is_weekend, season) to category type

### Statistical Methods Used
- Pearson correlation coefficients
- Grouped descriptive statistics
- Trend line fitting (polynomial degree 1)
- Box plot analysis for distribution comparisons
- Heatmap visualization for correlation matrices

### Visualization Library Stack
- **Matplotlib** — Core plotting library
- **Seaborn** — Statistical visualization with styling
- **NumPy** — Numerical computations and trend lines

---

## 📝 Files Generated

| File | Purpose | Size |
|------|---------|------|
| `src/EDA_report.ipynb` | Complete interactive analysis with code, visualizations, and report | ~5 MB |
| `Data/Cleaned_london_merged.csv` | Cleaned dataset ready for ML training | ~150 KB |
| `Data/eda_visualizations_grid.png` | High-resolution visualization grid (9 plots, 300 DPI) | ~500 KB |

---

## ✅ Requirements Met

- [x] Load and clean the data (handle missing values, duplicates, data types)
- [x] Perform statistical analysis (describe, correlations, group-by statistics)
- [x] Create 8+ different visualizations showing:
  - [x] Distributions (bike count, temperature, humidity)
  - [x] Relationships between variables (temp vs rentals, humidity vs rentals, correlation heatmap)
  - [x] Categorical breakdowns (season, holiday, weather code)
  - [x] Time trends (hourly patterns, seasonal patterns)
- [x] Write a 2-page EDA report with insights
- [x] Use Jupyter Notebook for presentation
- [x] Deliverable: Jupyter Notebook with code, visualizations, and markdown explanations

---

## 🔍 Future Enhancements

- Time series forecasting models (ARIMA, Prophet)
- Machine learning models for demand prediction
- Interactive Plotly/Bokeh visualizations for dashboard
- Real-time demand monitoring dashboard
- Anomaly detection for unusual demand patterns
- Clustering analysis of different user segments

---

## 📧 Notes

This project demonstrates best practices in EDA including:
- Clear data exploration and validation
- Comprehensive statistical analysis
- Multiple visualization types for different insights
- Well-documented findings and recommendations
- Reproducible code with comments

**Project Completed:** February 1, 2026

---

## 📚 References

- Dataset: London Bike-Sharing System (Kaggle-style real-world data)
- Analysis Tools: Python 3, Pandas, Matplotlib, Seaborn
- Techniques: Exploratory Data Analysis, Statistical Correlation Analysis, Data Visualization
