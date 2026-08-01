# 📒⚡ KhataSnap — AI-Powered Kirana Ledger & Smart ERP System

[![Project Status: Active](https://img.shields.io/badge/Project-Integrated--Microservices-brightgreen.svg)](https://github.com/Tinaasahu/khatasnap-improved)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100%2B-009688.svg)](https://fastapi.tiangolo.com/)
[![React](https://img.shields.io/badge/React-18.0-61DAFB.svg)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-5.0-646CFF.svg)](https://vitejs.dev/)
[![Express.js](https://img.shields.io/badge/Express-4.x-000000.svg)](https://expressjs.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> **KhataSnap** digitizes the traditional Indian shopkeeper's ledger (*khata*) using advanced multi-modal OCR pipelines, voice recognition (ASR), and intelligent Bayesian sales reconciliation — turning handwritten notes and spoken entries into an automated inventory, tax, and sales system.

---

## 📌 Executive Overview & Problem Statement

Millions of small shopkeepers (*Kirana stores*) and micro-enterprises across India rely daily on paper-based handwritten ledgers (*khatas*) to record sales, credit (*udhar*), and inventory. This traditional workflow presents critical operational challenges:

1. **Manual & Error-Prone Bookkeeping**: Miscalculations in handwritten entries lead to financial leakage.
2. **Lack of Inventory & Profit Visibility**: No real-time tracking of high-margin vs. slow-moving goods.
3. **Reconciliation Bottlenecks**: Significant time wasted cross-checking physical cash drawers against ledger logs.
4. **Complex Tax Computation**: Difficulty extracting line items for accurate GST tracking.

**KhataSnap** addresses these pain points by offering a multi-modal input system (Camera + Voice + Smart Keypad) backed by a microservices orchestrator that automatically processes, reconciles, and logs every transaction into a centralized database.

---

## ✨ Key Capabilities & Highlights

### 📸 1. OCR Ledger & Invoice Digitization
- **Multi-Stage Vision Pipeline**: Scans handwritten ledger pages and printed invoices.
- **8-Step Processing**: Includes Image Quality Analysis → Contrast Enhancement → Perspective Crop & Deskewing → OCR Extraction (PaddleOCR / VLM GLM-OCR) → Layout Row Grouping → Regex Extraction → Confidence Scoring.

### 🎙️ 2. Natural Language Voice Billing (ASR)
- **Hands-Free Logging**: Designed for quick counter sales. Speak entries like *"2 packets of sugar 50 rupees"*.
- **Speech Parsing Engine**: Converts spoken audio/text into structured item tuples containing quantity, unit, product name, and computed totals.

### 🧮 3. Price-to-Product Bayesian Inference
- **Smart Keypad Assistance**: When a busy shopkeeper inputs only a price (e.g., `₹50`), KhataSnap’s inference engine uses historical frequency models to predict the most likely item sold (e.g., *"Amul Butter 100g"*), accelerating checkout speed.

### ⚖️ 4. Smart Reconciliation Engine (SRE v5)
- **Automated Discrepancy Prevention**: Uses Bayesian probability modeling with historical warm-start memory to audit cash drawer totals against itemized stock updates.
- **Safety Flags**: Every transaction is checked for stock mismatches or pricing anomalies before permanent database execution.

### 📦 5. Real-Time Inventory & Stock Management
- **Automated Auditing**: Stock levels decrease automatically as transactions are confirmed.
- **Catalog & Supplier Mapping**: Manages category mappings, supplier SKUs, and low-stock threshold alerts.

---

## 🏗️ System Architecture & Data Flow

KhataSnap is structured as an **Orchestrated Microservice Architecture**. The React frontend communicates strictly with a central **FastAPI Orchestrator Gateway**, which delegates specialized processing to backend microservices.

