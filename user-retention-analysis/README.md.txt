# **user retention cohort analysis**

## **User retention analysis** digunakan sebagai metode untuk mengevaluasi seberapa efektif suatu bisnis dalam mempertahankan user pelanggan yang sudah ada. 
## Dengan adanya user yang loyal dan terus kembali untuk bertransaksi atau menggunakan produk kita akan menghasilkan keuntungan bagi bisnis kita.

## **Cohort** merupakan suatu kelompok yang mempunyai kesamaan,seperti tanggal pendaftaran, bulan pembelian, dan lokasi geografis. 
## Cohort analysis merupakan proses mengidentifikasi kelompok user atau pengguna ini dari waktu ke waktu sehingga kita dapat mengidentifikasi pola atau perilaku umum user atau pengguna.

## repository
/user-retention-analysis
	|___ data/raw/online_retail.xlsx
	|___ image/user_retention_cohort.png
	|___ notebook/user_retention.ipynb
	|___ README.md

## Tujuan analisis
* mengetahui retention rate berdasarkan kohort dalam periode bulan

## dataset
* https://archive.ics.uci.edu/dataset/352/online+retail

## tools
* Jupyter notebook. package : pandas, numpy, matplotlib, seaborn

## metriks
1. periode transaksi (year_month)
2. jarak transaksi terakhir ke transaksi pertama
3. total transaksi per user tiap bulan
4. kohort bulan transaksi
5. banyaknya user di masing-masing kohort

## wawasan
| **temuan** | **deskripsi** |
| ---- | ---- |
| desember 2010 menjadi bulan dengan user terbanyak | jumlah user 949 |
| retention rate stabil | min 28% max 50% average 38% |
| bulan setelahnya rate turun dibawah 30% | januari 2011 retention rate hanya 24% |
| desember 2011 menjadi bulan dengan user paling sedikit | jumlah user baru hanya 41 |