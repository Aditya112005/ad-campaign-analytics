#  Ad Campaign Analytics

This project analyzes April ad campaign data (~15,000 records) to uncover trends in engagement, conversions, and ROI. It answers 20 key business questions using Python, visualizations, and machine learning to guide smarter ad spending.

---

##  Dataset

- ~15,000 records with:
  - `campaign`, `placement`, `banner_size`
  - `revenue`, `cost`, `clicks`, `user_enga`, `post_click`
- Tracks both **pre-click engagement** and **post-click conversions**

---

##  Goals

- Identify top-performing placements, banners, and campaigns  
- Understand pre/post-click user behavior  
- Recommend ROI-driven ad optimizations  

---

##  KPIs Computed

- **CTR** (Click Through Rate)  
- **CPC** (Cost Per Click)  
- **Conversion Rate**  
- **ROI** (Return on Investment)  
- **Revenue per Impression**

---

##  Tools & Technologies

- Python: `pandas`, `matplotlib`, `seaborn`
- Jupyter Notebook  
- Git & GitHub  
- PowerPoint (presentation)

---

## Machine Learning: Post-Click Conversion Prediction

Used **Random Forest Classifier** to predict whether a user will convert after clicking an ad.

### Model Highlights:
- **Features**: campaign metadata, engagement metrics, CPC, ROI  
- **Target**: `post_click` (binary: 1 = converted, 0 = not)  
- **Accuracy**: ~87%, balanced **F1 Score**  
- **Outputs**:
  - `post_click_rf_model.joblib`: trained model  
  - `feature_importance.csv`: top predictors
 Enables **conversion probability scoring** for better targeting and budget allocation.

---

## Key Insights

-  **160x600** banners → highest conversion rate  
-  **Campaign 0** → ROI > 1.1; Campaigns 1 & 2 underperform  
-  **Placements 2, 4, 1** → Highest CPC (~0.075–0.078)  
-  **Placement 5** → Lowest CPC, highly cost-effective  
-  **Weekdays** outperform weekends in both clicks and conversions  
-  Some campaigns spend high but yield zero conversions  
- Top predictive ML features: **CPC**, **ROI**, **Clicks**, **Campaign ID**

---

## 📎 Files Included

- `campaign_analysis.ipynb` – Main analysis notebook  
- `post_click_rf_model.joblib` – Trained ML model  
- `feature_importance.csv` – Ranked ML features  
- `conversion_rate_banner.png` – Visual output
- `Ad-Campaign-Analytics-and-ML-Based-Conversion-Prediction.pdf`-presentation
- `online_advertising_performance_data`-data on which the analysis was performed

---

## 💡 Author

*Aditya Kumar Singh*
