# Project Technical Description: Stock Divergence Analysis

File ini menjelaskan metodologi teknis, logika perhitungan indikator, dan pendekatan statistik yang digunakan dalam analisis saham **WINE.JK**, **INAI.JK**, dan **HUMI.JK**.

---

## 1. Analisis Teknikal (Momentum Indicators)

Proyek ini menggunakan dua indikator utama untuk mendeteksi *Market Anomaly* melalui metode **Divergence**:

### A. MACD (Moving Average Convergence Divergence)
- **Parameters:** Fast EMA (12), Slow EMA (26), Signal Line (9).
- **Logika:** Digunakan untuk mengidentifikasi perubahan kekuatan, arah, momentum, dan durasi tren harga saham. Sinyal pembalikan dideteksi ketika pergerakan histogram MACD berlawanan arah dengan pergerakan harga (*Convergence/Divergence*).

### B. RSI (Relative Strength Index)
- **Parameters:** 14-period.
- **Logika:** Mengukur besarnya perubahan harga terbaru untuk mengevaluasi kondisi *overbought* (di atas 70) atau *oversold* (di bawah 30).
- **Divergence Detection:** - **Bullish Divergence:** Harga membuat *Lower Low*, tapi RSI membuat *Higher Low*.
  - **Bearish Divergence:** Harga membuat *Higher High*, tapi RSI membuat *Lower High*.

---

## 2. Metodologi Statistik

Validasi sinyal tidak hanya dilakukan secara visual, tetapi juga melalui pengujian kuantitatif:

### Z-Score Analysis
Digunakan untuk menentukan seberapa jauh harga saat ini menyimpang dari rata-rata pergerakannya. 
- **Z > 2 atau Z < -2** dianggap sebagai kondisi ekstrim yang memperkuat potensi *reversal*.

### Kruskal-Wallis Test
Karena data harga saham seringkali tidak terdistribusi normal (memiliki *skewness*), maka digunakan uji non-parametrik **Kruskal-Wallis** untuk membandingkan apakah terdapat perbedaan performa/volatilitas yang signifikan secara statistik antara ketiga emiten tersebut.

### Confidence Interval (95%)
Menghitung estimasi rentang harga di masa depan berdasarkan volatilitas historis. Ini memberikan batasan risiko bagi investor sebelum melakukan *Entry*.

---

## 3. Workflow Data (Pipeline)

1. **Extraction:** Penarikan data *Real-Time* melalui API `yfinance`.
2. **Preprocessing:** - Konversi tipe data datetime.
   - Penanganan nilai kosong pada kolom `Adj Close`.
   - Feature engineering untuk kolom *Returns* dan *Volatility*.
3. **Indicator Calculation:** Menggunakan library `pandas-ta` untuk menjamin akurasi perhitungan matematis.
4. **Visualization:** - **Exploratory Data Analysis (EDA):** Menggunakan Seaborn dan Matplotlib.
   - **Interactive Dashboard:** Data diekspor ke format `.csv` yang kompatibel dengan skema data Tableau.

---

## 4. Target & Output Bisnis
- **Profit Target:** Estimasi **33%** berdasarkan perhitungan *Risk-to-Reward Ratio*.
- **Statistical Significance:** Seluruh keputusan strategis harus melewati ambang batas **P-Value < 0.05**.
- **User Interface:** Dashboard Tableau yang memungkinkan pengguna memantau sinyal secara interaktif.

---