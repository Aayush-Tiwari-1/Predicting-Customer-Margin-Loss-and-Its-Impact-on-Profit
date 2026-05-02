# 📊 Predicting Customer Margin Loss in Retail

### Identifying Profit Leakage through Machine Learning and Behavioral Segmentation
**Aayush Pradeep Tiwari**

---

## 🚀 Project Overview
In contemporary retail, aggregate revenue growth often conceals systemic margin erosion. This project develops a predictive analytics framework to identify individual transactions at risk of **margin loss**—events where total fulfillment costs (COGS, shipping, and returns) exceed realized revenue. 

Using a dataset of **10,000 retail transactions**, this study validates that margin erosion is a predictable outcome of structural drivers, primarily **Cost Burden** and aggressive discounting on high-COGS products.

## 🛠️ Tech Stack
*   **Language:** Python
*   **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, LightGBM, Statsmodels
*   **Explainability:** SHAP (SHapley Additive exPlanations)
*   **Data Visualization:** Matplotlib, Seaborn

## 📈 Key Findings & EDA
*   **Exploratory Data Analysis:** Comprehensive EDA was conducted, utilizing bar charts to analyze structural cost distributions and customer segment performance.
*   **The "Cost Burden" Dominance:** Statistical testing (Logit $p=1.05e-132$) confirmed that **Cost Burden** (Total Cost / Sales Revenue) is the single most powerful predictor of margin loss.
*   **Segment Paradox:** The study revealed that a buyer's label (e.g., "Premium Loyal" vs. "At-Risk") is a poor discriminator of profit, with only a 1.3 percentage point spread in loss rates across segments. 
*   **Death Spiral Risk Matrix:** Identifies the "danger zone" where high COGS and deep discounts (>25%) result in a 95%+ loss rate.
*   **K-Means Personas:** Segmented transactions into four actionable behavioral clusters, including "Deep-Discount Loss Leaders" who generate a -23.0% average pocket margin.

## 🤖 Model Performance
Six classifiers were benchmarked to find the optimal balance between catching profit leaks (Recall) and minimizing false alarms (Precision).

| Model | F1-Score | Recall | Precision |
| :--- | :--- | :--- | :--- |
| **XGBoost (Selected)** | **77.5%** | **76.7%** | **78.3%** |
| Decision Tree | 77.4% | 81.0% | 74.1% |
| LightGBM | 77.3% | 76.8% | 77.8% |

> **Business Impact:** Implementing an AI-governed 15% discount cap on high-risk transactions predicted by the model resulted in a **+12.8% annualized profit uplift** (₹1.49M) and a 3.1% increase in gross revenue.

## 📂 Project Structure
1.  **Phase 1: EDA** – Characterizing margin loss distribution across 19 features using descriptive statistics and bar charts.
2.  **Phase 2: Risk Anatomy** – Isolating structural drivers through Logit coefficients and SHAP.
3.  **Phase 3: K-Means Clustering** – Visualizing behavioral personas in the risk space.
4.  **Phase 4: ML Development** – Training and comparing six ensemble and linear classifiers.
5.  **Phase 5: Prescriptive Simulation** – A "live" CRM governance mockup demonstrating real-world ROI.

## 💡 How to Use
```bash
git clone [https://github.com/yourusername/retail-margin-loss-prediction.git](https://github.com/yourusername/retail-margin-loss-prediction.git)
cd retail-margin-loss-prediction
pip install -r requirements.txt
