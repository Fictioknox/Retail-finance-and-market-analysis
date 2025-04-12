# E-commerce Analytics Project

## Overview
This project analyzes a real-world dataset from the UCI Online Retail repository, containing 397,924 transactions from December 2010 to December 2011. The goal was to derive financial and marketing insights using Python, enhancing customer segmentation, predicting purchase behavior, and optimizing revenue strategies.

---

## Objectives
- Segment customers for targeted marketing using RFM (Recency, Frequency, Monetary) analysis.
- Predict next-day purchases to improve retention.
- Simulate campaign ROI and assess financial impact.
- Identify sales trends, top products, and market basket associations.
- Visualize key metrics like LTV, churn, and price sensitivity.

---

## Methodology

### Data Source
- **Dataset**: UCI Online Retail (397,924 rows, 4,339 unique customers).
- **Preprocessing**: Cleaned missing CustomerIDs, negative quantities; added synthetic `age` and `gender`.

### Tools & Libraries
- **Python**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn, Plotly, MLxtend.
- **Environment**: Google Colab for analysis and visualization.

### Analysis Steps
1. **RFM Segmentation**: Grouped customers by Recency, Frequency, Monetary into "Champions," "Loyal," "At Risk."
2. **Next-Day Purchase Prediction**: Logistic regression model (89.8% accuracy) on real-world transaction data.
3. **LTV Calculation**: Total spend per customer from UCI dataset.
4. **Cohort Retention**: Tracked monthly active customers over time.
5. **Sales Forecasting**: Applied 3-month moving average to monthly revenue.
6. **Top Products**: Identified high-quantity items per segment.
7. **Market Basket Analysis**: Used Apriori algorithm for product associations (e.g., lift 18.12 for lunch boxes).
8. **Trends & Sensitivity**: Analyzed monthly order patterns and price vs. quantity relationships.
9. **Churn Rate**: Calculated 33% of customers inactive >90 days.
10. **Campaign ROI Simulation**: Split data pre/post June 1, 2011, yielding 67.4% revenue increase.

---

## Key Findings

### Customer Insights
- **RFM Segments**: 4,339 customers segmented; "At Risk" dominates bulk purchases (e.g., 80,995 units of "PAPER CRAFT , LITTLE BIRDIE").
- **Next-Day Prediction**: Model achieved 89.8% accuracy, with 10.3% of transactions followed by a next-day purchase.

### Financial Metrics
- **LTV**: Top customer spent $77,183.60; distribution visualized via histogram.
- **Campaign ROI**: Simulated 67.4% revenue growth post-June 2011 ($3.33M pre vs. $5.58M post).
- **Churn Rate**: 33% of customers inactive beyond 90 days.

### Sales & Marketing
- **Sales Forecast**: Peaks in Nov/Dec 2011 (holiday season), smoothed by 3-month moving average.
- **Top Products**: "Champions" favor decorative items (e.g., 6,283 units of "FAIRY CAKE FLANNEL").
- **Market Basket**: Strong associations (e.g., "SPACEBOY LUNCH BOX" → "DOLLY GIRL LUNCH BOX", lift 18.12).
- **Trends**: Highest order volume in November; price sensitivity shows higher quantities at lower prices.

---

## Visualizations
- **RFM Segments**: Bar chart (`rfm_segments.png`).
- **Sales Forecast**: Line plot with moving average (`sales_forecast.png`).
- **Monthly Trends**: Order count by month (`ecommerce_trends.png`).
- **Price Sensitivity**: Scatter plot (`price_sensitivity.png`).
- **Interactive**: LTV histogram and cohort retention line chart via Plotly.

---

## Outputs
- **Excel Files**: 
  - `rfm_analysis.xlsx`: RFM scores and segments.
  - `ltv_analysis.xlsx`: Customer lifetime values.
  - `market_basket_rules.xlsx`: Association rules.
  - `next_day_predictions.xlsx`: Next-day purchase predictions.
- **Charts**: Saved as PNGs for dashboard/report use.

---

## Challenges
- **Streamlit in Colab**: Ngrok tunneling issues prevented live dashboard; shifted to static outputs.
- **Data Scale**: Handled 397k rows efficiently with pandas optimizations.

---

## Recommendations
- **Marketing**: Bundle high-lift items (e.g., lunch boxes) and target "At Risk" with bulk discounts.
- **Financial**: Focus retention on 33% churned customers; leverage 67.4% ROI for campaign planning.
- **Sales**: Boost holiday promotions in Nov/Dec based on trends.

---

## Future Work
- Integrate real campaign data for precise ROI.
- Deploy interactive dashboard with Dash or Streamlit locally.
- Expand with customer demographics beyond synthetic data.

---

## How to Run
1. **Clone Repo**: Download code and assets.
2. **Install Dependencies**: `pip install pandas numpy scikit-learn matplotlib seaborn plotly mlxtend openpyxl`.
3. **Execute**: Run Steps 1-5 in Colab or Jupyter with UCI dataset (`Online_Retail.csv`).
4. **View Outputs**: Check Excel files and PNGs in file explorer.

---

## Credits
- **Dataset**: UCI Machine Learning Repository.
- **Tools**: xAI’s Grok 3 for guidance; Python ecosystem for analysis.
