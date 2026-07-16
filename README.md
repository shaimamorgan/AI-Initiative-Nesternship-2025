# AI-Initiative-Nesternship-2025
# 🧾 Nestlé Trade Agreement & Tax Invoice Validation Tool

## 📌 Project Overview

This repository contains the conceptual design and implementation framework for an **AI-powered validation tool** developed during my internship at **Nestlé (Batch 2025)** .

The primary objective of this tool is to automate the double-verification process between **Trade Agreements** and **Tax Invoices**. By leveraging Microsoft’s Power Platform, we aim to reduce manual reconciliation errors, ensure compliance, and speed up the financial auditing process.

---

## 🧠 The Problem

During my internship at Nestlé, I observed sales teams often struggled with:

- **Manual Data Entry** 
- **Time Consumption** 

> This sparked the idea: *"What if we could train AI to read these documents and flag mismatches instantly?"*

---

## 🚀 The Solution

We propose a **Low-Code AI Validation Tool** built entirely within the Microsoft Power Platform ecosystem. The tool scans, extracts, and validates data from both unstructured trade agreements and structured tax invoices, providing a clear "Match" or "Mismatch" status with highlighted discrepancies.

### Core Value Proposition
- **Accuracy** 
- **Speed** 
- **Audit Trail:** Stores every scanned document and validation result for review.

---

## 🛠️ Technical Architecture

This solution utilizes a robust stack of Microsoft tools to ensure seamless integration and scalability.

### 1. 📱 Power Apps (Front-End Interface)
- **Role:** Acts as the user-friendly interface for the sales teams.
- **Features:**
  - Upload interface for Trade Agreements (PDF).
  - Upload interface for Tax Invoices (PDF).
  - Dashboard displaying validation results (Green = Match / Red = Mismatch).
  - Comment on the "Mismatch Report" viewer.

### 2. ⚙️ Power Automate (Backend & AI Training)
- **Role:** The brain of the operation. Orchestrates the AI models and workflow.
- **Process:**
  - Triggers a flow when a new document is uploaded.
  - Uses **AI Builder** (pre-trained and custom models) to extract key fields:
    - *From Agreement items* 
    - *From Invoice items*
  - Compares extracted data against the specific agreement rules.
  - Sends the structured results back to Power Apps.

### 3. 🗄️ SharePoint (Document Storage & Metadata)
- **Role:** Secure document repository and metadata management.
- **Structure:**
  - **Library 1:** `Agreements` (Stores original Trade Agreement PDFs).
  - **Library 2:** `Invoices` (Stores original Tax Invoices).
  - **List:** `Validation_Results` (Stores the JSON data/results from AI, allowing for easy searching and filtering).

---

