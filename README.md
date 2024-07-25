# Performance Appraisal Loyalty Program Pada Ritel
# Pendahuluan <a id='intro'></a>

Dalam era persaingan ketat di pasar ritel, pemahaman terhadap pola pembelian pelanggan menjadi krusial bagi kesuksesan perusahaan. Proyek ini bertujuan untuk menggali data pembelian dari sebuah jaringan toko dan mengevaluasi dampak keanggotaan dalam loyalty program  terhadap pola pembelian pelanggan. Pendekatan statistik akan digunakan untuk menguji hipotesis apakah terdapat perbedaan signifikan dalam rata-rata pembelian antara pelanggan yang terdaftar dalam loyalty program dan mereka yang tidak.

Analisis ini diharapkan memberikan wawasan bagi manajemen perusahaan untuk merancang strategi pemasaran yang lebih efektif, menyasar pelanggan potensial, dan meningkatkan retensi pelanggan. Dengan memahami bagaimana loyalty program memengaruhi perilaku pembelian, perusahaan dapat mengoptimalkan alokasi sumber daya untuk meningkatkan kinerja penjualan dan keuntungan.

Pendahuluan ini akan diikuti oleh serangkaian tahap analisis, termasuk pemrosesan data, eksplorasi data, pengujian hipotesis statistik, serta formulasi kesimpulan dan rekomendasi berdasarkan temuan analisis. Mari kita mulai dengan menyelidiki data yang tersedia dan membangun dasar untuk analisis mendalam.

Latar belakang tujuan project 

1. **Siapa Pelanggannya**
   - Manajer Proyek yang bertanggung jawab untuk Loyalty Program akan mengetahui siapa pelanggan yang terlibat dalam proyek tersebut.
   

2. **Siapa Pengguna yang dituju dari hasil akhir**
   - Pelanggan yang memulai proyek. Dalam hasil akhir proyek, pelanggan yang menjadi target atau fokus utama dari program loyalitas akan ditentukan.
   
   
3. **Tujuannya apa yang ingin dilakukan**
   - Mengevaluasi hasil dari analisa pengenalan loyalty program 
   
   
4. **Apakah kita tertarik pada periode waktu tertentu? Atau kita sedang menyelidiki seluruh periode yang dicakup oleh data sumber ini?**
   - Analisis mencakup seluruh periode yang tercakup dalam data sumber.
   
   
5. **Presentasinya ditujukan untuk siapa?**
   - Presentasi ditujukan untuk pelanggan yang memulai proyek.


6. **Mengapa analisis ini diperlukan? Mengapa analisis ini spesifik?**
   - Setelah diperkenalkannya loyalty program , penting untuk memahami apakah itu benar-benar menyebabkan pertumbuhan yang diharapkan dalam ukuran pembelian rata-rata dan jumlah item di keranjang. Analisa ini akan memberi tahu kita seberapa efektif program tersebut.
   
   
7. **Apakah penelitian semacam ini pernah dilakukan sebelumnya?**
   - Tidak ada penelitian serupa yang telah dilakukan sebelumnya. Solusi yang dikembangkan dalam proyek ini akan menjadi pendekatan baru.
   

# Tujuan <a id='GoalSet'></a>

* Performance Appraisal untuk loyalty program. Kita akan menelaah seberapa efektif atau signifikan dalam penggunaan loyalty program terhadap proses bisnis.

# Tahapan yang dilakukan<a id='StepbyStep'></a>

Dalam Project ini ada 2 file csv. Memuat file data dan pelajari informasi umumnya.

**kode_produk: `/datasets/product_codes_us.csv.`**

**data_retail: `/datasets/retail_dataset_us.csv.`**

Tahapan-tahapan yang akan dilakukan adalah sebagai berikut:

**1. Melakukan analisis data eksploratif (EDA):Untuk memeriksa distribusi, nilai yang hilang serta keterlibatan data**
   * Proses
      - Memeriksa dataset yang ada, cek apakah ada nilai yang hilang󠀲󠀡?
      - Memeriksa dan validasi distribusi data
      - Membuat korelasi matriks
      - Membuat histogram untuk melihat distribusi dan analisa lebih lanjut.
         
**2. Menguji Hipotesis**
   * Maksud dan tujuannya : Menguji hipotesis bahwa ukuran pembelian rata-rata untuk member loyality program  lebih tinggi daripada yang non-member loyality program .
   * Proses
     - Memisahkan data pembelian antara member loyality program dan non-member loyality program.
     - Melakukan uji statistik, seperti uji t atau uji Mann-Whitney (depend on data distribution), untuk membandingkan rata-rata  pembelian.
     - Menganalisa hasil dan menentukan apakah ada perbedaan yang substansial.
     
**3. Memformulasikan dan Menguji Hipotesis Statistik**
   * Maksud dan tujuannya: Menyusun hipotesis statistik berdasarkan data dari dataset dan menguji hipotesis tersebut.
   * Proses
     - Mengidentifikasi variabel yang akan diuji dan mengasumsikan yang mendasarinya.
     - Menyusun hipotesis nol (H0) dan hipotesis alternatif (H1).
     - Memilih tingkat signifikansi (umumnya 0,05).
     - Mengunakan uji statistik yang sesuai untuk data.
     - Menganalisis hasil dan mengambil keputusan apakah menerima atau menolak H0.
     
**4. Merumuskan Kesimpulan dan Rekomendasi:**
   * Maksud dan tujuannya: Menarik kesimpulan dari hasil analisis dan menyusun rekomendasi berdasarkan temuan.
   * Proses
     - Meninjau hasil dari uji hipotesis dan analisis data lainnya.
     - Memastikan terhadap temuan tersebut apakah konsisten dengan hipotesis atau tidak.
     - Menjelaskan keterkaitan serta arti dari temuan tersebut.
     - Menyajikan kesimpulan dan saran (rekomendasi).
     
**5. Mempresentasikan**
   * Maksud dan tujuannya: Menyampaikan dan menyajikan dalam bentuk laporan hasil analisis dan temuan kepada pelanggan.
   * Proses
     - Mempersiapkan presentasi laporan dengan ringkas dan jelas.
     - Menyertakan grafik, tabel, dan visualisasi data untuk mendukung temuan.
     - Penyusunan materi dan menjelaskan metodologi yang digunakan dan interpretasi hasil.
     - Memberikan rekomendasi berdasarkan temuan.
     - Memberikan kesempatan untuk pertanyaan dan diskusi.
     
# Deskripsi dataset <a id='description'></a>
**1. retail_dataset_us.csv:**
   - `purchaseId:` ID pembelian yang unik.
   - `item_ID:` ID unik untuk setiap item yang dibeli.
   - `purchasedate:` Tanggal pembelian.
   - `Quantity:` Jumlah item yang dibeli dalam pembelian tersebut.
   - `CustomerID:` ID pelanggan yang unik.
   - `ShopID:` ID toko tempat pembelian dilakukan.
   - `loyalty_program:` Informasi apakah pelanggan adalah anggota program loyalitas (kita mungkin bisa memberi nilai "Yes" atau "No").
   
**2. product_codes_us.csv:**
   - `productID:` ID unik untuk setiap produk.
   - `price_per_one:` Harga per satu item dari produk tersebut.
