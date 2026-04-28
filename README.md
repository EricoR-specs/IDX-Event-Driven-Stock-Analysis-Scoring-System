
# 📊 IDX Event-Driven Stock Analysis & Scoring System

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Status](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-MIT-green)
![Data](https://img.shields.io/badge/Data-IDX%20%7C%20News-orange)

Sistem analisis saham otomatis berbasis **event-driven** yang menggabungkan:

* Scraping keterbukaan informasi IDX
* Agregasi berita finansial
* Mekanisme **weighted scoring**

untuk mengidentifikasi emiten dengan potensi pergerakan harga signifikan.

---

## 🚀 Problem Statement

### 1. Analisis Masalah

Pasar saham Indonesia memiliki:

* Volume informasi tinggi (IDX + media)
* Banyak noise (laporan rutin, dividen, dll)
* Sulit mengidentifikasi katalis yang benar-benar impactful

### 2. Asumsi Tersembunyi

* Tidak semua berita berdampak ke harga
* Aksi korporasi tertentu memiliki bobot lebih tinggi
* Kombinasi multi-source > single source

### 3. Solusi

Pipeline otomatis yang:

* Menyaring noise
* Mengidentifikasi katalis
* Memberi skor prioritas
* Menyusun konteks siap analisis

---

## ⚙️ Features

✅ IDX Web Scraping (Selenium)
✅ News Classification (Keyword-based NLP)
✅ Corporate Action Detection
✅ Transaction Value Extraction
✅ Weighted Scoring System
✅ Multi-source News Enrichment
✅ AI Prompt Generator

---

## 🧠 Pipeline Architecture

```text
IDX Announcements
        ↓
Scraping (Selenium)
        ↓
Cleaning & Filtering
        ↓
Keyword Classification
        ↓
Scoring Engine
        ↓
Top Emiten Selection
        ↓
News Enrichment
        ↓
Final Scoring
        ↓
AI Prompt Generation
```

---

## 📁 Project Structure

```bash
IDX-Event-Driven-Stock-Analysis/
│
├── notebooks/
│   └── IDX_Webscrap.ipynb       # Main pipeline (end-to-end)
│
├── data/
│   ├── raw/
│   │   └── idx_raw.csv
│   ├── processed/
│   │   ├── idx_company_summary.csv
│   │   ├── idx_top_10_emitten.csv
│   │   ├── search.csv
│   │   ├── articles.csv
│   │   └── final.csv
│
├── output/
│   └── prompt_final.txt         # AI-ready prompt
│
├── src/
│   ├── scraper.py              # Scraping IDX
│   ├── cleaner.py              # Data cleaning
│   ├── scoring.py              # Scoring logic
│   ├── enrichment.py           # News scraping tambahan
│   └── utils.py
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

## 🛠️ Tech Stack

* Python
* Selenium
* BeautifulSoup
* Pandas
* Regex
* Scikit-learn
* XGBoost / SVR / Ridge
* Jupyter Notebook

---

## ▶️ How to Run

### 1. Clone Repository

```bash
git clone https://github.com/your-username/idx-event-driven-analysis.git
cd idx-event-driven-analysis
```

---

### 2. Setup Environment

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
venv\Scripts\activate     # Windows
```

---

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

### 4. Setup WebDriver

Download:

* ChromeDriver sesuai versi Chrome

Lalu pastikan:

```bash
chromedriver ada di PATH
```

---

### 5. Run Pipeline

#### Opsi 1 — Notebook

```bash
jupyter notebook
```

Buka:

```
notebooks/IDX_Webscrap.ipynb
```

#### Opsi 2 — Script (jika sudah modular)

```bash
python src/scraper.py
python src/scoring.py
```

---

### 6. Output

Hasil akan tersedia di:

```bash
data/processed/
output/prompt_final.txt
```

---

## 📊 Example Output

* Top Emiten berdasarkan katalis
* Skor gabungan IDX + News
* Ringkasan berita relevan
* Prompt siap analisis AI

---

## 📈 Impact

### Sebelum

* Manual screening
* Noise tinggi
* Lambat

### Sesudah

* Automated pipeline
* Noise terfilter
* Fokus pada katalis penting
* Siap untuk AI analysis

---

## ⚠️ Limitations

* Rule-based (belum fully NLP model)
* Bergantung pada struktur website IDX
* Belum ada backtesting terhadap harga saham

---

## 🔮 Future Improvements

* Integrasi IndoBERT / LLM untuk klasifikasi
* Backtesting dengan data historis harga
* Dashboard (Streamlit / Tableau)
* Real-time alert (Telegram / WhatsApp)

---

## 📌 Key Insight

Pendekatan terbaik bukan sekadar scraping data, tapi:

> **mengubah data menjadi sinyal, dan sinyal menjadi keputusan.**

---

## 📄 License

MIT License — bebas digunakan dan dikembangkan.

---

## 🤝 Let's Connect

Jika tertarik berdiskusi:

* Data Science
* Quant Analysis
* AI for Finance

Silakan connect 🚀
