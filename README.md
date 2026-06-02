# 🌙 Smart Shariah Zakat & Multi-Crop Ushr Calculator

A highly responsive, single-page Islamic FinTech web application built to calculate individual wealth Zakat and multi-crop agricultural Zakat (Ushr). This engine isolates the calculation tracks using a dynamic interface, ensuring strict adherence to classical Shariah guidelines regarding asset thresholds (Nisab) and specific execution timings.

---

## 🚀 Live Demo
🔗 **https://jabidmuntasir1219-ship-it.github.io/Smart-zakat-and-Ushr-calculator/**

---

## ✨ Key Features & Shariah Logic Implemented

### 1. Isolated Timelines via Dynamic UI Tabs
In Islamic jurisprudence, personal wealth Zakat and agricultural Ushr operate on completely different schedules:
* **Zakat:** Calculated **once a year** (upon completing a lunar year cycle) on accumulated savings.
* **Ushr:** Due **immediately at the time of harvest**, regardless of how many times a year a crop is reaped.

The calculator implements a dynamic dropdown that switches the view entirely between **Zakat Mode** and **Ushr Mode**. This keeps the interface clean and prevents users from misinterpreting the separate timelines.

### 2. Smart Nisab Selection (Personal Wealth)
* **Gold Nisab ($7.5 \text{ Vhari / Tola}$):** Activated automatically if the user owns only gold with no other mixed assets.
* **Silver Nisab ($52.5 \text{ Vhari / Tola}$):** Triggered if the user possesses mixed liquid assets (Cash, Silver, or Business Goods) to ensure the maximum benefit for Zakat recipients under modern economic consensus.

### 3. Bulletproof Multi-Crop Ushr Engine
* **Dynamic Crop Repeater:** Users can dynamically click **"+ Add Another Crop"** to list multiple distinct crops (e.g., Rice, Wheat, Mangoes) harvested within the same season.
* **Independent Weight Filter:** It locks the traditional requirement of **$5 \text{ Wasqs}$ ($\approx 612 \text{ KG}$)**. Each crop card independently verifies whether its specific harvest weight meets the threshold. If a crop falls below $612 \text{ KG}$, its Ushr safely evaluates to `$0.00$`.
* **Dual Irrigation Tier Scaling:** Computes complex natural rain-fed yield (**$10\%$** tax) and artificial irrigated yield (**$5\%$** tax) accurately on a per-kilogram basis before applying local market prices.

---

## 🛠️ Tech Stack

* **Frontend:** Semantic HTML5, CSS3 (Modern responsive card layouts, flexbox structures, and dynamic visibility states).
* **Backend Logic:** Pure Vanilla JavaScript (ES6+). Light-weight execution running entirely on client-side client architecture—making it 100% mobile-friendly for both coding and end-user execution.

---

## 📂 Open Source Roadmap & How to Contribute 🚀

This repository is now **Public** and open for worldwide community contributions! We aim to make this tool a robust solution for the global Muslim community. 

If you want to contribute, please clone the repository, create a separate branch, and open a **Pull Request (PR)** targeting any of the following open development challenges:

### 1. [Bug Fix] String Concatenation Issue
* **Problem:** JavaScript sometimes treats the raw DOM input values of `cropRainWeight` and `cropIrrigWeight` as text strings rather than numbers, resulting in string gluing (e.g., inputting `500` and `200` calculates as `500200` KG instead of `700` KG).
* **Goal:** Explicitly enclose the multi-crop weight parameters within robust arithmetic parsing wrappers (`parseFloat()`).

### 2. [Feature Implementation] Live Market Price API Integration
* **Problem:** Users currently have to look up and input today's Gold, Silver, and Crop market wholesale rates manually.
* **Goal:** Integrate a reliable financial market API to pull real-time gold/silver data per Vhari, making the Nisab threshold fully automated.

### 3. [Logic Optimization] Combined Species Evaluation
* **Problem:** If a user registers "Boro Rice" (500 KG) and "Amon Rice" (300 KG) in separate cards, the loop reviews them as independent species and rejects both for Ushr since neither crosses 612 KG on its own. Fiqh dictates they should be summed up since they belong to the same genus.
* **Goal:** Update the backend array iteration to parse crop names or tags, grouping identical/similar genera together before calculating the Nisab validation block.

### 4. [UI/UX] State Management Reset
* **Goal:** Write an automated data flush script inside the `toggleFormSections()` function so that changing the calculation selection completely resets previous execution data fields, eliminating stale state errors.

---

## 🛡️ License
Distributed under the MIT License. Feel free to use, modify, and distribute.
