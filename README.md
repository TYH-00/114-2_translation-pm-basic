# 114-2_translation-pm-basic
A basic translation project management tool.

## Real-Time Translation Project Management System (TEP Framework)

A lightweight, high-fidelity Translation Project Management (TPM) dashboard designed for academic simulation and small-scale Localization Service Provider (LSP) workflows. This system enables real-time Tracking, Evaluation, and Pricing by dynamically parsing and cross-referencing live data streams from Google Sheets (via published CSV endpoints).

---

### 🚀 Key Features

* **Dynamic Data Synchronization:** Real-time integration with Translator Reports, Reviewer Feedback, Project Dispatcher, and Budget Estimation spreadsheets.
* **Cross-Table Relation Engine:** Automatically links proofreading records back to the original translation entry using `Translator Name`, `Version Number`, and `Document Page/Video Timestamp` to dynamically resolve missing word counts for reviewer metrics.
* **Robust Field-Matching:** Built-in fuzzy-matching logic to prevent parsing failures caused by automated Google Forms trailing parentheses or white spaces (e.g., dynamically handling `Actual Hours (hrs)` vs `Actual Hours`).
* **TEP Financial KPI Gauge:** Visualizes budget burn rate and surplus ratios using a responsive Morandi-styled dashboard interface.
* **Smart `+` Accumulator:** Custom algorithms designed to parse and tally human-entered data markers (such as counting cumulative edits with trailing `+` signs) without crashing the dashboard logic.

---

### 💼 Business Logic & TEP Cost Allocation

While standard Localization Service Providers (LSPs) typically present clients with an all-inclusive single rate per word, internal operations and production-level project management require strict cost splitting across the **TEP (Translation, Editing, Proofreading)** pipeline. 

This project simulates a highly professional and realistic cost breakdown to balance labor distribution and daily yield realities:

| Phase | Role | Production Benchmark | Standard Cost Allocation |
| :--- | :--- | :--- | :--- |
| **Translation (T)** | Initial Draft Creation | ~2,000 to 3,000 words / day | **60% - 70%** (e.g., NT$ 1.5 / word) |
| **Editing (E)** | Bilingual Review & Accuracy | ~6,000 to 8,000 words / day | **20% - 25%** (e.g., NT$ 0.5 / word) |
| **Proofreading (P)** | Monolingual Fluency & DTP | ~10,000+ words / day | **10% - 15%** (e.g., NT$ 0.2 / word) |

*Note: This system's budget engine is fully dynamic and auto-fetches your adjusted, realistic unit costs directly from your cloud spreadsheet.*

---

### 🛠️ Architecture & Translation Workflow

The system maps metrics and quality indicators across three major project lifecycle gates:

#### 1. Preparation Phase
* **Project Scope Analysis:** PM evaluates technical difficulty, duplicate metrics, and files.
* **Glossary & TM Alignment:** Setting up specific term bases to ensure consistency.

#### 2. Execution Phase
* **Draft Generation:** Translators submit word counts and actual duration metrics.
* **Bilingual Review:** Reviewers perform linguistic quality assurance (LQA), scoring errors using a 5-tier classification system (Terminology, Mistranslation, Grammar, Omission, Context).
* **Rework Loops:** Automatically flags rejected milestones back to "Rework in Progress" state.

#### 3. Delivery Phase
* **Final Quality Gates:** Monolingual proofing and tag verifications.
* **Financial Reconciliation:** Automatic computation of finalized expenditures against the global project budget.

---

### 📥 Getting Started

#### Prerequisites
To hook up your own data sources, you need a Google Spreadsheet with four distinct tabs corresponding to:
1. Translator Reports
2. Reviewer Feedback
3. Budget Estimation
4. Project Dispatcher

#### Cloud Connection Setup
1. In your Google Spreadsheet, navigate to `File` -> `Share` -> `Publish to Web`.
2. Select the specific tab you wish to connect.
3. Change the export type from *Web Page* to **Comma-separated values (.csv)**.
4. Copy the generated link.
5. Open this dashboard, click on **Cloud Data Configuration**, paste your URLs, and click **Sync Cloud Data**.

---

### 🎨 Design Theme
The user interface features a custom-designed **Morandi Palette**—utilizing muted Sage Greens (`#7D9D8C`), Slate Grays (`#2C3531`), and Warm Clays (`#C2B29E`) to minimize cognitive fatigue during long hours of data monitoring, typical of standard localization production environments.

---

### 👩‍💻 Credits & Project Info

* **Project Type:** Academic Course Simulation / Portfolio Demonstration
* **System Version:** Basic Version
* **Author / Designer:** Samantha
* **Technical Development:** Powered by Gemini (AI-Collaborative Architecture)
* **Copyright:** &copy; 2026 翻譯專案管理 (基礎款). Designed by Samantha (Powered by Gemini)

---

### ⚠️ Academic Disclaimer

This repository is created solely for educational and simulation purposes as part of a university course assignment. The integrated datasets, forms, and financial models represent mock scenarios designed to test localized workflow logic and cross-table automation. They do not constitute official corporate financial records or live business operations.
