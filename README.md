# E-Commerce Costumer Churn

# Permasalahan Bisnis

Untuk menarik pelanggan E-Commerce tentu membutuhkan modal yang besar untuk marketing, edukasi, dan lainnya. Bahkan ada konsep "bakar uang" yang dilakukan startup 
demi melakukan penetrasi kepasar yang tentu akan sia - sia apabila pelanggan yang sudah "dibina" untuk menggunakan produk jasa kita malah meninggalkan jasa perusahaan. 
Analisis data kostumer untuk mengklasifikasi setiap kebiasaan kostumer sehingga perusahaan dapat waspada akan kebutuhan kostumer dengan memprediksi 
peluang kostumer tersebut tetap berlangganan atau tidak. Hal ini perlu diketahui perusahaan untuk mengetahui apa yang dibutuhkan pelanggannya dan solusi untuk itu sehingga perusahaan memberikan layanan khusus terhadap konsumen yang setia dan menarik kembali konsumen yang meninggalkan jasa dengan tujuan akhir untuk meningkatkan pendapatan perusahaan.

# Tujuan

Tujuan analisis ini adalah mengklasifikasi peluang kostumer berlangganan atau tidak berdasarkan data yang ada agar perusahaan dan mengetahui mana saja 
kostumer yang memiliki peluang bertahan atau berhenti berlangganan sehingga perusahaan dapat mengetahui secara spesifik target konsumen mana yang perlu diprioritaskan.

## Analytic Approach - Klasifikasi

Membuat model klasifikasi yang mampu membedakan mana pelanggan yang loyal dan pelanggan yang berhenti atau pindah dari layanan.

# Evaluation Metrics

Metric yang digunakan roc_auc dikarenakan perusahaan harus tetap fokus terhadap kostumer yang loyal maupun yang telah berhenti karena kedua kelas kostumer ini 
sangat penting untuk keuntungan perusahaan. kostumer yang loyal akan menjadi partner penting dan kostumer yang berhenti diharapkan ada solusi atau strategi untuk 
menarik kembali sehingga pasar perusahaan akan berkembang.

# Metode Preprocessing

Metode preprocessing untuk missing value menggunakan simple imputer yaitu median karena ada kencenderungan data memiliki outlier. Binary encoding digunakan
untuk mengencoding data dari preferedordercategory dan onehot untuk status nikah atau lajang dari kostumer. robust scaler digunakan untuk menskala data agar memiliki ukuran yang tidak jauh dari awal.

# Penjelasan Modeling

Berikut langkah - langkah modeling :
1. Menggunakan beberapa model klasifikasi yang akan dibandingkan berdasarkan nilai cross validasinya dan metric roc_aucnya lalu dilakuan model selection menggunakan Hyperparameter. 
2. Setelah didapat model yang terbaik dilakukan evaluation metric dengan handling imbalance menggunakan metode RandomOverSampling, SMOTE, dan RandomUnderSampling. ketiga metode itu akan dibandingkan menggunakan cross validation dan juga diseleksi menggunakan hyperparameter.
3. Setelah didapat model terbaik akan dilakukan hyperparameter tuning kembali untuk meningkatkan peforma model.
