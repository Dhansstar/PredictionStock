Ini draf README.md yang jauh lebih profesional dan "mahal" tampilannya. Gue sesuaikan dengan gaya Quantitative Analyst atau Data Scientist di bidang finance, lengkap dengan visualisasi badges dan struktur yang rapi.

Markdown
<div align="center">
  
  # 📈 Stock Trend Prediction: Divergence Analysis
  ### Case Study: WINE.JK, INAI.JK, and HUMI.JK (2025-2026)
  
  [![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
  [![Tableau](https://img.shields.io/badge/Tableau-Dashboard-E97627?style=for-the-badge&logo=tableau&logoColor=white)](https://public.tableau.com/app/profile/risyadhana.syaifuddin4030/viz/HargaSaham/Dashboard1)
  [![Status](https://img.shields.io/badge/Project-Milestone%201-success?style=for-the-badge)]()

  <p align="center">
    <i>An algorithmic approach to identifying market reversals and continuations using Momentum Divergence & Statistical Validation.</i>
  </p>
</div>

---

## 📌 Project Overview
Proyek ini mengintegrasikan **Technical Analysis** dan **Statistical Inference** untuk memprediksi pergerakan harga saham pada tiga emiten di Bursa Efek Indonesia (BEI): **WINE.JK, INAI.JK, dan HUMI.JK**. Fokus utama adalah mendeteksi sinyal *Bullish/Bearish Divergence* guna mengoptimalkan strategi *Entry* dan *Exit* pasar.

## 💡 Problem Statement
Mengidentifikasi sinyal pembalikan arah (*reversal*) dan kelanjutan tren (*continuation*) melalui analisis **MACD** dan **RSI Divergence**. Proyek ini bertujuan untuk menentukan titik eksekusi yang optimal guna mencapai target estimasi profit **33%** dengan validitas statistik ($P < 0.05$) pada periode analisis 2025-2026.

## 🛠️ Technical Stacks
| Category | Tools / Libraries |
| :--- | :--- |
| **Language** | Python 3.9+ |
| **IDE** | Visual Studio Code |
| **Data Visualization** | Tableau Public, Matplotlib, Seaborn |
| **Data Manipulation** | Pandas, NumPy |
| **Technical Analysis** | Pandas-TA |
| **Data Source** | Yahoo Finance API (`yfinance`) |

## 📊 Analytical Methods
1. **Technical Indicators:**
   - **MACD (12, 26, 9):** Digunakan untuk melihat momentum dan konfirmasi tren.
   - **RSI (14):** Digunakan untuk mengukur kondisi *overbought/oversold* dan deteksi *divergence*.
2. **Statistical Testing:**
   - **Kruskal-Wallis Test:** Uji non-parametrik untuk membandingkan distribusi antar saham.
   - **Z-Score:** Identifikasi anomali dan volatilitas harga.
   - **Confidence Interval (95%):** Estimasi rentang pergerakan harga di masa depan.

## 📁 Repository Structure
* **`POM1_Risyadhana.ipynb`**: Notebook utama yang mencakup seluruh *pipeline* data:
    * **I. Introduction:** Identitas dan profil teknis.
    * **II. Problem Statement:** Latar belakang dan penjabaran SMART framework.
    * **III. Data Loading:** Ekstraksi data dari Yahoo Finance API.
    * **IV. Data Cleaning:** *Preprocessing*, penanganan *missing values*, dan *feature engineering*.
    * **V. Exploration & Analysis:** Visualisasi teknikal dan uji hipotesis statistik.
    * **VI. Conclusion:** Solusi manajerial dan rekomendasi investasi.
* **`P0M1_Risyadhana_dataset.csv`**: Dataset hasil olahan yang telah dioptimasi untuk visualisasi di Tableau.

## 🔗 Project Links
- **Tableau Interactive Dashboard:** [View Dashboard](https://public.tableau.com/app/profile/risyadhana.syaifuddin4030/viz/HargaSaham/Dashboard1?publish=yes)

---

## 👷 Author
**Risyadhana Syaifuddin**
*Data Scientist | Financial Market Analyst*

---
> **Disclaimer:** Analisis ini bertujuan untuk kepentingan edukasi dan riset data. Segala