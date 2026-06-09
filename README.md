# African Sovereign Analysis

## 📋 Project Overview

**Research Question:** Where should patient capital (long-term, risk-tolerant investors) be deployed across African markets in 2026?

**Thesis:** Despite Kenya's reputation as East Africa's financial hub, data suggests Ghana presents a superior risk-adjusted opportunity for patient capital deployment in 2026.

**Author:** Mark Wema  
**Date:** 4th June 2026  
**Analysis Universe:** 5 African markets (Kenya, Ghana, Nigeria, South Africa, Egypt)

---

## 🎯 Key Findings Summary

### Kenya vs Ghana Comparison (Head-to-Head)

| Metric | Kenya | Ghana | Winner |
|--------|-------|-------|--------|
| **GDP Growth** | 4.73% | 5.59% | 🇬🇭 Ghana |
| **Inflation** | 4.49% | 22.85% | 🇰🇪 Kenya |
| **FDI (% of GDP)** | 0.39% | 2.15% | 🇬🇭 Ghana |
| **GDP per Capita (USD)** | $2,132 | $2,391 | 🇬🇭 Ghana |
| **Government Debt (% GDP)** | 70.2% | 84.9% | 🇰🇪 Kenya |
| **Consumer Momentum (Trends)** | 14.2/25 | 16.8/25 | 🇬🇭 Ghana |

**Initial Score:** Kenya 2 - Ghana 4  
**Conclusion:** "Ghana ahead early - thesis has legs"

---

## 📁 Repository Structure & File Documentation

### 1. **African_Sovereign_Analysis.ipynb**
**Type:** Jupyter Notebook (Primary Analysis)  
**Size:** 82.7 KB  
**Status:** ✅ Complete Analysis Notebook

#### Contents:
- **Data Collection Pipeline:**
  - World Bank API integration (13 indicators)
  - IMF WEO 2024 estimates (macroeconomic data)
  - Google Trends API (consumer/business signals)
  
- **Scoring Model:**
  - Macro Stability (30%): Inflation, debt, current account
  - Growth Trajectory (25%): GDP growth, FDI, investment
  - Digital Economy (20%): Mobile & internet penetration
  - Market Maturity (15%): GDP per capita, literacy
  - Consumer Momentum (10%): Google Trends signals
  
- **Key Analyses:**
  - Comparative country scoring
  - Sensitivity analysis (±10% to ±20%)
  - Peer country analysis
  - Investment thesis validation

#### World Bank Indicators Extracted:
```
✓ GDP (USD)                    - Market size
✓ GDP Growth (%)               - Growth trajectory
✓ GDP per Capita (USD)         - Development level
✓ Inflation Rate (%)           - Macro stability
✓ Current Account (% GDP)      - External balance
✓ FDI Inflows (% GDP)          - Foreign investor confidence
✓ Gross Investment (% GDP)     - Capital formation
✓ Mobile Phones (per 100)      - Digital infrastructure
✓ Internet Users (%)           - Digital access
✓ Adult Literacy Rate (%)      - Human capital
✓ Life Expectancy (years)      - Development indicator
✓ Government Debt (% GDP)      - Fiscal sustainability
✓ Tax Revenue (% GDP)          - Fiscal capacity
```

#### Google Trends Keywords Monitored:
- Mobile Banking (fintech adoption)
- Online Shopping (consumer growth)
- Business Loan (business activity)
- Property Investment (real estate sector)
- Startup Funding (startup ecosystem)

---

### 2. **ASA_Investment_Memo.docx**
**Type:** Microsoft Word Document  
**Size:** 40.7 KB  
**Purpose:** Executive Summary & Investment Recommendation

#### Likely Contents:
- Executive summary of findings
- Investment thesis
- Risk/opportunity assessment
- Recommended allocation framework
- Key decision drivers for investment committee

---

### 3. **African Sovereign Analysis Dashboard.pbix**
**Type:** Power BI File  
**Size:** 59.7 KB  
**Purpose:** Interactive Visualization & Reporting

#### Dashboard Features (Typical):
- Country comparison matrices
- Scoring breakdown by dimension
- Time-series trends (Google Trends evolution)
- Risk-return scatter plots
- Sensitivity analysis charts
- KPI cards for quick analysis

#### Visualizations Expected:
- Macro Stability Radar Charts (all 5 countries)
- Growth Trajectory Line Charts
- Heatmaps: Score distribution by dimension
- Waterfall Charts: Scoring components
- Comparative dashboards: Kenya vs Ghana focus

---

### 4. **CSV Data Files** (Supporting Datasets)

#### a) **pc_country_scores.csv**
**Type:** Country Scoring Results  
**Purpose:** Final composite scores for all countries

**Expected Schema:**
```
Country,Macro_Stability,Growth_Trajectory,Digital_Economy,Market_Maturity,Consumer_Momentum,Total_Score,Rank
Kenya,X,X,X,X,X,X,X
Ghana,X,X,X,X,X,X,X
Nigeria,X,X,X,X,X,X,X
South Africa,X,X,X,X,X,X,X
Egypt,X,X,X,X,X,X,X
```

---

#### b) **pc_kenya_ghana.csv**
**Type:** Kenya vs Ghana Head-to-Head Comparison  
**Purpose:** Focused comparative analysis

**Expected Schema:**
```
Indicator,Kenya_Value,Ghana_Value,Winner,Margin,Weight_Category
gdp_growth,4.73,5.59,Ghana,0.86,Growth_Trajectory
inflation,4.49,22.85,Kenya,18.36,Macro_Stability
...
```

---

#### c) **pc_macro_indicators.csv**
**Type:** Macroeconomic Data Extract  
**Purpose:** Underlying data for macro stability scoring

**Indicators Likely Included:**
```
Country,GDP_USD,GDP_Growth_Pct,Inflation_Pct,Current_Account_Pct_GDP,Govt_Debt_Pct_GDP,Tax_Revenue_Pct_GDP
Kenya,120.3B,4.73,4.49,-1.29,70.2,X
Ghana,82.3B,5.59,22.85,2.04,84.9,X
Nigeria,252.3B,4.06,33.24,6.82,46.7,N/A
South Africa,401.1B,0.54,4.36,-0.64,73.8,X
Egypt,389.1B,2.40,28.27,-5.69,96.4,X
```

---

#### d) **pc_sensitivity.csv**
**Type:** Sensitivity Analysis Results  
**Purpose:** Stress-test scores with ±10%, ±15%, ±20% shocks

**Expected Schema:**
```
Country,Base_Score,Shock_Minus_20,Shock_Minus_10,Shock_Plus_10,Shock_Plus_20,Volatility_Rank
Kenya,X,X,X,X,X,X
Ghana,X,X,X,X,X,X
...
```

**Purpose:** Validates robustness of conclusions; shows which countries are most sensitive to data changes.

---

## 🔍 Data Sources & Methodology

### Primary Data Sources:
1. **World Bank Open Data API**
   - 13 macroeconomic indicators
   - 5-year historical coverage
   - 25 data points retrieved (5 countries × 5 years)
   
2. **IMF World Economic Outlook 2024**
   - Q1 2026 forward estimates
   - Fills World Bank data gaps
   - Current account, inflation, debt estimates
   
3. **Google Trends API**
   - 5-year search volume trends
   - 5 keyword categories (fintech, consumer, business, real estate, startups)
   - Momentum calculation: 6M recent vs 6M prior

### Data Quality Metrics:
- **World Bank Completeness:** 13/13 indicators (100%)
- **Data Points Retrieved:** 25/25 expected (100%)
- **IMF Fill Rate:** 4/5 countries (80% for debt)
- **Google Trends Success Rate:** 25/25 signals (100%)

---

## 📊 Scoring Model Architecture

### Dimension Weights (Total: 100%)
```
Macro Stability      ███████████████████████████████ 30%
Growth Trajectory    █████████████████████████░░░░░░ 25%
Digital Economy      ████████████████████░░░░░░░░░░░ 20%
Market Maturity      ███████████████░░░░░░░░░░░░░░░░ 15%
Consumer Momentum    ██████████░░░░░░░░░░░░░░░░░░░░░ 10%
```

### Scoring Philosophy:
- **For Patient Capital (5-10 year horizon):**
  - Macro stability matters MORE than current size
  - Growth trajectory matters MORE than current level
  - Capital safety matters MORE than return potential

### Scoring Ranges:
- **Total Score Range:** 0-100 points
- **Macro Stability:** 0-30 points
- **Growth Trajectory:** 0-25 points
- **Digital Economy:** 0-20 points
- **Market Maturity:** 0-15 points
- **Consumer Momentum:** 0-10 points

---

## 🚀 Usage Instructions

### For Analysts:
1. **Review Notebook:** Open `African_Sovereign_Analysis.ipynb` in Jupyter/Colab
2. **Examine Raw Data:** Reference `.csv` files for specific data points
3. **Cross-check Dashboard:** Use `African Sovereign Analysis Dashboard.pbix` in Power BI

### For Decision Makers:
1. **Start with Memo:** Read `ASA_Investment_Memo.docx` for exec summary
2. **Explore Dashboard:** Use Power BI dashboard for interactive analysis
3. **Reference Comparison:** Check `pc_kenya_ghana.csv` for quick KPIs

### For Investors:
1. **Risk Assessment:** Check sensitivity analysis results
2. **Peer Comparison:** Review full country scores in `pc_country_scores.csv`
3. **Thesis Validation:** Review notebook conclusions on Kenya vs Ghana thesis

---

## 💡 Key Insights & Implications

### For Ghana:
✅ **Strengths:**
- Higher FDI inflows (2.15% vs 0.39% for Kenya)
- Stronger GDP growth (5.59% vs 4.73%)
- Higher consumer momentum (Google Trends)
- Better digital infrastructure adoption

⚠️ **Challenges:**
- High inflation (22.85% vs Kenya's 4.49%)
- Higher government debt (84.9% vs 70.2%)
- Currency risk implications

### For Kenya:
✅ **Strengths:**
- Macroeconomic stability (low inflation)
- Manageable debt levels
- Established regional financial hub

⚠️ **Challenges:**
- Lower FDI attraction
- Slower GDP growth
- Weaker consumer momentum

### Investment Recommendation:
**Ghana presents superior risk-adjusted opportunity** despite inflation concerns, supported by:
- Foreign investor confidence (FDI metrics)
- Growth trajectory alignment
- Consumer and business activity momentum
- Digital economy development

---

## 🔧 Technical Stack

| Component | Technology |
|-----------|------------|
| Analysis | Python 3.x, Pandas, NumPy |
| Data APIs | World Bank API, Google Trends API |
| Visualization | Power BI, Matplotlib |
| Environment | Google Colab (cloud execution) |
| Export | CSV, DOCX, PBIX formats |

---

## 📈 Countries Analyzed

| Country | Region | WB Code | IMF Code |
|---------|--------|---------|----------|
| Kenya | East Africa | KE | KEN |
| Ghana | West Africa | GH | GHA |
| Nigeria | West Africa | NG | NGA |
| South Africa | Southern Africa | ZA | ZAF |
| Egypt | North Africa | EG | EGY |

---

## 🎓 Project Methodology

### Phase 1: Data Collection ✓
- Extract World Bank indicators
- Gather IMF forward estimates
- Capture Google Trends momentum

### Phase 2: Data Blending ✓
- Merge multi-source data
- Fill gaps (IMF → WB)
- Normalize and validate

### Phase 3: Scoring ✓
- Build composite index
- Weight dimensions
- Rank countries

### Phase 4: Sensitivity Analysis ✓
- Stress-test with ±10%, ±15%, ±20% shocks
- Validate thesis robustness
- Identify tail risks

### Phase 5: Reporting ✓
- Executive memo
- Interactive dashboard
- Detailed analysis notebook
- Supporting data exports

---

## 📞 Contact & Attribution

**Analysis by:** Mark Wema  
**Analysis Date:** 4th June 2026  
**Last Updated:** 2026-06-09

---

## 📝 License & Disclaimer

This analysis is based on publicly available data from:
- World Bank Open Data
- IMF World Economic Outlook
- Google Trends

For professional investment decisions, validate findings with licensed financial advisors and conduct additional due diligence specific to your investment mandate.

---

## 🔗 Quick Links

- **Notebook:** [African_Sovereign_Analysis.ipynb](./African_Sovereign_Analysis.ipynb)
- **Dashboard:** [African Sovereign Analysis Dashboard.pbix](./African%20Sovereign%20Analysis%20Dashboard.pbix)
- **Memo:** [ASA_Investment_Memo.docx](./ASA_Investment_Memo.docx)
- **Country Scores:** [pc_country_scores.csv](./pc_country_scores.csv)
- **Comparison Data:** [pc_kenya_ghana.csv](./pc_kenya_ghana.csv)

---

**Analysis Type:** Quantitative Comparative Analysis | **Methodology:** Weighted Scoring Model | **Data Vintage:** Q1 2026
