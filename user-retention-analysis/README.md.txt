# Analisis Data Online Retail - Customer Retention Cohort

## Pendahuluan

Proyek ini bertujuan untuk menganalisis data transaksi dari **Online Retail** (bersumber dari UCI Machine Learning Repository) guna memahami perilaku pembelian pelanggan, mengevaluasi tingkat retensi, dan mendapatkan wawasan strategis untuk meningkatkan nilai pelanggan (*Customer Lifetime Value*).

Analisis utama berfokus pada **Cohort Analysis** untuk melacak retensi pelanggan dari waktu ke waktu.

## Sumber Data

* **Nama Dataset:** Online Retail Data Set
* **Sumber:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Online+Retail)
* **Periode Data:** 01/12/2010 hingga 09/12/2011.
* **Fokus Analisis:** Transaksi dari pelanggan yang terdaftar di Britania Raya.

## Teknologi dan Pustaka yang Digunakan

Proyek ini dikembangkan menggunakan **Python** dan didukung oleh pustaka-pustaka utama untuk analisis data dan visualisasi:

* **Python 3.x**
* **Pandas:** Manipulasi dan pembersihan data.
* **NumPy:** Komputasi numerik.
* **Matplotlib & Seaborn:** Visualisasi data (khususnya untuk *Heatmap Cohort*).

## Hasil dan Wawasan Utama

### 1. Pembersihan Data (*Data Preprocessing*)

Langkah-langkah pembersihan data meliputi:
* Penghapusan baris dengan `CustomerID` yang hilang.
* Penanganan transaksi yang dibatalkan (diidentifikasi dari `InvoiceNo` yang dimulai dengan 'C').
* Penghapusan anomali (misalnya, harga satuan atau kuantitas negatif).
* Penghitungan dan penentuan *First Order Month* (`CohortMonth`) untuk setiap pelanggan.

### 2. Analisis Kohort Retensi Pengguna (*User Retention Cohort Analysis*)

Analisis ini mengelompokkan pelanggan berdasarkan bulan pembelian pertama mereka (`First Order Month`) dan melacak persentase mereka yang kembali bertransaksi di bulan-bulan berikutnya (`Month Number`).

#### **Visualisasi Kohort Retensi**

![User Retention Cohort Heatmap](user_retention_cohort.png)

#### **Wawasan Kunci:**

* **Penurunan Retensi Awal:** Terjadi penurunan drastis dalam retensi dari Bulan 1 ke Bulan 2 di hampir semua kohort (misalnya, Kohort 2010-12 turun dari 100% menjadi 38%), menunjukkan bahwa banyak pelanggan tidak melakukan pembelian kedua segera.
* **Stabilitas Kohort Senior:** Kohort yang lebih tua (e.g., 2010-12, 2011-01) menunjukkan tingkat retensi yang lebih stabil dalam jangka panjang (bulan 6 hingga 13), bahkan mempertahankan retensi di atas 30% setelah setahun, menunjukkan adanya kelompok pelanggan setia.
* **Tantangan Retensi Kohort Baru:** Kohort yang baru bergabung (terutama pertengahan 2011) memiliki tingkat retensi bulanan yang sangat rendah dan cepat memudar (ditandai dengan warna merah tua), mengindikasikan adanya isu pada strategi *onboarding* atau kualitas penawaran untuk pelanggan baru.
* **Rekomendasi Strategis:** Fokus pada inisiatif retensi yang ditargetkan dalam **2-3 bulan pertama** setelah pembelian awal untuk mengubah pelanggan satu kali beli menjadi pelanggan berulang.

## Struktur Proyek
user-retention-analysis
├───data
│   └───raw/online_retail.xlsx
├───image/user_retention_cohort.png
└───notepad/user_retention.ipynb

## Cara Menjalankan Proyek

1.  **Clone Repositori:**
    ```bash
    git clone [https://github.com/fikri3392/data_analisis.git](https://github.com/YourUsername/YourRepoName.git)
    cd YourRepoName
    ```
2.  **Instal Dependensi:**
    ```bash
    # Pastikan Anda memiliki environment management (conda/venv) aktif
    pip install -r requirements.txt 
    ```
    *(Buat file `requirements.txt` yang mencantumkan `pandas`, `numpy`, `matplotlib`, `seaborn`, dll.)*
3.  **Jelajahi Analisis:** Buka *Jupyter Notebook* atau *JupyterLab* di direktori proyek dan ikuti alur analisis di folder `notebooks/`.

## Kontribusi

Saran, perbaikan, atau tambahan analisis (misalnya, analisis RFM, *clustering*) sangat disambut baik! Silakan buka *Issue* atau kirimkan *Pull Request*.

## Penulis

* [Fikri Miftahurrohman] - [https://www.linkedin.com/in/fikri-miftahurrohman-14413b399]

---