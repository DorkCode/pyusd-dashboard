# 🚀 PYUSD X Google RPC Hackathon Project Submission

Welcome to my submission for the **PYUSD X Google RPC Hackathon**!  
This project uses **Google Colab** and **Google BigQuery** to analyze and visualize blockchain data related to **PYUSD**.

---

## 📑 Project Overview

An interactive Google Colab notebook that fetches, processes, and analyzes blockchain data using **Google BigQuery** and **Google RPC**.

---

## 📘 Steps in the Notebook

### 1. **Importing Library and Setting Up the Environment**

Initialize all necessary Python libraries and configure the Colab environment.

### 2. **Inputting GCP Project ID and Blockchain RPC URLs**

Configure user-specific details:

```python
GCP_PROJECT_ID = "your-google-cloud-project-id"

BLOCKCHAIN_RPC = {
    'ethereum': {
        'holesky': 'https://blockchain.googleapis.com/v1/projects/',
        'mainnet': 'https://blockchain.googleapis.com/v1/projects/',
        'sepolia': 'https://blockchain.googleapis.com/v1/projects/'
    }
}
```

### 3. Testing Google RPC

Verify your RPC setup by fetching:

A specific Ethereum transaction

A specific Ethereum block

### 4. Setting Up BigQuery (Requires Service Account Key)

Authenticate BigQuery access using your Google Service Account key (as a triple-quoted string).

Required IAM Roles:

BigQuery Data Viewer

BigQuery Job User

BigQuery Read Session

🔗 How to Generate a Service Account Key
https://chatgpt.com/c/67fd9c44-e3b4-800c-8a9d-6e650bd5146f#

### 5. Recent PYUSD Transfers Involving Wallet

Analyze recent PYUSD transfers for a given wallet_address on a selected_date.
Output is styled in a clean, readable table.

### 6. Minimum Gas Fee Over a Period

Query Ethereum transactions to calculate the minimum gas fee (Gwei) over a defined time range.

### 7. Sanction Check

Check wallet addresses against known sanction lists.
Also detects if the wallet interacted with any sanctioned address.

### 8. Top PYUSD Accounts by Daily Activity

Identify most active PYUSD accounts based on today’s transaction count.

### 9. Daily Minimum and Average Gas Fee Over the Last 30 Days

Visualize the daily minimum and average gas fee (in Gwei) over the last 30 days. Presented as:

- An enhanced table
- A line chart

### 10. Daily PYUSD Transaction Count (30 Days)

Track and visualize daily PYUSD transaction trends across the past 30 days.

### 11. Stablecoin Transfer Counts for the Last 30 Days and Their Distribution

Aggregate the transfer counts for various stablecoins over the last 30 days and display their distribution.

### 12. Stablecoin Transfer Volume for the Last 30 Days and Their Distribution

Compute the overall transfer volume for each stablecoin (accounting for differences in decimal points) over the last 30 days and visualize their distribution.

### 13. PYUSD Transactions of a Selected Wallet in Last 30 Days

Retrieve and display detailed PYUSD transactions (showing from/to addresses and PYUSD value) for a specified wallet over the last 30 days.

---

## 🛠️ Requirements

🔹 Google Cloud Setup
Active Google Cloud Project with BigQuery enabled

Service Account Key with roles:

BigQuery Data Viewer

BigQuery Job User

BigQuery Read Session

Paste your key string in Step 4.

## Python Libraries

- google.cloud.bigquery

- google.oauth2.service_account

- pandas

- matplotlib

- IPython.display

```bash
pip install google-cloud-bigquery google-auth pandas matplotlib

```

## 🧠 How to Run the Notebook

Open the notebook in Google Colab

Configure:

GCP_PROJECT_ID

BLOCKCHAIN_RPC

Paste your Service Account key in Step 4

Execute each step sequentially

## 📊 Features

Enhanced Tables: Clean formatting, centered alignment, alternating row colors

Graphs: Matplotlib line charts for trends

## 🌟 Benefits

Hands-on exploration of blockchain data

Save gas fees by analyzing historical patterns

Compliance checks with sanction detection

Insights into wallet activity & trends

## 🤝 Contribution & Feedback

Feel free to:

Fork or extend the project

Open issues

Drop feedback!
