# Laporan Proyek Machine Learning - Luqman Hakim

## Daftar Isi

- [Domain Proyek](#domain-proyek)
- [Business Understanding](#business-understanding)
- [Data Understanding](#data-understanding)
- [Data Preparation](#data-preparation)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Referensi](#referensi)

## Domain Proyek

Emas telah lama dikenal sebagai salah satu instrumen investasi yang diminati secara global. Pergerakan nilainya dipengaruhi oleh sejumlah variabel seperti inflasi, kebijakan suku bunga, dinamika perekonomian dunia, serta tingkat permintaan terhadap komoditas logam mulia ini. Fluktuasi harga emas yang cukup dinamis membuat prediksi terhadap pergerakannya menjadi hal yang kompleks bagi para investor. [[1]](https://money.kompas.com/read/2025/03/22/081200526/faktor-faktor-ini-yang-pengaruhi-pergerakan-harga-emas?utm_source=Various&utm_medium=Referral&utm_campaign=Top_Desktop)

![fZ-2qwcv55LciXkKzUnU](https://github.com/user-attachments/assets/c7157372-9507-4901-94a7-aebbd70f2194)


**Gambar 1. Ilustrasi Gold (Emas)**

Dalam hal ini, pemanfaatan teknologi Machine Learning (ML) menjadi alternatif yang menjanjikan untuk melakukan prediksi harga emas di masa yang akan datang. Teknologi ini mampu mengidentifikasi pola dari data historis harga emas, sehingga dapat digunakan untuk menghasilkan estimasi pergerakan harga secara lebih akurat berdasarkan pembelajaran dari data terdahulu.

Adapun dataset yang digunakan dalam studi ini mencakup data harga emas dari tahun 2009 hingga 2018, dengan rata-rata harga per tahunnya sebagai berikut:

| _Year_ | _Gold_ |
| ------ | ------ |
| 2008   | 86.11  |
| 2009   | 95.83  |
| 2010   | 119.97 |
| 2011   | 152.59 |
| 2012   | 162.15 |
| 2013   | 136.85 |
| 2014   | 121.72 |
| 2015   | 111.17 |
| 2016   | 118.78 |
| 2017   | 119.55 |
| 2018   | 126.02 |

## Business Understanding

### Problem Statements

1. Emas merupakan salah satu aset investasi paling populer secara global. Namun, prediksi terhadap fluktuasi harganya menjadi tantangan besar bagi para investor karena harga emas sangat sensitif terhadap berbagai variabel ekonomi.
   Beberapa faktor utama yang memengaruhi nilai emas antara lain:

- Inflasi
  Kenaikan inflasi biasanya menyebabkan menurunnya daya beli uang. Dalam kondisi ini, investor cenderung mengalihkan asetnya ke emas sebagai bentuk perlindungan nilai, sehingga harga emas meningkat.

- Keadaan Ekonomi Dunia
  Ketidakpastian dalam ekonomi global, krisis keuangan, atau instabilitas geopolitik sering kali mendorong investor untuk beralih ke emas sebagai aset aman, yang biasanya mendorong harga emas naik.

- Tingkat Suku Bunga
  Kenaikan suku bunga membuat instrumen investasi lain seperti deposito dan obligasi menjadi lebih menarik. Hal ini dapat menurunkan minat terhadap emas, menyebabkan harga emas turun.

- Permintaan dan Pasokan
  Fluktuasi dalam permintaan industri maupun cadangan emas oleh bank sentral berpengaruh langsung terhadap harga. Ketidakseimbangan antara permintaan dan penawaran akan menciptakan tekanan harga.

- Kurs Dolar AS
  Karena emas dihargai dalam dolar AS, penguatan atau pelemahan dolar akan berdampak pada harga emas. Ketika dolar melemah, harga emas cenderung menguat.

- Spekulasi Investor dan Psikologi Pasar
  Reaksi emosional pasar, seperti kepanikan atau euforia, serta aktivitas spekulatif bisa memicu pergerakan harga emas yang tidak selalu mencerminkan kondisi fundamental.

- Situasi Geopolitik
  Konflik internasional dan ketegangan politik sering memicu lonjakan harga emas karena tingginya permintaan atas aset yang dianggap stabil dan aman.

2. Teknologi Machine Learning (ML) telah berkembang menjadi alat bantu potensial dalam memprediksi tren harga emas. Dengan kemampuan mempelajari pola dari data historis, ML memberikan pendekatan analitis berbasis data. Namun demikian, prediksi yang dihasilkan masih belum sepenuhnya akurat karena tingginya kompleksitas pasar emas. Oleh karena itu, analisis berbasis ML perlu dikombinasikan dengan strategi manajemen risiko dan diversifikasi investasi untuk mendukung pengambilan keputusan yang lebih tepat.

### Goals

1. Meningkatkan performa model prediksi harga emas melalui penerapan algoritma Machine Learning yang lebih modern, efektif, dan adaptif. Tujuan ini mencakup pengembangan model yang responsif terhadap dinamika pasar yang kompleks dan volatil, dengan pendekatan analitis yang lebih presisi dan berdaya saing.

2. Menyediakan wawasan analitis yang bermanfaat bagi investor guna menunjang pengambilan keputusan investasi emas secara strategis dan berbasis data. Prediksi harga emas yang akurat diharapkan mampu mengurangi ketidakpastian dan risiko yang melekat pada instrumen investasi ini. Informasi yang disajikan antara lain:

- Analisis faktor ekonomi makro seperti inflasi, suku bunga, serta ketegangan geopolitik yang dapat mempengaruhi pergerakan harga emas, sehingga investor dapat memahami latar belakang pergerakan harga secara lebih mendalam.

- Pola historis harga emas yang ditampilkan dalam bentuk visualisasi tren dan analisis teknikal, guna mendukung investor dalam mengidentifikasi momen terbaik untuk melakukan aksi beli atau jual.

- Sentimen pasar terkini, baik yang berasal dari berita ekonomi maupun opini analis, membantu memetakan persepsi pasar terhadap situasi global yang sedang berlangsung.

- Prediksi harga berbasis model ML yang dihasilkan dari data historis dan variabel pendukung lainnya, menjadi alat bantu utama dalam merancang strategi investasi masa depan.

- Konsep diversifikasi aset, yang menjelaskan peran emas dalam struktur portofolio investasi agar risiko keseluruhan dapat diminimalkan.

- Strategi manajemen risiko investasi emas, yang mencakup perlindungan terhadap fluktuasi harga dan instrumen mitigasi risiko seperti derivatif.

- Pilihan instrumen investasi berbasis emas termasuk ETF, kontrak berjangka, atau saham tambang emas, yang disesuaikan dengan profil risiko dan tujuan finansial investor.

- Evaluasi terhadap biaya investasi, seperti biaya penyimpanan fisik emas atau biaya pengelolaan instrumen berbasis emas, agar investor dapat menghitung estimasi keuntungan bersih secara lebih tepat.

### Solution statements

1. Salah satu metode untuk meningkatkan akurasi prediksi harga emas adalah dengan menggunakan teknik ensemble learning yang mengombinasikan berbagai model Machine Learning. Karena setiap algoritma memiliki keunikan dan performa yang berbeda tergantung pada jenis data, pendekatan ini memungkinkan kelebihan masing-masing model untuk saling melengkapi. Contohnya, algoritma Linear Regression dapat dimanfaatkan untuk menangkap pola tren jangka panjang, sedangkan Random Forest Regression dapat digunakan untuk menangani fluktuasi harga jangka pendek yang lebih kompleks dan variatif.

2. Strategi lainnya adalah dengan melakukan penyempurnaan terhadap model awal melalui proses penyesuaian parameter yang dikenal sebagai hyperparameter tuning. Model baseline yang belum dioptimalkan cenderung memberikan hasil prediksi yang kurang akurat. Oleh karena itu, mengatur nilai-nilai hyperparameter—yang merupakan parameter eksternal dari model—secara cermat dapat menghasilkan performa model yang lebih baik. Proses ini melibatkan pencarian kombinasi nilai parameter terbaik melalui pendekatan seperti grid search atau random search, sehingga model dapat menghasilkan estimasi harga emas dengan tingkat presisi yang lebih tinggi.

## Data Understanding

Dataset yang digunakan dalam proyek ini adalah dataset [Gold Price Prediction](https://www.kaggle.com/datasets/altruistdelhite04/gold-price-data) yang diambil dari platform Kaggle. _File_ yang digunakan berupa _file_ csv, yaitu `gld_price_data.csv`.

Dataset ini disimpan dalam format Comma Separated Values (CSV) dan terdiri dari 2290 entri dengan total 6 atribut. Lima atribut di antaranya bertipe numerik, sementara satu kolom lainnya merupakan data bertipe tanggal. Data ini mencatat nilai variabel SPX, GLD, USO, SLV, serta EUR/USD yang terorganisasi berdasarkan tanggal.

- DATE
  Menunjukkan tanggal pengambilan data dalam dataset, yang disajikan dalam format bulan/tanggal/tahun (mm/dd/yyyy).

- SPX
  Merupakan indeks S&P 500, yaitu indeks saham yang merepresentasikan performa 500 perusahaan besar yang tercatat di bursa saham Amerika Serikat. SPX dikenal sebagai salah satu indikator utama dalam pasar keuangan global.

- GLD
  Mengacu pada SPDR Gold Shares, sebuah Exchange-Traded Fund (ETF) yang memiliki kepemilikan emas fisik sebagai aset dasarnya. GLD termasuk ETF berbasis emas yang paling populer secara global.

- USO
  Merupakan singkatan dari United States Oil Fund, yaitu ETF yang berfokus pada investasi di kontrak berjangka minyak mentah jenis West Texas Intermediate (WTI). USO menjadi salah satu ETF minyak yang paling banyak diperdagangkan.

- SLV
  Adalah iShares Silver Trust, ETF yang mencerminkan harga perak fisik melalui kepemilikan langsung. SLV merupakan salah satu produk ETF utama yang mewakili komoditas perak.

- EUR/USD
  Merupakan kurs pasangan mata uang euro terhadap dolar Amerika Serikat. Pasangan ini termasuk salah satu yang paling aktif diperdagangkan di pasar valuta asing (forex).

**Tabel 1. Deskripsi variabel**
| # | Column | Non-Null Count | Dtype |
|---|-----------|----------------|---------|
| 0 | Date | 2290 non-null | object |
| 1 | SPX | 2290 non-null | float64 |
| 2 | GLD | 2290 non-null | float64 |
| 3 | USO | 2290 non-null | float64 |
| 4 | SLV | 2290 non-null | float64 |
| 5 | EUR/USD | 2290 non-null | float64 |

Berdasarkan output di atas, terdapat 5 kolom dengan tipe data float64, 1 kolom dengan tipe data objek.

**Tabel 2 : Deskripsi Statistik Dataset**  
| Desc | SPX | GLD | USO | SLV | EUR/USD |
|-------|---------|---------|---------|---------|---------|
| count | 2290.00 | 2290.00 | 2290.00 | 2290.00 | 2290.00 |
| mean | 1654.32 | 122.73 | 31.84 | 20.85 | 1.28 |
| std | 519.11 | 23.28 | 19.52 | 7.09 | 0.13 |
| min | 676.53 | 70.00 | 7.96 | 8.85 | 1.04 |
| 25% | 1239.87 | 109.73 | 14.38 | 15.57 | 1.17 |
| 50% | 1551.43 | 120.58 | 33.87 | 17.27 | 1.30 |
| 75% | 2073.01 | 132.84 | 37.83 | 22.88 | 1.37 |
| max | 2872.87 | 184.59 | 117.48 | 47.26 | 1.60 |

Berdasarkan output diatas memberikan informasi mengenai statistik dataset yaitu count(jumlah data), mean(nilai rata-rata), std(standard deviasi), min(nilai terendah), 25%(quartil 1), 50%(median), 75%(quartil 3) dan max(nilai tertinggi).

Grafik 1: Menampilkan pola korelasi variabel dengan pairplot
![download](https://github.com/user-attachments/assets/3586e65c-966d-446d-90dd-0db47bfa2a6a)


## Data Preparation

Langkah-langkah dalam Menyiapkan Data

1. Mengimpor library dan memuat dataset:
   Langkah awal ini bertujuan untuk menyiapkan lingkungan kerja dengan memuat pustaka Python seperti pandas, numpy, dan pustaka lain yang relevan. Dataset kemudian diambil dari sumber yang tersedia, seperti file CSV, Excel, atau basis data, untuk diproses lebih lanjut. Tahap ini merupakan dasar sebelum memasuki proses analisis.

2. Meninjau struktur data:
   Pemeriksaan awal data bertujuan untuk mendapatkan pemahaman umum terhadap isi dataset, mengidentifikasi kemungkinan adanya data yang tidak valid, serta mengevaluasi kelengkapan dan tipe data tiap kolom. Kegiatan ini biasanya melibatkan pengecekan dimensi dataset, contoh baris, informasi tipe data, nilai kosong, dan ringkasan statistik.

3. Eksplorasi data lebih lanjut:
   Proses ini berfokus pada analisis visual dan statistik guna menemukan pola tersembunyi atau hubungan antar variabel. Diagram seperti histogram, scatter plot, dan box plot digunakan untuk memahami distribusi dan interaksi antar fitur. Analisis ini membantu dalam merumuskan hipotesis awal atau mengarahkan pemilihan model.

4. Membersihkan dataset:
   Data yang diperoleh sering mengandung ketidaksempurnaan seperti nilai hilang, anomali (outlier), atau kesalahan entri. Oleh karena itu, proses pembersihan dilakukan dengan cara menghapus atau memperbaiki nilai-nilai tersebut, menyaring kolom yang tidak relevan, serta melakukan transformasi data agar lebih konsisten dan siap dianalisis.

5. Membagi data menjadi subset:
   Untuk membangun model machine learning yang dapat diandalkan, data perlu dipisahkan menjadi dua bagian: satu untuk pelatihan (training set) dan lainnya untuk pengujian (testing set). Rasio umum yang digunakan adalah 70:30 atau 80:20. Tujuannya adalah untuk memastikan bahwa model diuji pada data yang belum pernah dilihat sebelumnya, sehingga performanya dapat dievaluasi secara objektif.

6. Menyelaraskan skala data (normalisasi):
   Ketika fitur dalam dataset memiliki skala nilai yang sangat bervariasi, hal ini dapat memengaruhi performa beberapa algoritma. Normalisasi atau standarisasi digunakan untuk menyetarakan skala seluruh variabel agar algoritma seperti regresi linier atau k-means dapat bekerja lebih optimal. Teknik populer termasuk Min-Max Scaling, StandardScaler, dan Z-Score, serta pendekatan lanjutan seperti PCA bila diperlukan.

## Modeling

1. Linier Regression
   Konsep Dasar:
   Regresi linier adalah metode statistik yang digunakan untuk memodelkan hubungan antara satu atau lebih variabel independen dengan variabel dependen melalui garis lurus. Model ini berusaha mengestimasi koefisien yang menghubungkan fitur dengan target sehingga dapat memprediksi nilai target berdasarkan data masukan.

Kelebihan:

Mudah Dipahami dan Dijelaskan: Pendekatan ini menghasilkan model yang transparan berupa persamaan linear, sehingga pengguna bisa memahami kontribusi masing-masing fitur.

Efisien untuk Hubungan Linier: Sangat efektif bila data memiliki pola hubungan linier, memberikan hasil prediksi yang solid dalam konteks tersebut.

Cepat dalam Komputasi: Model ini ringan untuk dilatih dan sangat cepat dalam proses prediksi.

Kekurangan:

Rentan terhadap Nilai Ekstrem: Model dapat terdistorsi oleh keberadaan outlier karena sifatnya yang sensitif terhadap perubahan ekstrem pada data.

Tidak Cocok untuk Pola Kompleks: Jika hubungan antar variabel bersifat non-linier, model ini akan menghasilkan prediksi yang kurang akurat.

Parameter Umum:

copy_X: Menentukan apakah data fitur disalin saat pelatihan berlangsung. Default: True.

fit_intercept: Apakah model harus menghitung nilai bias (intercept). Default: True.

n_jobs: Jumlah core CPU yang digunakan untuk komputasi paralel. Default: None.

positive: Menentukan apakah koefisien regresi hanya boleh bernilai positif. Default: False.

coefficients: Koefisien regresi yang menunjukkan kontribusi masing-masing fitur terhadap prediksi.

2. Random Forest Regressor
   Konsep Dasar:
   Random Forest merupakan algoritma berbasis ensemble learning yang menggunakan banyak pohon keputusan (decision tree) untuk menghasilkan prediksi regresi. Hasil akhir prediksi adalah rata-rata dari semua pohon yang dibentuk selama proses pelatihan, sehingga meningkatkan stabilitas dan akurasi model.

Kelebihan:

Akurat dan Tahan Terhadap Overfitting: Dengan menggabungkan hasil dari banyak pohon, Random Forest mampu mengurangi varians dan meminimalkan overfitting yang umum terjadi pada pohon tunggal.

Dapat Menangani Hubungan Non-linear: Mampu mengatasi pola yang kompleks antara fitur dan target tanpa perlu transformasi fitur secara manual.

Tahan Terhadap Outlier dan Nilai Hilang: Model ini tetap dapat bekerja dengan baik walaupun data mengandung anomali atau nilai yang tidak lengkap.

Kekurangan:

Kurang Interpretatif: Berbeda dengan regresi linier, sulit untuk memahami secara langsung bagaimana setiap fitur memengaruhi hasil karena model terdiri dari banyak pohon.

Butuh Sumber Daya Lebih Banyak: Proses pelatihan dan prediksi bisa memakan waktu lebih lama dan membutuhkan memori lebih besar, terutama jika jumlah pohon sangat banyak.

Tuning Parameter yang Kompleks: Parameter seperti jumlah pohon (n_estimators) atau kedalaman maksimal (max_depth) harus disesuaikan agar mendapatkan kinerja optimal.

Parameter Umum:

n_estimators: Jumlah pohon dalam hutan.

max_depth: Kedalaman maksimum masing-masing pohon.

min_samples_split: Jumlah minimum sampel yang dibutuhkan untuk membagi simpul internal.

random_state: Untuk memastikan hasil yang reprodusibel.

n_jobs: Menentukan jumlah CPU core yang digunakan secara paralel.

## Evaluation

Untuk mengukur akurasi prediksi harga emas, digunakan beberapa metrik evaluasi berikut:

1. Mean Absolute Error (MAE)

- MAE menghitung rata-rata dari selisih absolut antara nilai aktual dan nilai prediksi, dengan menggunakan rumus
- MAE = (1/n) × Σ |actual - predicted|.
- Semakin kecil nilai MAE, semakin akurat prediksi model terhadap data sebenarnya, dan metrik ini kurang sensitif terhadap outlier.

2. Mean Squared Error (MSE)

- MSE menghitung rata-rata dari kuadrat selisih antara nilai aktual dan prediksi, melalui rumus
- MSE = (1/n) × Σ (actual - predicted)².
- Nilai MSE yang lebih kecil menunjukkan kesalahan prediksi yang rendah, namun karena sifatnya mengkuadratkan selisih, MSE lebih sensitif terhadap kesalahan besar atau outlier.

3. Coefficient of Determination (R²)

- R² atau koefisien determinasi menunjukkan proporsi variabilitas target yang dapat dijelaskan oleh model, dengan rumus
- R² = 1 - (MSE_model / MSE_mean).
- Nilai R² berkisar antara 0 hingga 1, di mana semakin mendekati 1, berarti model semakin baik dalam menjelaskan variasi data.

Ringkasan Perbandingan

- MAE memberikan ukuran kesalahan yang mudah dipahami dalam satuan yang sama dengan target.

- MSE lebih sensitif terhadap prediksi yang jauh meleset, cocok jika kesalahan besar ingin ditekan.

- R² menunjukkan sejauh mana model dapat menjelaskan variasi data, memberikan perspektif kecocokan model secara keseluruhan.

### Memilih model yang terbaik berdasarkan metrik evaluasi

Tabel 4 : Skor MAE, MSE dan R2 dengan parameter cv=5  
| | MAE _Train_| MAE _Test_|MSE _Train_|MSE _Test_|R2 _Train_|R2 _Test_|
|-------------------|------------|-----------|-----------|----------|----------|---------|
| Linear Regression | 8.343 | 8.018 | 132.806 | 126.818 | 0.683 | 0.691 |
| Random Forest Regressor | 0.831 | 2.197 | 4.363 | 33.551 | 0.990 | 0.918 |

Berdasarkan output diatas menunjukkan perbandingan performa dua model regresi berdasarkan tiga metrik utama: MAE, MSE, dan R2.
Model Random Forest Regressor memperlihatkan performa yang lebih baik secara keseluruhan, terutama pada nilai MAE dan MSE yang jauh lebih kecil dibandingkan dengan Linear Regression, serta nilai R2 yang jauh lebih mendekati 1.

**Kesimpulan**:

1. **MAE (Mean Absolute Error)**:  
   Menunjukkan rata-rata kesalahan absolut prediksi. Semakin kecil nilai MAE, semakin presisi model dalam memprediksi nilai target.

2. **MSE (Mean Squared Error)**:  
   Mengkuadratkan selisih antara nilai prediksi dan aktual, sehingga lebih sensitif terhadap kesalahan besar. Nilai MSE yang rendah menunjukkan prediksi yang stabil dan akurat.

3. **R-squared (R2)**:  
   Menjelaskan seberapa baik variasi data target dijelaskan oleh model. Semakin tinggi nilai R², semakin besar proporsi variasi yang dapat dijelaskan.

Berdasarkan hasil permodelan dan evaluasi, model terbaik untuk diterapkan pada dataset prediksi emas adalah **Random Forest Regressor**

## Referensi

[1] Faktor-faktor Ini yang Pengaruhi Pergerakan Harga Emas (https://money.kompas.com/read/2025/03/22/081200526/faktor-faktor-ini-yang-pengaruhi-pergerakan-harga-emas?utm_source=Various&utm_medium=Referral&utm_campaign=Top_Desktop)
