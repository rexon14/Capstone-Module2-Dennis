# Strategi Diskon Optimal: Analisis AWS SaaS Sales

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)
![Status](https://img.shields.io/badge/Status-Completed-success.svg)

## 📋 Deskripsi Project

Capstone Project Module 2 - Data Analysis yang menganalisis **pengaruh diskon terhadap profitabilitas** pada perusahaan SaaS B2B. Project ini bertujuan menentukan tingkat diskon optimal untuk memaksimalkan penjualan tanpa mengorbankan profit.

## 🎯 Problem Statement

> *"Bagaimana menentukan tingkat diskon yang optimal agar dapat meningkatkan penjualan tanpa menurunkan profitabilitas?"*

## 📊 Dataset

- **Sumber**: [AWS SaaS Sales Dataset (Kaggle)](https://www.kaggle.com/datasets/nnthanh101/aws-saas-sales)
- **Periode**: Januari 2020 - Desember 2023
- **Total Transaksi**: 9,994 baris
- **Jumlah Variabel**: 19 kolom

### Variabel Utama
| Variabel | Deskripsi |
|----------|-----------|
| Sales | Nilai penjualan ($) |
| Profit | Keuntungan ($) |
| Discount | Persentase diskon (0-80%) |
| Segment | SMB, Strategic, Enterprise |
| Region | EMEA, AMER, APJ |
| Product | 14 jenis produk software |

## 🔍 Metodologi

1. **Data Understanding** - Eksplorasi struktur dan karakteristik data
2. **Data Cleaning** - Penanganan missing values, duplicates, outliers
3. **Exploratory Data Analysis (EDA)** - Visualisasi distribusi dan pola data
4. **Statistical Analysis**:
   - Analisis korelasi (Pearson)
   - Uji normalitas (Shapiro-Wilk)
   - Uji Kruskal-Wallis (non-parametrik)
5. **Threshold Analysis** - Penentuan batas diskon optimal

## 📈 Key Findings

| Temuan | Detail |
|--------|--------|
| Korelasi Diskon vs Profit | **r = -0.22** (negatif signifikan, p < 0.001) |
| Transaksi Rugi | **18.7%** transaksi menghasilkan profit negatif |
| Threshold Kritis | Diskon **≥30%** → 87-100% transaksi rugi |
| Batas Aman | Diskon **≤20%** masih menghasilkan profit positif |

### Kategori Risiko Diskon
- ✅ **Aman (0-20%)**: <35% transaksi rugi
- ⚠️ **Waspada (21-30%)**: 50-90% transaksi rugi  
- ❌ **Bahaya (>30%)**: 87-100% transaksi rugi

## 💡 Rekomendasi

1. **Batas Maksimal Diskon 20%** - Implementasi kebijakan batas diskon
2. **Review Transaksi Diskon Tinggi** - Evaluasi kontrak dengan diskon >30%
3. **Strategi Diskon per Segmen**:
   - Enterprise: max 15-20%
   - Strategic: max 15%
   - SMB: max 10%
4. **Alternatif Diskon** - Value-added services, volume pricing
5. **Monitoring Dashboard** - Real-time tracking diskon dan profitabilitas

## 🛠️ Tools & Libraries

```
pandas==2.0.0
numpy==1.24.0
matplotlib==3.7.0
seaborn==0.12.0
scipy==1.10.0
```

## 📊 Tableau Dashboard

[Link Dashboard Tableau Public] *https://public.tableau.com/app/profile/dennis.schira/viz/CapstoneProject_M2_DennisSchira/Dashboard-Page1?publish=yes*

## 👤 Author

**Dennis Schira**  
Capstone Project Module 2 - Data Science & Machine Learning Bootcamp
---

*Dibuat sebagai bagian dari Capstone Project Module 2 - Data Analysis*
