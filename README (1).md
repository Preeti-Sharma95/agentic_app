
# 🏦 Unified Dormant Account Compliance App

A Streamlit-based interactive web application to analyze dormant and inoperative banking accounts in compliance with regulatory frameworks like **CBUAE** (Central Bank of the UAE).

## 📌 Features

- 🔍 Agent-based account analysis using inactivity and contact attempt logic
- 📤 Upload CSVs with transaction and KYC data
- 🧠 Optional AI insight summaries (Groq/LLM-enabled)
- 📊 Data visualization and CSV export of detected accounts

## 📂 Supported Agents

| Agent | Description |
|-------|-------------|
| 🏦 Fixed Deposit Agent | Detects fixed deposits inactive for 3+ years |
| 📉 3-Year General Inactivity Agent | Flags savings/call/current accounts inactive >3 years |
| 📵 Unreachable + Marked Dormant Agent | Identifies unreachable dormant accounts |
| 📨 Contact Attempt Verification Agent | Finds accounts with incomplete outreach |
| 🚩 Flag Dormant Account Agent | Flags accounts for dormancy classification |
| 📘 Dormant Ledger Reclassification Agent | Moves eligible accounts to dormant ledger |
| ❄ Freeze Eligibility Agent | Finds dormant accounts with expired KYC |
| 🏦 CBUAE Transfer Agent | Identifies accounts for central bank transfer |

## 🏁 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-org/dormant-compliance-app.git
cd dormant-compliance-app
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Run the App

```bash
streamlit run newcode_fixed.py
```

## 📤 CSV Format

Make sure your CSV includes at least:

- `Account_Type`
- `Last_Transaction_Date`
- `Account_Status`
- `Email_Contact_Attempt`
- `SMS_Contact_Attempt`
- `Phone_Call_Attempt`
- `KYC_Status` (for Freeze Agent)

## 🔐 Optional AI (Groq / Langchain)

To enable AI insights:

```toml
# .streamlit/secrets.toml
GROQ_API_KEY = "your_groq_api_key_here"
```

## 🧠 AI Insight Use

- Uses `langchain` + `Groq` to summarize data trends
- Requires additional packages (`langchain`, `langchain_groq`, `openai`)

## 📜 License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for more info.

---

> Built with ❤️ for compliance, transparency, and data governance.
