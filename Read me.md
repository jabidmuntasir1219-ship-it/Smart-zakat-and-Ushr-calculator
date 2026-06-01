# 🌙 Ultimate Shariah Zakat & Ushr Calculator

An advanced, responsive, single-page web application designed to compute individual wealth Zakat and agricultural Zakat (Ushr) with strict adherence to classical Shariah guidelines. The engine features dynamic Nisab selection based on asset composition and automatically evaluates multi-tier agricultural irrigation models against traditional weight thresholds.

---

## 🚀 Live Demo
*Deploy the `index.html` file to GitHub Pages or any static hosting service, and paste your URL here.*

---

## ✨ Features & Shariah Logic Implemented

### 1. Smart Shariah Nisab Selection (Personal Wealth)
The calculator automatically detects the composition of your assets to apply the correct jurisprudential (Fiqh) rules:
*   **Only Gold Rule:** If you only own gold without any mixed assets (Cash, Silver, or Business Goods), the system benchmarks your net worth against the **Gold Nisab ($7.5 \text{ Vhari / Tola}$)**.
*   **Mixed Asset Rule:** If you possess gold along with even a minimal amount of cash, silver, or commercial goods, the core engine dynamically switches the evaluation benchmark to the **Silver Nisab ($52.5 \text{ Vhari / Tola}$)** as decreed by contemporary and classical consensus to maximize benefit for the recipients of Zakat.

### 2. Automatic Short-term Liability Deduction
Before calculating your due Zakat, the system subtracts immediate short-term debts, commercial liabilities, and pending utility/rental bills to evaluate your true **Net Excess Wealth ($Net \text{ } Wealth = Assets - Debts$)**, preventing unlawful taxation on debt.

### 3. Bulletproof Ushr Logic (Agricultural Produce)
Unlike basic calculators that run flat rate equations on raw valuations, this application accurately models agricultural jurisprudence:
*   **Weight-Based Nisab Verification:** It locks the traditional requirement of **$5 \text{ Wasqs}$ ($\approx 612 \text{ KG}$)** into the backend. Ushr is only triggered if the total accumulated harvest crosses this weight threshold.
*   **Dual Irrigation Tier Scaling:** It handles split-source irrigation yields dynamically within the same harvest period:
    *   **Rain-fed / Natural Water:** Taxed at **$10\%$** ($0.10$).
    *   **Irrigated / Artificial Water:** Taxed at **$5\%$** ($0.05$).
*   **Dynamic Valuation:** It converts the final deductible crop weight into local currency utilizing today's market rate per kilogram provided by the user.

---

## 🛠️ Tech Stack & Architecture

*   **Frontend:** Semantic HTML5, CSS3 (Modern clean cards, layout grid, flexbox system, responsive viewport scaling).
*   **Logic Engine:** Pure Vanilla JavaScript (ES6+). Zero external framework dependencies, ensuring immediate execution, optimal caching, and instant offline compilation.

### Core Mathematical Formulations Inside:

$$Net \text{ } Wealth = (Cash + GoldValue + SilverValue + BusinessGoods) - Debts$$

$$\text{If } Net \text{ } Wealth \ge Nisab \implies Zakat = Net \text{ } Wealth \times 0.025$$

$$\text{If } Total \text{ } Crop \text{ } Weight \ge 612\text{KG} \implies Ushr = [(RainCrop \times 0.10) + (IrrigatedCrop \times 0.05)] \times PricePerKg$$

---

## 📂 Installation & Local Setup

Since the entire application is fully contained within a single file, setting it up locally takes less than a minute.

1. **Clone the repository:**
```bash
   git clone [https://github.com/yourusername/shariah-zakat-ushr-calculator.git](https://github.com/yourusername/shariah-zakat-ushr-calculator.git)
