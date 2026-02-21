# Used Car Price Analysis

## Overview

Analysis of 426K used car listings to identify key price drivers for a used car dealership. Built using the CRISP-DM framework with regression modeling.

## Business Goal

Understand what factors make a car more or less expensive to help a dealership optimize inventory and pricing.

## Dataset

- **Source**: Kaggle used car listings
- **Size**: 426,880 records → ~370K after cleaning
- **Features**: year, manufacturer, condition, fuel, odometer, transmission, type, etc.

## Methodology

1. **Data Cleaning**: Filtered unrealistic prices/years, handled missing values
2. **Feature Engineering**: Created vehicle_age, log-transformed odometer
3. **Modeling**: Tested Linear, Ridge, and Lasso regression with cross-validation
4. **Best Model**: Ridge Regression (R² ≈ 0.61, RMSE ≈ $8,900)

## Key Findings

### Top Price Drivers (in order of importance):
1. **Vehicle Age** - Newer = higher price
2. **Odometer** - Lower mileage = higher price  
3. **Vehicle Type** - Trucks/pickups hold value best
4. **Fuel Type** - Diesel commands premium
5. **Condition** - Excellent/like new adds 20-40%
6. **Title Status** - Clean titles essential

## Recommendations for Dealerships

✅ **Stock**: 1-5 year old vehicles with <60K miles  
✅ **Prioritize**: Trucks, pickups, SUVs (especially diesel)  
✅ **Focus on**: Toyota, Ford, Chevrolet trucks  
✅ **Avoid**: High mileage, salvage titles, poor condition  
✅ **Invest in**: Reconditioning to improve condition ratings  

## Quick Start

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook prompt_II.ipynb
```

## Files

- `prompt_II.ipynb` - Complete analysis notebook
- `data/vehicles.csv` - Dataset
- `notebook_answers.txt` - Summary findings

## Model Performance

| Model | RMSE | R² |
|-------|------|-----|
| Linear Regression | $9,000 | 0.60 |
| **Ridge Regression** | **$8,900** | **0.61** |
| Lasso Regression | $8,950 | 0.60 |

---

**Key Takeaway**: Vehicle age and mileage are the strongest predictors. Focus on acquiring newer, low-mileage trucks with clean titles for best margins.
