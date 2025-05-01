# Warehouse-Inventory-Optimization---EDA
Warehouse inventory analysis identifying demand patterns, seasonal trends, and product correlations. Contains Python EDA, Jupyter notebooks, and actionable insights for inventory optimization.  🔑 Keywords: inventory optimization, sales analysis, demand forecasting, Python EDA

# Warehouse Inventory Optimization - EDA

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🔍 Project Overview
Analysis of warehouse inventory patterns to optimize stock levels and reduce carrying costs. Identifies:
- High-risk SKUs with demand variability (CV >7)
- Seasonal trends (41% winter sales dominance)
- Product bundling opportunities (r >0.8)

![Seasonal Sales Distribution](reports/figures/seasonal_sales.png)

## 📁 Dataset
`Sales_Transactions_Dataset_Weekly.csv`  
- 811 products with 52-week sales history
- Columns: `Product_Code`, `W0-W51`, Normalized features

## 🚀 Key Findings
1. **Critical Stock Risks**: 15% of SKUs show extreme demand variability (CV >5)
2. **Winter Focus**: 41% of annual sales occur December-February
3. **Top Correlations**: P215-P457 (r=0.81) ideal for bundling

## ⚙️ Usage
```bash
# Clone repo
git clone https://github.com/KaluOkorie/Warehouse-Inventory-Optimization.git

# Install dependencies
pip install -r requirements.txt

# Run analysis
jupyter notebook notebooks/02_eda_analysis.ipynb
