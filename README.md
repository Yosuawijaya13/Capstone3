# Capstone3

Halo rekan-rekan, ini adalah project phyton ketiga dari aku. Project ini merupakan sebuah proyek membuat model Machine Learning, dimana aku bermain role sebagai data scientist yang direkurt oleh sebuah Perusahaan Asuransi.

Dimana pada project ini, aku bertugas untuk menjawab sebuah pertanyaan bisnis. **apakah terdapat pola dari para pemegang polis yang mengajukan claim?**

Dalam prosesnya dilakukan beberapa tahapan
1. Data preprocess (data cleaning, feature enrichment, feature selection)
2. Proses pengujian model dalam beberapa skenario (Baseline, Class Weight, Oversampling (SMOTE), undersampling (NearMiss)
3. Optimalisasi model (Hyperparameter Tuning)

# Dari proses tersebut ada poin-poin menarik yang bisa dianalisa lebih lanjut

Hasil pengujian mode di beberapa skenario:
- Undersampling Gagal: Menghapus data terbukti menghilangkan informasi penting dan menghasilkan model terburuk.
- Baseline & Class Weight Tidak Cukup: Tanpa menyeimbangkan data, model gagal mendeteksi klaim (Recall ≈ 0).
- SMOTE adalah Pemenangnya: Oversampling (SMOTE) secara konsisten menjadi strategi terbaik, memungkinkan semua model untuk belajar mengenali pola klaim.

Model yang digunakan adalah `LightGBM dengan Oversampling (SMOTE)`, dipilih karena menghasilkan AUC-ROC dan nilai recall yang cukup baik, didukung dengan hasil pengujian Cross Validation yang meningkat

Faktor Pendorong Klaim Teratas:
1. Commission_Rate & Net Sales: Struktur finansial polis adalah prediktor utama.
2. Duration: Semakin lama perjalanan, semakin tinggi kemungkinan klaim.
Kesimpulan Wawasan: Model menunjukkan bahwa "apa yang dijual" dan “Durasi perjalanan” lebih berpengaruh daripada profil demografis pelanggan.


# Kesimpulan Proyek:
Berhasil membangun model LightGBM yang telah dioptimalkan dan mampu mengidentifikasi 68% dari total potensi klaim.
Berdasarkan simulasi Dengan menggunakan model, perusahaan dapat mengurangi jumlah dana cadangan hingga 62%, membebaskan modal secara signifikan untuk diinvestasikan."

# Rekomendasi Pengembangan Model:
- Mengubah Threshold sesuai dengan kebutuhan dari stakeholders dan melakukan uji coba kembali
- Menambahkan Fitur baru seperti jenis claim yang diajukan
- Menganalisa lebih lanjut kelompok data yang salah prediksi

# Rekomendasi Aksi:
Pengembangan Produk: Gunakan wawasan dari Duration dan Commission_Rate untuk merancang produk dan struktur premi yang lebih baik di masa depan.

Ini adalah bukti pembelajaranku, dan berharap kedepannya skillku semakin terasah Saran dan masukan rekan-rekan sangat berarti.


