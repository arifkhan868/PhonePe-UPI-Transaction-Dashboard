# PhonePe UPI Transaction Dashboard 📊

An interactive Excel dashboard analyzing **502,888 UPI transactions**, built with PivotTables, PivotCharts, and slicers to explore transaction volume, revenue, fraud signals, and user behavior across India.

![Dashboard Overview](screenshots/dashboard_overview.png)

## 🔍 Overview

This project simulates a real-time analytics dashboard for PhonePe-style UPI transactions, covering payment apps, banks, merchant categories, states, and time-of-day patterns. It's designed the way a fintech analytics/ops team might monitor daily transaction health.

## 📈 Key Metrics

| Metric | Value |
|---|---|
| Total Transactions | 502.89K |
| Total Amount | $442.48 (in dataset currency units) |
| Total Cashback | $3.46M |
| Success Rate | 91.00% |
| Suspected Fraud | 17.09K transactions |

## 🧩 Dashboard Features

- **KPI cards** — transaction count, amount, cashback, success rate, and fraud flags at a glance
- **Transaction Amount Over Time** — daily trend area chart
- **Transaction by UPI App** — PhonePe, Google Pay, Paytm, Amazon Pay, BHIM, Cred Pay, WhatsApp Pay
- **Transaction by Status** — Success / Failed / Pending / Refunded breakdown
- **Transaction by State** — choropleth map of India
- **Transaction by Bank** — top banks by transaction value
- **Transaction by Type** — P2M, P2P, Bill Payment, Online Shopping, Recharge, Subscription, Wallet Transfer
- **Transaction by Hour** — intraday volume distribution
- **Transaction by Day & Hour** — heatmap identifying peak usage windows
- **Slicers** — filter live by City, Gender, Merchant Name, and Merchant Category

## 🛠️ Tools & Techniques

- Microsoft Excel (PivotTables, PivotCharts, Slicers)
- Data cleaning and transformation
- Map chart (Filled Map / Bing Maps integration)
- Conditional formatting for heatmap visualization
- Dashboard layout and UX design principles

## 📁 Repository Structure

```
phonepe-repo/
├── README.md
├── screenshots/
│   └── dashboard_overview.png
├── data/
│   └── sample_transactions.csv   # 3,000-row sample of the full 502K-row dataset
└── Phonepe_project.xlsx          # full Excel workbook (see note below)
```

## 📦 Dataset

The full dataset contains **502,888 rows × 24 columns**, including:

`Transaction_ID, Transaction_Date, Transaction_Time, UPI_App, Customer_ID, Age_Group, Gender, State, City, Merchant_Name, Merchant_Category, Transaction_Type, Payment_Mode, Bank_Name, Amount_INR, Cashback_INR, Transaction_Fee_INR, Status, Failure_Reason, Device_OS, Risk_Score, Is_Suspected_Fraud`

A representative **3,000-row sample** is included in [`data/sample_transactions.csv`](data/sample_transactions.csv) for quick exploration. The full workbook is included in this repo directly (see note below on Git LFS if it exceeds GitHub's file size limits).

> **Note:** GitHub has a 100MB per-file limit. If `Phonepe_project.xlsx` is close to or over that limit, use [Git LFS](https://git-lfs.com/) to track it — see setup steps below.

## 🚀 Getting Started

1. Clone this repo
2. Open `Phonepe_project.xlsx` in Excel (2016+ recommended for map charts)
3. Explore the `Dashboard` sheet — use the slicers on the left to filter by city, gender, merchant, or category
4. Check the `Analysis` and `Matric` sheets for underlying PivotTables and calculations

## 💡 Insights

- Peak transaction activity occurs in the late afternoon/evening hours (based on the hourly distribution chart)
- PhonePe leads transaction share among UPI apps, followed by Google Pay and Paytm
- P2M (person-to-merchant) and P2P transfers make up the largest transaction-type categories
- ~91% of transactions succeed, with a small but notable fraud-flag rate worth monitoring

## 📄 License

This project uses a synthetic/simulated dataset for educational and portfolio purposes. Not affiliated with or endorsed by PhonePe.
