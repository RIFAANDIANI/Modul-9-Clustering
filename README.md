# Modul-9-Clustering
##  Visualisasi

![Dashboard Auto-MPG](https://github.com/RIFAANDIANI/Modul-9-Clustering/blob/master/Screenshot%202025-10-28%20024241.png)
1. Sumbu X dan Y

Sumbu X: kemungkinan menunjukkan pendapatan tahunan (Annual Income) atau variabel serupa.
Sumbu Y: tertulis “Spending Score (1–100)”, yaitu skor kebiasaan belanja (semakin tinggi, semakin suka belanja).
Cluster
0 → ungu tua  
1 → biru tua  
2 → hijau toska  
3 → hijau muda  
4 → kuning
Cara Membaca Pola Tiap Cluster

Contohnya:

Cluster 0 (Ungu Tua)
Pendapatan sedang, spending sedang. Biasanya ini pelanggan “biasa” — nggak terlalu konsumtif.

Cluster 1 (Biru Tua)
Spending tinggi, kemungkinan pendapatan juga lumayan. Ini segmen pelanggan “premium” atau “royal spender”.

Cluster 2 (Hijau Toska)
Spending tinggi tapi mungkin pendapatan menengah. Biasanya kelompok “smart spender” — suka belanja tapi terkontrol.

Cluster 3 (Hijau Muda)
Pendapatan rendah, spending rendah. Ini segmen pelanggan yang “hemat” atau jarang belanja.

Cluster 4 (Kuning)
Pendapatan tinggi, spending rendah. Bisa jadi ini orang kaya tapi nggak suka belanja (conservative customer).

## visualisasi distribusi data (histogram + garis KDE)

![Dashboard Auto-MPG](https://github.com/RIFAANDIANI/Modul-9-Clustering/blob/master/Screenshot%202025-10-28%20030212.png)

Cara Baca Setiap Grafik
🧍‍♀️ a. Distribusi Age

Sumbu X: usia pelanggan.

Sumbu Y: jumlah orang pada kelompok usia itu.

Artinya:
Terlihat paling banyak pelanggan berusia sekitar 30 tahun, dan makin sedikit di atas umur 50–60 tahun.
Jadi kebanyakan pelanggan di dataset ini adalah dewasa muda.

Distribusi Annual Income (k$)

Sumbu X: pendapatan tahunan (dalam ribuan dolar).

Sumbu Y: jumlah pelanggan pada rentang pendapatan itu.

Artinya:
Sebagian besar pelanggan punya pendapatan antara 50–80 ribu dolar per tahun, sedangkan yang berpendapatan tinggi (di atas 100 ribu) jumlahnya sedikit.
Ini menunjukkan data cenderung condong ke kanan (right-skewed) — banyak orang berpenghasilan menengah.

Distribusi Spending Score (1–100)

Sumbu X: skor belanja (semakin tinggi = semakin sering dan banyak belanja).

Sumbu Y: jumlah pelanggan.

Artinya:
Nilai spending score menyebar cukup merata, tapi paling banyak di sekitar 40–60.
Artinya, kebanyakan pelanggan punya kebiasaan belanja sedang — tidak terlalu boros dan tidak terlalu hemat.

Fungsi Garis Biru

Garis biru di atas batang histogram itu disebut KDE (Kernel Density Estimate) — tujuannya membantu kamu melihat bentuk pola distribusi:

Kalau garis naik di tengah → berarti data menumpuk di nilai tengah.

Kalau garis punya dua puncak → artinya ada dua kelompok berbeda (bimodal) di data.
Misalnya di Spending Score ada dua puncak, berarti ada dua tipe pelanggan:
satu kelompok belanja rendah, satu lagi belanja tinggi.

kesimpulan: 
Mayoritas pelanggan usia 25–35 tahun.

Pendapatan tahunan rata-rata sekitar 50–80k$.

Spending Score tersebar merata, artinya pola belanja pelanggan cukup beragam.

## eatmap korelasi antar fitur (correlation matrix)

![Dashboard Auto-MPG](https://github.com/RIFAANDIANI/Modul-9-Clustering/blob/master/Screenshot%202025-10-28%20031443.png)

Sumbu X dan Y berisi tiga variabel:

Age (usia pelanggan)

Annual Income (k$) (pendapatan tahunan dalam ribuan dolar)

Spending Score (1–100) (tingkat kebiasaan belanja)

Warna pada kotak menunjukkan arah dan kekuatan hubungan:

🔴 Merah tua (+1) = hubungan positif kuat

🔵 Biru tua (–1) = hubungan negatif kuat

⚪ Abu-abu (0) = tidak ada hubungan yang berarti

### Cara Membaca Nilainya

| Hubungan Variabel                   | Nilai Korelasi | Arti           | Penjelasan                                                                                                                                      |
| ----------------------------------- | -------------- | -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| **Age vs Annual Income**            | –0.012         | Hampir 0       | Tidak ada hubungan berarti antara usia dan pendapatan. Jadi, umur tidak memengaruhi besar kecilnya pendapatan dalam data ini.                   |
| **Age vs Spending Score**           | –0.33          | Negatif sedang | Artinya, semakin tua umur pelanggan, semakin rendah *spending score*-nya. Jadi, pelanggan muda cenderung lebih suka belanja.                    |
| **Annual Income vs Spending Score** | +0.0099        | Hampir 0       | Tidak ada hubungan berarti antara pendapatan dan kebiasaan belanja. Jadi, orang dengan pendapatan tinggi belum tentu suka belanja lebih banyak. |

Arti Warna di Grafik

Kotak merah diagonal (nilai = 1) menunjukkan korelasi diri sendiri (setiap variabel dengan dirinya).

Kotak biru muda (contoh Age vs Spending Score) menunjukkan hubungan negatif sedang.

Kotak abu-abu berarti hubungan sangat lemah atau hampir tidak ada.

kesimpulan 

Variabel Age punya pengaruh negatif sedang terhadap Spending Score.
→ Orang muda lebih sering berbelanja, sedangkan orang lebih tua lebih hemat.

Annual Income hampir tidak berpengaruh pada Spending Score.
→ Spending habit tidak ditentukan oleh seberapa besar pendapatan.

Tidak ada korelasi yang kuat antar variabel (semuanya < |0.5|).
