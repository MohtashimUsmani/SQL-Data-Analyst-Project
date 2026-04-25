# 💳 SQL Fraud Detection & Analysis Project

This project focuses on analyzing financial transaction data using SQL to detect suspicious patterns, fraudulent activities, and anomalies.

It is designed as a hands-on practice project for improving SQL skills, especially for data analysis and fintech-related problems.

---

## 🚀 Project Objectives

- Detect fraudulent transactions
- Analyze transaction behavior over time
- Identify suspicious patterns (e.g., zero balance anomalies)
- Practice advanced SQL concepts like:
  - CTEs (Common Table Expressions)
  - Recursive queries
  - Window functions
  - Joins & aggregations

---

## 📊 Dataset

The dataset contains transaction-level data with fields such as:

- `nameOrig` – Sender account
- `nameDest` – Receiver account
- `amount` – Transaction amount
- `type` – Transaction type (TRANSFER, CASH_OUT, etc.)
- `oldbalanceOrg`, `newbalanceOrig`
- `oldbalanceDest`, `newbalanceDest`
- `isFlaggedFraud` – Fraud indicator

---

## 🧠 Key SQL Tasks Covered

### 1. Detect Recursive Fraud Chains
Identify multi-step money transfers across accounts using recursive CTEs.

### 2. Analyze Fraud Over Time
Calculate rolling sums of fraudulent transactions using window functions.

### 3. Large Suspicious Transfers
Filter high-value transfers combined with unusual balance behavior.

### 4. No Balance Change Detection
Detect cases where balances remain unchanged after transactions.

### 5. Zero Balance Transactions
Find transactions where the destination account had zero balance before or after.

---

## 🛠️ SQL Concepts Used

- WITH (CTE)
- Recursive CTE
- INNER JOIN
- USING vs ON
- Window Functions (`SUM OVER`)
- Filtering & Conditions

---

## 💡 Sample Query

```sql
SELECT *
FROM transactions
WHERE oldbalanceDest = 0 OR newbalanceDest = 0;
