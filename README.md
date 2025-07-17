#  Ad Campaign Analytics

This project analyzes April ad campaign performance data to extract insights into user engagement, conversion behavior, and ROI. It answers 20 business-critical questions using Python and visualizes patterns in revenue, clicks, cost, and placements.

---

##  Dataset

- Over 15,000 records
- Columns include:
  - `campaign`, `placement`, `banner_size`
  - `revenue`, `cost`, `clicks`, `user_enga`, `post_click`
- Tracks both **pre-click engagement** and **post-click conversions**

---

## 🎯 Objectives

- Understand which placements and banners perform best
- Analyze conversion trends across campaigns and channels
- Recommend data-backed marketing actions

---

## 📈 KPIs Computed

- Click Through Rate (CTR)
- Cost Per Click (CPC)
- Conversion Rate
- Return on Investment (ROI)
- Revenue per Impression

---

## 🔍 Tools & Technologies

- Python (Pandas, Matplotlib, Seaborn)
- Jupyter Notebook
- PowerPoint (for presentation)
- Git & GitHub

---

## 🤖 Machine Learning: Post-Click Conversion Prediction

To enhance business decision-making, a supervised ML model was trained to **predict post-click conversions** — helping marketers allocate ad spend more intelligently.

### 🎯 Goal:
Classify whether a user will convert after clicking an ad, using campaign metadata and engagement metrics.

### 🛠️ Model:
- **Algorithm**: Random Forest Classifier
- **Features Used**:
  - Encoded: `campaign`, `placement`, `banner_size`
  - Numeric: `clicks`, `cost`, `revenue`, `user_enga`, `CPC`, `ROI`
- **Target**: `post_click` (binary: 1 = converted, 0 = not converted)

### 📊 Performance:
- **Accuracy**: ~87% on test data
- **F1 Score**: Balanced to account for class imbalance
- **ROC-AUC Score**: Evaluates overall classifier power

### 📌 Additional Outputs:
- `post_click_rf_model.joblib`: Trained model saved for reuse
- `feature_importance.csv`: Ranked features by contribution to prediction

This model enables **data-driven retargeting**, helping businesses focus on segments most likely to convert.

---

## 📊 Key Insights

- 🔼 **High CPC Placements**:
  - Encoded placements **2, 4, and 1** had the **highest average CPC** (~0.075–0.078).
  - Indicates costly ad spaces—only worth investing in if they yield high ROI or conversions.
  
- 🔽 **Low CPC Placement**:
  - Encoded placement **5** showed the **lowest CPC**, making it a cost-effective channel worth deeper analysis.

- 💰 **Top Performing Campaign**:
  - Encoded **Campaign 0** had an **ROI > 1.1**, generating strong returns.
  - Campaigns 1 and 2 had lower ROI and may need optimization.

- 📐 **Best Banner Size**:
  - **160x600** banners had the **highest conversion rate**, confirming their effectiveness.

- 📅 **Timing Matters**:
  - Weekday campaigns showed **better performance** in both **clicks** and **post-click conversions** than weekends.

- ⚠️ **Optimization Opportunity**:
  - Some campaigns incurred **high costs with zero conversions**—candidates for elimination or redesign.

- 🤖 **ML Model Insights**:
  - **Random Forest** classifier achieved an **F1 Score of ~87%**.
  - Top predictive features: **CPC, ROI, Clicks, Campaign ID**.
  - Enables **conversion probability scoring** for smarter targeting and ad spend optimization.

---
