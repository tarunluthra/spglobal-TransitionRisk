# Transition Risk Analysis

This repository analyzes **climate transition risks** for companies using S&P Global data. It includes code for emissions projection, carbon pricing cost estimation, abatement modeling, and financial trade-off analysis. The results help evaluate corporate exposure to carbon pricing and identify cost-effective decarbonization strategies.

---

## 📦 Repository Structure

| File / Folder                | Description |
|-----------------------------|-------------|
| `climatetransitionriskTL.py`| Core logic for emissions projection, carbon pricing, and abatement modeling. |
| `spworkStoryboard.ipynb`    | Visualization notebook for generating graphs, insights, and scenario comparisons. |
| `*.csv`                     | Output files from the analysis: projected emissions, costs, and results per company. |
| `README.md`                 | This file. |
| `S&P Global S1 Transition Risk Data.xlsx` | (not included) Input Excel file with raw emissions, targets, and pricing data. |

---

## 🎯 Objective

Estimate future Scope 1 and Scope 2 emissions (2025–2050), evaluate carbon pricing exposure under low/medium/high scenarios, and compare those costs to abatement investments. The goal is to guide strategic decisions by:
- Quantifying emission paths under different reduction strategies.
- Calculating cumulative carbon cost exposure.
- Identifying companies or sectors where abatement is financially preferable.

---

## 🔧 Key Functionalities

### 1. Data Loading and Cleaning
- Reads emissions, targets, carbon prices, and abatement tables from Excel.
- Standardizes column names and fills missing values (e.g., mean or median imputation).
- Corrects regional naming mismatches and aligns year formats.

### 2. Emissions Projection
- Projects emissions under **absolute** or **intensity-based** targets.
- Supports static or growth-based production assumptions.
- Incorporates **interpolation methods**: `linear`, `exponential`, and `S-curve`.

### 3. Carbon Pricing Cost Estimation
- Multiplies projected emissions by scenario-specific carbon prices.
- Fallbacks to global prices if region-sector-specific prices are missing.
- Aggregates cost exposure by year, region, and company.

### 4. Abatement Modeling
- Matches companies to relevant abatement technologies by sector and region.
- Estimates cost-effective emission reductions.
- Compares total abatement costs to carbon price costs.

### 5. Visual Analysis (`spworkStoryboard.ipynb`)
- Line plots of emissions trajectories.
- Sector-wise stacked area charts.
- Heatmaps of carbon cost intensity by scenario.
- Scatter plots of abatement vs. carbon price costs.
- Boxplots and waterfall charts for company-level insights.

---

## 📊 Example Visuals

- **Emissions by Sector Over Time**
- **Carbon Price Projections by Scenario**
- **Net Benefit of Abatement vs. Paying Carbon Costs**
- **Top Emitters and Cost-Exposed Companies**

---
