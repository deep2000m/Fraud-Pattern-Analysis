# 💳 Ad-Hoc Fraud Pattern Analysis Using Synthetic Transaction Data

# 📘 Project Overview

This project explores transactional fraud using synthetic financial data to simulate real-world customer behavior. The analysis was conducted as an ad-hoc investigation into fraud concentration by merchant, transaction type, demographic segment, and geographic context.

The objective was to identify key behavioral and transactional flags that may indicate fraud risk, and to provide actionable insights for merchant compliance, card issuance policy, and risk operations.


---

# 📊 Dashboard Highlights



Built in Power BI, the dashboard enables dynamic exploration of fraud patterns via:

🛒 Merchant-level fraud concentration

💳 Card type-specific fraud breakdown

👤 Demographic risk segments (age, employment)

🗺 Fraud hotspots by location and category

💰 High-value transaction analysis


> 🎛 Interactivity allows filtering by transaction size, merchant risk level, and customer profile.


---

# 🔍 Key Insights

1. Fraud Prevalence

Approximately 51% of all recorded transactions exhibit characteristics aligned with fraud patterns 

2. Merchant Risk

25% of merchants were flagged as high-risk, often linked to transactions exceeding ₹5,000.

3. Total Fraud Exposure

The cumulative fraud impact reached approximately ₹25.2 million.

4. Card Usage Patterns

Discover cards were most frequently linked to fraud.
Visa was commonly used at gas stations, which ranked as the top location for fraud.

5. Demographic Trends

Individuals aged 25–50 were most represented in fraud cases, despite weak correlation (r = -0.005).

6. Unexpected Merchant Types

Grocery stores — typically low-risk — showed surprisingly high fraud rates, warranting further investigation.


—
# ❓ Exploratory Questions

## 1. What is the relationship between card type and fraudulent transactions?

Discover and Visa cards were most commonly associated with fraudulent transactions in the dataset.

- *Discover* accounted for the *highest number of fraud cases*, suggesting possible vulnerabilities in either user verification, transaction monitoring, or popularity among fraudsters.
- *Visa* was the second most common, especially in *gas station transactions*, where fraud concentration was high.
- Other card types showed significantly lower fraud density, possibly due to lower usage volume or stronger fraud prevention protocols.

> 🔍 Conclusion: Card-level fraud detection systems and merchant verification mechanisms need strengthening — especially for Discover and Visa at high-risk locations.

## 2. Why are grocery stores and gas stations the top fraud-prone locations?

These two merchant categories accounted for the *majority of fraudulent transactions*.

Possible reasons include:

- *High transaction volume*: Both categories see frequent, low-to-mid value transactions, making them attractive for fraudsters aiming to avoid detection.
- *Self-service environments: Gas stations, in particular, often involve **card-not-present* or *contactless* payments, which have higher fraud risk.
- *Less stringent verification*: Grocery stores may prioritize speed over security at checkout, enabling quick swipe or tap frauds.
- *Skimming devices*: Gas pumps are common targets for installing skimmers that steal card data.

> 🔍 Conclusion: These locations require *enhanced fraud monitoring*, better terminal protection, and possibly AI-driven flagging based on usage patterns.

## 3. Does transaction amount influence fraud risk?

While fraud is spread across all amount ranges, transactions over *$5,000* were disproportionately associated with high-risk merchants.

- *High-value transactions* accounted for a significant portion of the total fraud amount — $25.2M.
- Fraudsters may be targeting high-ticket purchases intentionally to maximize gain per transaction.
- However, low-value fraud also existed, likely intended to bypass detection systems.

> 🔍 Conclusion: Fraud detection should not rely solely on amount thresholds. Both *low-amount stealth fraud* and *high-amount burst fraud* exist, requiring *multi-dimensional detection models*.

___

# 📌 Recommendations

1. Merchant Risk Oversight

Prioritize audits and compliance reviews for flagged merchants to curb recurrent fraud.

2. Stricter Card Issuance Protocols

Implement enhanced identity and financial screening for new cardholders to limit exposure.

3. Location-Specific Monitoring

Focus fraud investigation efforts on gas stations and grocery merchants, which emerged as major fraud hotspots.


---

# 📊 Detailed Visual Analysis

## C1. Merchant-Level Risk Map
25 merchants were flagged high-risk due to repeated fraud and high transaction values (>$5,000).




---

## C2. Card Types & Location-Based Fraud
Discover and Visa dominate fraud cases. Gas stations lead as the most targeted location.





---

## C3. Age Categories & Risk
Working-age individuals (25–50) are most represented in fraud cases, though the correlation is minimal.



---


# 💼 Tools & Technology

Power BI – Visualization, dashboard design, filtering logic

Excel – Data preparation and formatting

DAX – Custom segmentation, fraud rate measures

Synthetic Transaction Data – Simulated to reflect real-world financial behavior patterns

—

# Key formulae and calculation(most relevant ones)

**Fraud Amount =
CALCULATE(
    SUM(synthetic_financial_data[amount]),
    synthetic_financial_data[is_fraudulent] = 1
)**

**Possible Fraud Merchants = 
DIVIDE(
    CALCULATE(
        COUNTROWS(synthetic_financial_data),
        synthetic_financial_data[fraudulent merchant] = "High Risk"
    ),
    COUNTROWS(synthetic_financial_data),
    0
)**


---

# 🧠 Analytical Approach

Fraud segmentation by merchant, card type, age, and transaction value

Threshold logic for “high-risk” merchant classification (e.g., high-value, repeat fraud)

Use of correlation analysis to identify weak but suggestive trends

Categorical analysis of merchant types against fraud counts

---

# ✅ Summary

This project demonstrates the use of synthetic data analytics to simulate a real-world fraud detection use case. The output enables financial stakeholders to identify high-risk merchants, risky transaction patterns, and targetable fraud hotspots, making it well-suited for roles in fraud analytics, risk reporting, or financial BI.

____________________________

🚀 How to Use

1. Download the .pbix file from this repository.
2. Open it using Power BI Desktop (free from Microsoft).
3. Explore the dashboard
4. No installation or code setup is required — just open and explore.
> 💡 Tip: Use “Focus Mode” in Power BI to expand visuals for deeper analysis.


# 📬 Contact

Created by: Deepak Das
📧  deepakdas909@gmail.com
🔗 Portfolio
💼 LinkedIn
