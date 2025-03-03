# Bank-Churn-Analysis
# 📋 Overview  
Despite the continuous efforts of banks to attract and retain customers, the banking industry faces a persistent challenge in the form of customer churn, leading to financial losses and reduced customer satisfaction. It is advantageous for banks to know what leads a client towards the decision to leave the company.

The aim of this project is to analyze the customer churn rate for bank because it is useful to understand why the customers leave.

# 1. **Overall Churn Rate**   
  - 20.37% of customers churned, while 79.63% did not.
  - This indicates that approximately 1 in 5 customers left the service, which is a significant churn rate and warrants attention.

<br />
<br />
<img src="https://i.imgur.com/lIhogaE.png"/>

---

# 2. **Churn by Gender**  
- Female customers have a higher churn rate (25.07%) compared to male customers (16.46%).
- This suggests that female customers are more likely to leave the service, which could be due to dissatisfaction with the product, service, or other factors.
- **Recommendations:**
  - Investigate why female customers have a higher churn rate and address potential issues such as product suitability, customer service, or pricing.
  - Consider offering tailored promotions or incentives to retain female customers.

<br />
<br />
<img src="https://i.imgur.com/LNBhTOy.png"/>                                        

---

# 3. **Churn by Product Usage**   
  - Customers with 4 products have the highest churn rate, while those with 2 products have the lowest churn rate (7.58%).
  - This indicates that customers with more products are more likely to churn, possibly due to more financial committments, overwhelming complexity, dissatisfaction with bundled services, or poor customer experience when managing multiple products.
- **Recommendation:**
  - Since customers with 2 products have the lowest churn rate, consider promoting 2-product bundles as the "sweet spot" for customer satisfaction.
  - Simplify the experience for customers with multiple products by offering better integration between services or providing a dedicated account manager for high-product customers.
  <img src="https://i.imgur.com/MThqeDu.png"/>

  ---
  
# 4. **Churn by Activity Status**:  
  - Inactive customers have a higher churn rate (65.3%) compared to active customers.
  - This suggests that inactivity is a strong predictor of churn, and efforts should be made to re-engage inactive customers.
- **Recommendations:**
  - Implement re-engagement campaigns for inactive customers, such as personalized emails, special offers, or loyalty programs.
  - Monitor activity levels and proactively reach out to customers who show signs of disengagement.

<br />
<br />

<img src="https://i.imgur.com/h6IVi7C.png"/>

---

# 4. **Churn by Age Group**  

   - Younger customers, particularly those between 20 and 30 years old, exhibit higher churn rates, whereas customers 60 and older churn less frequently.

- **Recommendation:**
  - Introduce tiered pricing plans, student discounts, or promotional bundles tailored to budget-conscious younger users.
  - Offer incentives for long-term commitments.
  - Reward long-term customers with loyalty programs.
  - Ensure customer service teams are trained to address older users’ needs empathetically (e.g., tech support).
 <br />
<br />
<img src="https://i.imgur.com/ERSwElA.png"/>


---

# 5. **Churn by Balance Range**   
   - Customers with lower balances (0-50k) have a higher churn rate (35%), while those with higher balances (>150k) have a lower churn rate.
   - This suggests that customers with lower balances may feel less committed to the service or may be more price-sensitive.
- **Recommendation**
  - Customers with lower balances may be more price-sensitive. Consider offering tiered pricing or loyalty rewards to retain them.
  - Provide financial education or tools to help them manage their accounts better.
 
<br />
<br />
<img src="https://i.imgur.com/sdQDGlK.png"/>

---
# 6. **Churn by Tenure**   
  - Customers with 0-1 years of tenure have the highest churn rate (23%), while those with >5 years of tenure have the lowest churn rate (19.5%).
  - This indicates that newer customers are more likely to churn, possibly due to unmet expectations or lack of loyalty.
- **Recommendation**
  - Newer customers (0-1 years of tenure) are more likely to churn. Improve onboarding processes to set clear expectations and build loyalty early.
  - Offer incentives for long-term commitments, such as discounts for annual subscriptions.
 
<br />
<br />
<img src="https://i.imgur.com/6WNPBg1.png"/>

---
# 7. **Churn by Geography**   
  - Germany has the highest churn rate at 32.44%, meaning nearly 1 in 3 customers left.
  - France and Spain have similar churn rates (~16%), which are much lower than Germany.
.
- **Recommendation**
  - Focus on improving customer satisfaction in Germany, where the churn rate is highest. Conduct surveys to identify pain points and address them.
  - Consider localizing marketing efforts and customer support to better meet the needs of customers in different regions.
 
<br />
<br />
<img src="https://i.imgur.com/AbP2lvT.png"/>

---
# 8. **Churn by Credit Score**   
  - The churn rate is lowest (18.62%) among customers with “Good” credit, whereas customers with “Poor” credit have the highest churn (22%).
  - This indicates that customers with lower credit scores may be more likely to churn, possibly due to financial instability or dissatisfaction with terms.
.
- **Recommendation**
  - Customers with fair or lower credit scores may need additional support. Offer flexible payment options or financial planning tools to help them manage their accounts.
  - Provide educational resources to improve their financial health and reduce churn.
 
<br />
<br />
<img src="https://i.imgur.com/vaPxj3h.png"/>

  ---

## 📊 Data Sources  
- **Primary Dataset**: Customer churn dataset  (hypothetical source - anonymized for privacy).  
- **Cleaning**: Data standardized in Excel (removed duplicates, handled missing vaues by filling it with the MODE for catergorical columns and MEDIAN from numerical values ).  
                e.g =IF(A2="", "Male", A2)
                e.g =IF(F2="", MEDIAN(F$2:F$1000), F2)
---

## 🛠️ Tools Used  
- **Power BI Desktop**: Dashboard design, DAX measures, and data modeling.
- **DAX measures:**
    - **Purpose:** This formula calculates the churn rate (percentage of customers who have exited) for each geographic region (France, Spain, Germany).

    - **Logic:**
      - ChurnedCustomers: Counts the number of rows where Exited = "YES" (churned customers).
      - TotalCustomers: Counts the total number of customers for each geography using ALL and VALUES to ensure the calculation is grouped by geography.
      - RETURN: Divides the number of churned customers by the total number of customers for each geography, returning the churn rate.
<img src="https://i.imgur.com/8WoOMU5.png"/>

  - **Purpose:** This formula categorizes customers into tenure groups based on the number of years they have been with the company.
   - **Logic:**
    - Uses SWITCH to evaluate the Tenure value and assign it to a group:
     - 0-1 Years: For tenure ≤ 1 year.
     - 1-3 Years: For tenure ≤ 3 years.
     - 3-5 Years: For tenure ≤ 5 years.
     - >5 Years: For tenure > 5 years.
<img src="https://i.imgur.com/mCs1cwJ.png"/>

  - **Purpose:** This formula categorizes customers into credit score groups (Poor, Fair, Good, Excellent) based on their credit score.
   - **Logic:**
    - Uses SWITCH to evaluate the Credit_Score value and assign it to a group:
     - Poor: For credit scores < 580.
     - Fair: For credit scores < 670.
     - Good: For credit scores < 740.
     - Excellent: For credit scores ≥ 740.
<img src="https://i.imgur.com/OMmdUBa.png"/>

  - **Purpose:** This formula calculates the overall churn rate (percentage of customers who have exited) for the entire dataset.
   - **Logic:**
     - COUNTROWS(FILTER(...)): Counts the number of rows where Exited = "YES" (churned customers).
     - COUNTROWS(...): Counts the total number of customers in the dataset.
     - DIVIDE: Divides the number of churned customers by the total number of customers, returning the churn rate.
<img src="https://i.imgur.com/pbt4cmr.png"/>
  
- **Excel**: Initial data cleaning and validation.  
- **GitHub**: Version control and portfolio hosting.  
