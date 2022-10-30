[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8580042&assignment_repo_type=AssignmentRepo)

## Dataset

Masuk ke dalam Google BigQuery. Gunakan informasi dibawah ini sebagai tempat untuk mengambil data (gunakan sebagai informasi untuk klausa `FROM`).
   * Project ID : `ftds-hacktiv8-project`
   * Dataset Name : 
     + Batch offline : `phase1_ftds_<nomor-batch>_hck` contoh `phase1_ftds_001_hck`
     + Batch online : `phase1_ftds_<nomor-batch>_rmt` contoh `phase1_ftds_001_rmt`
   * Table Name : `heart-failure`

Berikut ini adalah informasi dari setiap column. 
   <img src='https://i.ibb.co/YBGwMXm/P1-G3-Dataset-Information.png'>
---


## Objectives

Membuat model Classification menggunakan Random Forest dan salah satu algoritma boosting untuk memprediksi apakah seorang pasien akan meninggal atau tidak menggunakan dataset yang sudah didapatkan.

---


## Kesimpulan

Kedua model menghasilkan hasil score yang sangat baik dalam menangani kasus ini, namun kedua model ini mengalami overfit meskipun berbeda gapnya. Secara keseluruhan model Random Forest menghasilkan nilai lebih tinggi dalam Train-Set sedangkan model XGB lebih bagus dalam Test-Set. Model Random Forest mengalami overfit dengan gap sekitar 10% antara Train dan Test sedangkan model XGB memiliki gap sekitar 6% antara Train dan Test. Dalam inference set, kedua model ini berhasil memperoleh nilai recall sebesar 1.0 pada label 0 namun hanya 0.6 untuk model RFC dan 0.4 untuk model XGB pada label 1, dimana sebenarnya saya lebih fokus pada recall label 1 dalam kasus ini.

Jadi menurut saya model yang lebih bagus adalah model XGB karena mendapatkan hasil Test yang lebih tinggi dibandingkan dengan Random Forest dan juga gap antara Train dan Testnya tidak terlalu jauh jika dibandingkan dengan Random Forest. Untuk peningkatannya saya rasa jika targetnya lebih balance maka hasil recall pada label 1 akan lebih baik terlebih kita berfokus pada label 1.