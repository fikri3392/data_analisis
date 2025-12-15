# Bank Marketing Campaign Analysis  
### Exploratory Data Analysis menggunakan Excel & PivotTable  
Dataset: [UCI Bank Marketing](https://archive.ics.uci.edu/dataset/222/bank+marketing)  
45211 records │ 17 fitur │ Target: apakah nasabah subscribe term deposit (yes/no)

## Objective
Menemukan pola dan segmen nasabah yang paling potensial untuk kampanye telemarketing berikutnya hanya dengan Excel PivotTable & Chart (tanpa coding).

## 5 Insight & Metrik Paling Krusial

| # | Insight Utama                                                 | Conversion Rate / Nilai Kunci                  | Rekomendasi Bisnis                                      |
|---|----------------------------------------------------------------|------------------------------------------------|----------------------------------------------------------|
| 1 | Hasil kampanye sebelumnya (poutcome) adalah prediktor terkuat | **success → 65 %**<br>failure → 16 %<br>unknown → 9 % | Prioritaskan daftar nasabah dengan **poutcome = success** |
| 2 | Bulan kontak sangat memengaruhi konversi                      | Mar (28.7 %), Sep (25.8 %), Oct (23.3 %), Dec (22.6 %)<br>Mei hanya **6.5 %** | Hindari kampanye besar-besaran di bulan Mei             |
| 3 | Segmen pekerjaan tertentu jauh lebih responsif                | Student → 28.5 %<br>Retired → 25.3 %<br>Blue-collar hanya 7 % | Fokuskan calling ke **student & retired**                |
| 4 | Nasabah tanpa cicilan rumah (housing loan = no) 2× lebih mungkin subscribe | No housing loan → **16.7 %**<br>Yes housing loan → 7.5 % | Filter prospek yang **tidak sedang cicil KPR**          |
| 5 | Durasi panggilan adalah indikator sukses real-time           | Rata-rata **537 detik** (yes)<br>vs **221 detik** (no) | Agent harus berusaha memperpanjang call > 6 menit       |

## Visualisasi (Excel Charts)

| No | Chart                                                                                   | File di Repo                     |
|----|------------------------------------------------------------------------------------------|----------------------------------|
| 1  | Conversion Rate by Previous Campaign Outcome (poutcome)                                 | `chart_poutcome.png`             |
| 2  | Conversion Rate by Month of Contact                                                     | `chart_month.png`                |
| 3  | Conversion Rate by Job Type                                                             | `chart_job.png`                  |
| 4  | Conversion Rate by Housing Loan Status (Donut Chart)                                    | `chart_housing.png`              |
| 5  | Average Call Duration (seconds) by Campaign Outcome                                     | `chart_duration.png`             |

![5 Key Charts](screenshots/all_5_charts.jpg)  
*Semua chart dibuat hanya dengan PivotTable + Insert Chart di Microsoft Excel*

## File dalam Repository
- `bank-full.csv` → dataset lengkap (45.211 baris)  
- `Bank_Marketing_Analysis_5_Key_Insights.xlsx` → file Excel lengkap (5 sheet + 5 chart)  
- `screenshots/` → gambar chart individual (untuk README ini)

## Kesimpulan & Rekomendasi Kampanye Berikutnya
Dengan menerapkan 5 filter berikut secara bersamaan, bank dapat meningkatkan conversion rate dari 11.7 % menjadi > 50 %:

1. `poutcome = success`  
2. `month` ∈ {mar, sep, oct, dec}  
3. `job` ∈ {student, retired}  
4. `housing = no`  
5. Target durasi telepon minimal 6–8 menit

Analisis ini 100 % dilakukan di Excel tanpa satu baris kode pun.

Terima kasih!  
Feel free to fork & adapt untuk portofolio Anda.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com/in/nama-anda)  