# 📊 Pemodelan Stokastik Kepadatan Pengunjung Perpustakaan GK1 ITERA

**Tim:**  
 • Mayada (121450145) 
 • Gymnastiar Al Khoarizmy (122450096) 
 • Dwi Sulistiani (121450079) 
 • Evan Aprianto (121450024) 
 • Pramudya Wibowo (121450030)

## 📌 Deskripsi
Repository ini berisi kode dan hasil analisis pemodelan stokastik kepadatan pengunjung harian Perpustakaan GK1 ITERA menggunakan metode Rantai Markov Waktu Diskrit (Discrete-Time Markov Chain/DTMC).

## 🔍 Tujuan
- Mengidentifikasi pola transisi kepadatan pengunjung harian (rendah, sedang, tinggi)
- Membangun matriks probabilitas transisi dan diagram visualisasi
- Menganalisis distribusi stasioner dan Mean First Passage Time (MFPT)
- Memberikan insight untuk optimasi alokasi sumber daya perpustakaan

## 🛠 Metodologi
- **Data**: Log kunjungan harian Perpustakaan GK1 ITERA (September-Oktober 2025)
- **Klasifikasi State**: Berdasarkan metode kuantil data positif:
  - **Rendah**: ≤ 61 pengunjung/hari
  - **Sedang**: 62-105 pengunjung/hari
  - **Tinggi**: ≥ 106 pengunjung/hari
- **Analisis**:
  - Matriks probabilitas transisi satu langkah
  - Distribusi stasioner (steady-state)
  - Mean First Passage Time (MFPT)
  - Visualisasi heatmap dan diagram transisi

## 📈 Hasil Utama
- **State persisten**: State "Rendah" (p=0.77) dan "Tinggi" (p=0.67) memiliki probabilitas bertahan tinggi
- **Distribusi stasioner**: 
  - Rendah: 51.67%
  - Sedang: 23.33% 
  - Tinggi: 25.00%
- **MFPT**: Waktu rata-rata dari state "Rendah" ke "Tinggi" adalah 9.31 hari
- **Sifat rantai**: Ergodik (irreducible dan aperiodik) sehingga memiliki distribusi stasioner unik

## 💻 Dependensi R
```r
library(markovchain)
library(tidyverse)
library(ggplot2)
library(ggpubr)
library(knitr)
