# KhataSnap 📒⚡

**KhataSnap digitizes the traditional Indian shopkeeper's ledger (khata) using OCR, ASR, and intelligent sales analytics — turning handwritten and spoken entries into an automated inventory, tax, and reconciliation system.**

---

## 🔍 Problem Statement

Small shopkeepers and MSMEs in India still rely on handwritten ledgers (khatas) to track sales, dues, and inventory. This leads to:
- Manual, error-prone bookkeeping
- No visibility into profit margins or fast/slow-moving products
- Time lost reconciling mismatched entries
- Difficulty computing accurate tax liability

KhataSnap solves this by digitizing ledger entries and layering smart automation on top.

---

## ✨ Key Features

### 📸 OCR-Based Ledger Digitization
Scans handwritten khata entries (photos of ledger pages) and converts them into structured digital records — no manual data entry needed.

### 🎙️ ASR (Voice Input)
Shopkeepers can speak out a sale ("2 packets of sugar, 50 rupees") and the system transcribes and logs it automatically — built for users who may not be comfortable typing.

### 🧮 Smart Calculator
Learns sales patterns over time to:
- Calculate applicable taxes automatically
- Identify profit-making vs. loss-making products
- Surface which products are actually driving margin

### 📦 Smart Inventory
Tracks stock levels in real time as sales are logged, and flags items that need restocking based on sales velocity.

### 🔎 Price-to-Product Inference
A standout feature — if a shopkeeper just enters a **price**, the system intelligently guesses **which product** was likely sold, based on learned sales patterns. Speeds up entry when product name/details are skipped.

### ⚖️ Smart Reconciliation Engine
Detects mismatches between recorded ledger entries, inventory counts, and cash/sales totals — and helps pinpoint and correct human entry errors automatically.

---

## 🛠️ Tech Stack

> _Fill in the actual stack you used, e.g.:_
🛠️ Tech Stack

- Backend: Python (Flask/FastAPI)

- OCR: Tesseract

- ASR: Google Speech-to-Text

- ML/Pattern Learning:Pandas, scikit-learn

- Frontend:(React / HTML-CSS-JS)

- Database: (Supabase / PostgreSQL)

---

## ⚙️ How It Works

1. Shopkeeper uploads a photo of a ledger page or speaks a sale entry
2. OCR/ASR pipeline extracts and structures the transaction data
3. Smart calculator engine updates inventory, computes tax, and flags profit/loss per product
4. If only a price is entered, the inference model predicts the most likely product sold
5. Reconciliation engine cross-checks entries against inventory and cash records, surfacing and correcting discrepancies

---


## 🎯 Future Scope

- Multi-language OCR/ASR support for regional languages
- GST-compliant automated filing integration
- Predictive restocking alerts
- Mobile app version

---

## 👩‍💻 Author

**Tina Sahu**
[GitHub](https://github.com/Tinaasahu) · [LinkedIn](https://www.linkedin.com/in/tina-sahu-3609a6327/)
