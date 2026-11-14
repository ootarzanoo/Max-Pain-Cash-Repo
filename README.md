# 📈 Max Pain & Open Interest Cash Trading System
> An algorithmic monthly swing trading system for Indian Equities (F&O stocks in Cash delivery), leveraging Institutional Option Chain dynamics (Put Support & Max Pain).

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Win Rate](https://img.shields.io/badge/Backtest%20Win%20Rate-83.3%25-brightgreen.svg)]()
[![Risk Reward](https://img.shields.io/badge/Risk%20Reward-1%3A2.34-success.svg)]()

---

## 📌 Overview

Retail traders often lose money buying weekly options due to rapid **Theta (Time) Decay**. Meanwhile, institutional option writers position massive liquidity around key strikes to maximize their profits by monthly expiry.

This system exploits this institutional positioning by taking **Cash Delivery trades** (no time decay) at **Max Put OI (Institutional Floor/Support)** and targeting **Max Pain (Institutional Expiry Magnet)**.

---

## 🚀 Key Strategy Features
* **Zero Time Decay:** Operates strictly in the cash equity segment for F&O underlying stocks.
* **Mean Reversion to Max Pain:** Capitalizes on option writers pinning the price near Max Pain on monthly expiry.
* **Asymmetric Risk-to-Reward:** 1 : 2.34 Risk-to-Reward profile with strict -1.8% stop-loss rules.
* **Automated Telegram Alerts:** Real-time push notifications sent directly to your phone when stocks enter the buy zone.

---

## 📊 Backtested Performance (Past 12 Monthly Cycles)

| Metric | Result | Analysis |
| :--- | :--- | :--- |
| **Total Expiry Cycles Tested** | **12 Months** | Frontline heavyweights (RELIANCE, TATAMOTORS, SBIN, INFY, HDFCBANK) |
| **Winning Trades** | **10** | Reached Max Pain Target or Expiry Pin |
| **Losing Trades** | **2** | Stopped out cleanly on macro/earnings volatility |
| **Strategy Win Rate** | **83.3%** | Consistent monthly performance |
| **Average Profit per Win** | **+4.38%** | Net delivery profit per trade |
| **Average Loss per Stop Loss** | **-1.87%** | Strict risk containment |
| **Total Cumulative Return** | **+39.5%** | Pure cash equity return without leverage |

---

## 📐 The 4 Golden Execution Rules

1. **Rule 1 (Entry):** Buy cash delivery when Current Market Price (CMP) is within 2.5% of **Max Put OI Support** and **Max Pain** is at least 3.5% - 4% above CMP.
2. **Rule 2 (Target):** Book full profits when the stock price reaches the **Max Pain strike**.
3. **Rule 3 (Stop-Loss):** Exit immediately if daily close breaches 1.8% below the Support strike.
4. **Rule 4 (Time Exit):** Close any open swing position on monthly expiry Thursday by 3:15 PM IST.

---

## 🛠️ Quick Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/ootarzanoo/Max-Pain-Cash-Repo.git
cd Max-Pain-Cash-Repo
```

### 2. Install Dependencies
```bash
pip install pandas numpy requests
```

### 3. Run the Scanner
```bash
python script.py
```

---

## 📱 Telegram Alerts Configuration

1. Search for `@BotFather` on Telegram and send `/newbot` to generate your **Bot API Token**.
2. Search for `@userinfobot` to get your numeric **Chat ID**.
3. Open `script.py` and insert your credentials:
   ```python
   TELEGRAM_BOT_TOKEN = "your_bot_token_here"
   TELEGRAM_CHAT_ID = "your_chat_id_here"
   ```
4. Run `script.py` to start receiving instant alerts on your phone!

---

## ⚠️ Disclaimer
*This repository and strategy are for educational and analytical purposes only. Financial markets carry risk. Always consult a SEBI registered financial advisor before trading.*
