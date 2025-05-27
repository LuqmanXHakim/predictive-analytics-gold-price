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

![Image](https://github.com/user-attachments/assets/62c94c8e-8b8e-4f5f-9bc1-a2a7740fcd03)
**Gambar 1. Ilustrasi Gold (Emas)**

Dalam hal ini, pemanfaatan teknologi Machine Learning (ML) menjadi alternatif yang menjanjikan untuk melakukan prediksi harga emas di masa yang akan datang. Teknologi ini mampu mengidentifikasi pola dari data historis harga emas, sehingga dapat digunakan untuk menghasilkan estimasi pergerakan harga secara lebih akurat berdasarkan pembelajaran dari data terdahulu.

Adapun dataset yang digunakan dalam studi ini mencakup data harga emas dari tahun 2009 hingga 2018, dengan rata-rata harga per tahunnya sebagai berikut:

|*Year*| *Gold*|
|------|-------|    
| 2008 | 86.11 |    
| 2009 | 95.83 |    
| 2010 | 119.97|    
| 2011 | 152.59|    
| 2012 | 162.15|    
| 2013 | 136.85|    
| 2014 | 121.72|    
| 2015 | 111.17|    
| 2016 | 118.78|    
| 2017 | 119.55|    
| 2018 | 126.02|  


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

Dataset yang digunakan dalam proyek ini adalah dataset [Gold Price Prediction](https://www.kaggle.com/datasets/altruistdelhite04/gold-price-data) yang diambil dari platform Kaggle. *File* yang digunakan berupa *file* csv, yaitu `gld_price_data.csv`.

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
   | # | Column    | Non-Null Count | Dtype   |
   |---|-----------|----------------|---------|
   | 0 | Date      | 2290 non-null  | object  |
   | 1 | SPX       | 2290 non-null  | float64 |
   | 2 | GLD       | 2290 non-null  | float64 |
   | 3 | USO       | 2290 non-null  | float64 |
   | 4 | SLV       | 2290 non-null  | float64 |
   | 5 | EUR/USD   | 2290 non-null  | float64 |

   Berdasarkan output di atas, terdapat 5 kolom dengan tipe data float64, 1 kolom dengan tipe data objek.

**Tabel 2 : Deskripsi Statistik Dataset**      
| Desc  |   SPX   |   GLD   |   USO   |   SLV   | EUR/USD |
|-------|---------|---------|---------|---------|---------|
| count | 2290.00 | 2290.00 | 2290.00 | 2290.00 | 2290.00 |
|  mean | 1654.32 |  122.73 |   31.84 |   20.85 |    1.28 |
|  std  |  519.11 |   23.28 |   19.52 |    7.09 |    0.13 |
|  min  |  676.53 |   70.00 |    7.96 |    8.85 |    1.04 |
|  25%  | 1239.87 |  109.73 |   14.38 |   15.57 |    1.17 |
|  50%  | 1551.43 |  120.58 |   33.87 |   17.27 |    1.30 |
|  75%  | 2073.01 |  132.84 |   37.83 |   22.88 |    1.37 |
|  max  | 2872.87 |  184.59 |  117.48 |   47.26 |    1.60 | 

Berdasarkan output diatas  memberikan informasi mengenai statistik dataset yaitu count(jumlah data), mean(nilai rata-rata), std(standard deviasi), min(nilai terendah), 25%(quartil 1), 50%(median), 75%(quartil 3) dan max(nilai tertinggi).

Grafik 1: Menampilkan pola korelasi variabel dengan pairplot
![Image](https://github.com/user-attachments/assets/7eeac763-68cb-4e02-b58e-68c7f5f99867)

**Rubrik/Kriteria Tambahan (Opsional)**:
- Melakukan beberapa tahapan yang diperlukan untuk memahami data, contohnya teknik visualisasi data atau exploratory data analysis.

## Data Preparation
Pada bagian ini Anda menerapkan dan menyebutkan teknik data preparation yang dilakukan. Teknik yang digunakan pada notebook dan laporan harus berurutan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan proses data preparation yang dilakukan
- Menjelaskan alasan mengapa diperlukan tahapan data preparation tersebut.

## Modeling
Tahapan ini membahas mengenai model machine learning yang digunakan untuk menyelesaikan permasalahan. Anda perlu menjelaskan tahapan dan parameter yang digunakan pada proses pemodelan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan kelebihan dan kekurangan dari setiap algoritma yang digunakan.
- Jika menggunakan satu algoritma pada solution statement, lakukan proses improvement terhadap model dengan hyperparameter tuning. **Jelaskan proses improvement yang dilakukan**.
- Jika menggunakan dua atau lebih algoritma pada solution statement, maka pilih model terbaik sebagai solusi. **Jelaskan mengapa memilih model tersebut sebagai model terbaik**.

## Evaluation
Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

