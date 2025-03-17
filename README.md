# Fantom Opera
# 📋 Overview  

This portfolio demonstrates my ability to extract actionable insights from the Fantom Opera blockchain using Google BigQuery and SQL. The Fantom Opera dataset (bigquery-public-data.goog_blockchain_fantom_opera_us) contains granular on-chain data, including blocks, transactions, and log interactions. Below, I showcase queries ranging from basic data exploration to advanced network analytics, highlighting my technical proficiency in:

Data Aggregation (COUNT, SUM, AVG)
Joins (INNER JOIN, FULL OUTER JOIN)
Time-Series Analysis (DATE(), GROUP BY)
Performance Optimization (LIMIT, DISTINCT)


# 1. **Fetch the 10 Most Recent Blocks**   
Business Question: "How can we monitor real-time network activity to detect anomalies (e.g., spikes in block creation)?"

**SELECT *
FROM `bigquery-public-data.goog_blockchain_fantom_opera_us.blocks`
ORDER BY block_timestamp DESC
LIMIT 10;**

  - Operational Alerts: Sudden changes in block timing or gas usage could indicate network stress or attacks.
  - Validator Insights: Miners/validators can optimize block production strategies.

<br />
<br />
<img src="https://i.imgur.com/5l1dSyL.png"/>

---

# 2. **Total transactions on Fantom Opera.**  
Business Question: "Is Fantom Opera gaining traction compared to competitors like Ethereum or BSC?"

**SELECT COUNT(*) AS total_transactions
FROM `bigquery-public-data.goog_blockchain_fantom_opera_us.transactions;**

  - Investor Reporting: Total transactions are a KPI for ecosystem growth.
  - Partnership Decisions: High transaction volume attracts dApp developers.

<br />
<br />
<img src="https://i.imgur.com/5VDJ18e.png"/>                                        

---

# 3. **Daily average gas price**   
  Business Question: "When should users schedule transactions to minimize gas fees?"

**SELECT 
  DATE(t.block_timestamp) AS date,
  AVG(r.effective_gas_price) AS avg_gas_price_wei
FROM `bigquery-public-data.goog_blockchain_fantom_opera_us.transactions` AS t
INNER JOIN `bigquery-public-data.goog_blockchain_fantom_opera_us.receipts` AS r
  ON t.transaction_hash = r.transaction_hash
GROUP BY date
ORDER BY date;**
 
  - Cost Reduction: Users can avoid peak fee periods
  
  <img src="https://i.imgur.com/Mh1A7YK.png"/>

  ---
  
# 4. **Top 10 active addresses**:  
  Business Question: "Who are the most active users or contracts driving network activity?"

**SELECT 
  from_address AS address,
  COUNT(*) AS transaction_count
FROM `bigquery-public-data.goog_blockchain_fantom_opera_us.transactions`
GROUP BY from_address
ORDER BY transaction_count DESC
LIMIT 10;**

  - Customer Targeting: Engage high-frequency users with loyalty programs.
  - Fraud Detection: Flag suspiciously active addresses

<br />
<br />

<img src="https://i.imgur.com/cXE2IEF.png"/>

