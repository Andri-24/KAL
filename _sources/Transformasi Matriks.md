---
title: Transformasi Matriks

---

# Transformasi Matriks

## Pengertian

Definisi aljabar dari perkalian matriks tampak aneh pada awalnya, kita akan melihat bahwa definisi tersebut memungkinkan kita menggunakan matriks untuk mendefinisikan fungsi yang mengubah satu vektor menjadi vektor lain, seperti halnya fungsi-fungsi yang kamu kenal dari kalkulus. Kita kemudian akan memvisualisasikan matriks dan perkalian matriks dalam hal efeknya pada vektor.

Diberikan matriks $A$ berukuran $m \times n$, kita dapat mendefinisikan suatu fungsi $T$ yang menerima vektor kolom $\vec{x} \in \mathbb{R}^n$ sebagai input dan menghasilkan vektor kolom $\vec{y} \in \mathbb{R}^m$ sebagai output, menurut relasi berikut:

$$
\vec{y} = T(\vec{x}) = A\vec{x}
$$

Fungsi semacam ini disebut **transformasi matriks**; ini adalah contoh dari kelas fungsi yang lebih umum dari ruang vektor ke ruang vektor yang dikenal sebagai **transformasi linier**.

Representasi grafis dari vektor memungkinkan kita untuk memvisualisasikan transformasi matriks (setidaknya dalam dimensi rendah). Visualisasi ini memainkan peran penting dalam aplikasi seperti grafik komputer. Kita juga akan melihat bahwa keinginan untuk mendefinisikan fungsi menggunakan perkalian matriks memberikan pembenaran atas mengapa perkalian matriks didefinisikan seperti itu.

---

### A. Perkalian Matriks – Vektor

Untuk menyederhanakan diskusi, dan untuk memudahkan kita melihat apa yang sedang terjadi, kita akan membatasi diri (untuk sekarang) ke vektor di $\mathbb{R}^2$. Kita ingin memvisualisasikan hasil dari mengalikan sebuah vektor oleh matriks. Untuk mengalikan vektor 2D dengan matriks $2 \times 2$, kedua objek harus memiliki ukuran yang kompatibel: vektor 2D dapat dikalikan dengan matriks $2 \times 2$. 
Dengan beberapa vektor dan beberapa matriks, kita akan memplot vektor-vektor tersebut sebelum dan sesudah dikalikan. Dan seperti yang akan kita pelajari...

---

**Contoh 1. Mengalikan vektor dengan matriks**

Misalkan 

$$A = \begin{bmatrix} 2 & 4 \\ 3 & 1 \end{bmatrix}, \quad \vec{i} = \begin{bmatrix} 1 \\ 0 \end{bmatrix}, \quad \vec{j} = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$$

Maka:

$$A\vec{i} = \begin{bmatrix} 2 \\ 3 \end{bmatrix}, \quad A\vec{j} = \begin{bmatrix} 4 \\ 1 \end{bmatrix}$$

Vektor-vektor ini digambarkan dalam **Gambar 5.1.2**.

---

Ada beberapa hal yang perlu diperhatikan. Ketika setiap vektor dikalikan oleh $A$, hasilnya adalah vektor dengan panjang berbeda (dalam contoh ini, selalu lebih panjang), dan dalam dua dari tiga kasus (untuk $\vec{j}$ dan $\vec{z}$), vektor hasilnya menunjuk ke arah yang berbeda.

Ini mengejutkan. Dalam bagian sebelumnya kita belajar bahwa perkalian matriks adalah proses yang sangat sistematis dan dapat diprediksi. Haruskah kita mengharapkan beberapa pola segera terlihat dari perkalian oleh $A$? Jawabannya adalah "tidak selalu".  
Beberapa vektor tidak berubah arah, beberapa berubah arah tapi tetap di jalur yang sama (alias menjadi negatif), dan lainnya menyimpang dari arah aslinya.

---

**Contoh 2. Menggabungkan penjumlahan dan perkalian matriks**

Misalkan 

$$\vec{z} = \vec{i} + \vec{j}$$

dan

$$A\vec{z} = A(\vec{i} + \vec{j})$$

Maka:

$$
\vec{z} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad A\vec{z} = \begin{bmatrix} 6 \\ 4 \end{bmatrix}
$$

Kita telah menggambarkan hasilnya dalam **Gambar 5.1.4**.

---

**Contoh 3. Menggambarkan efek dari perkalian matriks**

Misalkan:

$$
A = \begin{bmatrix} -1 & 2 \\ 0 & 1 \end{bmatrix}, \quad \vec{i} = \begin{bmatrix} 1 \\ 0 \end{bmatrix}, \quad \vec{j} = \begin{bmatrix} 0 \\ 1 \end{bmatrix}
$$

Maka:

$$
A\vec{i} = \begin{bmatrix} -1 \\ 0 \end{bmatrix}, \quad A\vec{j} = \begin{bmatrix} 2 \\ 1 \end{bmatrix}
$$

Hasilnya digambarkan dalam **Gambar 5.1.6**.

---

### B. Transformasi pada Bidang Kartesius

Karena sifat Distributif, seperti yang diilustrasikan dalam Contoh 5.1.3, kita tahu bahwa bidang Kartesius akan ditransformasi secara sistematis: garis lurus akan tetap menjadi garis lurus (tidak akan menjadi lengkung, bergelombang, atau putus-putus).  
**Contoh 5.1.7 Memvisualisasikan transformasi matriks menggunakan vektor**

Plotkan vektor-vektor dari persegi satuan sebelum dan setelah dikalikan dengan 

$$
A = \begin{bmatrix} 2 & 4 \\ 1 & 3 \end{bmatrix}
$$

Empat sudut dari persegi satuan dapat direpresentasikan sebagai:

$$
\begin{bmatrix} 0 \\ 0 \end{bmatrix}, \quad \begin{bmatrix} 1 \\ 0 \end{bmatrix}, \quad \begin{bmatrix} 0 \\ 1 \end{bmatrix}, \quad \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$


---

**Contoh 1. Memvisualisasikan transformasi matriks pada suatu daerah**

Misalkan

$$
A = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}
$$

Maka hasil transformasi dari persegi satuan digambarkan dalam **Gambar 5.1.11**.

---

Kita melihat bahwa persegi satuan tidak hanya “bergeser ke kiri”, melainkan telah **berotasi**. Dalam hal ini, bentuk dari suatu objek tidak berubah: hanya orientasinya yang berubah.

---

Kita telah sampai pada bagaimana bidang Kartesius dapat ditransformasi melalui perkalian dengan matriks $2 \times 2$. Kita telah melihat beberapa contoh, tapi pertanyaannya adalah:

1. **Bagaimana menemukan matriks yang melakukan transformasi tertentu?**
2. **Bagaimana memahami perubahan seluruh bidang hanya dengan mengamati transformasi pada persegi satuan?**

Jawaban untuk pertanyaan 1:
Lihat bagaimana $\vec{i}$ dan $\vec{j}$ ditransformasikan. Matriks yang melakukan transformasi tersebut akan memiliki hasil-hasil tersebut sebagai kolomnya.

---

**Contoh 2. Menentukan suatu transformasi matriks**

Temukan matriks $A$ yang mem-flip bidang Kartesius di sumbu x dan meregangkannya secara horizontal dengan faktor 2.

Solusi:
Flip terhadap sumbu x mengubah $\vec{e}_2 \rightarrow \begin{bmatrix} 0 \\ -1 \end{bmatrix}$

Stretch horizontal faktor 2: $\vec{e}_1 \rightarrow \begin{bmatrix} 2 \\ 0 \end{bmatrix}$

Maka matriksnya:

$$
A = \begin{bmatrix} 2 & 0 \\ 0 & -1 \end{bmatrix}
$$

Visualisasi di **Gambar 5.1.13** dan **5.1.14**.

---

**Contoh 3. Menentukan dan menganalisis transformasi matriks**

Misalnya transformasi dilakukan dengan:
- Meregangkan bidang secara horizontal sebesar faktor $\frac{3}{2}$
- Rotasi 90° searah jarum jam

Rotasi 90° searah jarum jam mengubah:

$$
\vec{e}_1 \rightarrow \begin{bmatrix} 0 \\ -1 \end{bmatrix}, \quad \vec{e}_2 \rightarrow \begin{bmatrix} \frac{3}{2} \\ 0 \end{bmatrix}
$$

Maka:

$$
A = \begin{bmatrix} 0 & \frac{3}{2} \\ -1 & 0 \end{bmatrix}
$$

Visualisasi di **Gambar 5.1.18**.

---

### C. Transformasi Matriks 2D

Stretch horizontal sebesar faktor $k$:

$$
\begin{bmatrix} k & 0 \\ 0 & 1 \end{bmatrix}
$$


Untuk menemukan ke mana titik (2,3) dikirimkan, cukup kalikan

$$
\begin{bmatrix} 1 & 2 \\ 3 & -1 \end{bmatrix}
\begin{bmatrix} 2 \\ 3 \end{bmatrix}=
\begin{bmatrix} 2 + 6 \\ 6 - 3 \end{bmatrix}=
\begin{bmatrix} 8 \\ 3 \end{bmatrix}
$$


Ada cara lain yang tidak terlalu komputasional — tidak perlu menghitung hasil transformasi secara lengkap. Perhatikan persamaan berikut:

$$
\begin{bmatrix} 2 \\ 3 \end{bmatrix}=
2 \begin{bmatrix} 1 \\ 0 \end{bmatrix}+
3 \begin{bmatrix} 0 \\ 1 \end{bmatrix}
\Rightarrow
\begin{bmatrix} 2 \\ 3 \end{bmatrix}=
2\vec{i} + 3\vec{j}
$$

Persamaan ini menyatakan bahwa untuk tiba di vektor $\begin{bmatrix} 2 \\ 3 \end{bmatrix}$, kita perlu pergi 2 satuan ke arah $\vec{i}$ dan 3 satuan ke arah $\vec{j}$. Maka untuk mengetahui ke mana $(2,3)$ dikirimkan, kita hanya perlu melihat ke mana 2 satuan dalam arah baru $\vec{i}$ dan 3 satuan dalam arah baru $\vec{j}$ mengarah.

---

### Contoh 1: Menentukan dan menganalisis transformasi matriks

Langkah-langkah:
1. Temukan matriks $A$ yang mengubah bidang Kartesius dengan:
   - Peregangan vertikal sebesar 2
   - Refleksi horizontal
   - Rotasi 90° searah jarum jam

Solusi:
- Peregangan vertikal: tidak mengubah arah $\vec{i}$, tetapi menggandakan komponen y. Matriksnya:  

  $$
  \begin{bmatrix} 1 & 0 \\ 0 & 2 \end{bmatrix}
  $$

- Refleksi horizontal (terhadap sumbu y):  

  $$
  \begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}
  $$

- Rotasi 90° searah jarum jam:  

  $$
  \begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}
  $$

Gabungan transformasi:

$$
A = A_3 A_2 A_1 = 
\begin{bmatrix} 0 & 1 \\ -1 & 0 \end{bmatrix}
\begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}
\begin{bmatrix} 1 & 0 \\ 0 & 2 \end{bmatrix}=
\begin{bmatrix} 0 & 2 \\ 1 & 0 \end{bmatrix}
$$

---

**Contoh transformasi dasar menggunakan matriks:**

- **Peregangan Vertikal dengan faktor $k$:**  
  Matriks:  
  
  $$
  \begin{bmatrix} 1 & 0 \\ 0 & k \end{bmatrix}
  $$

- **Geseran Horizontal dengan faktor \(k\):**  
  Matriks: 
  
  $$
  \begin{bmatrix} 1 & k \\ 0 & 1 \end{bmatrix}
  $$

- **Geseran Vertikal dengan faktor \(k\):**  
  Matriks:  
  
  $$
  \begin{bmatrix} 1 & 0 \\ k & 1 \end{bmatrix}
  $$

- **Refleksi Horizontal (terhadap sumbu y):**  
  Matriks:
  
  $$
  \begin{bmatrix} -1 & 0 \\ 0 & 1 \end{bmatrix}
  $$


- **Proyeksi ke sumbu y (menekan ke arah y):**  
  Matriks: 
  
  $$
  \begin{bmatrix} 0 & 0 \\ 0 & 1 \end{bmatrix}
  $$

**Contoh 2: Menentukan matriks transformasi kompleks**

Langkah-langkah:
1. Peregangan vertikal sebesar 0.5: 

   $$
   A_1 = \begin{bmatrix} 1 & 0 \\ 0 & 0.5 \end{bmatrix}
   $$

2. Rotasi 30° berlawanan arah jarum jam: 

   $$
   A_2 = \begin{bmatrix} \cos 30° & -\sin 30° \\ \sin 30° & \cos 30° \end{bmatrix}
   = \begin{bmatrix} \sqrt{3}/2 & -1/2 \\ 1/2 & \sqrt{3}/2 \end{bmatrix}
   $$

3. Peregangan horizontal sebesar 2:  

   $$
   A_3 = \begin{bmatrix} 2 & 0 \\ 0 & 1 \end{bmatrix}
   $$

4. Refleksi diagonal terhadap garis \(y = x\):  

   $$
   A_4 = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
   $$

Gabungan transformasi:

$$
A = A_4 A_3 A_2 A_1
$$

Visualisasi transformasi matriks dari contoh sebelumnya.

**Gambar 5.1.20 dan 5.1.21:**  
- Bentuk awal: persegi satuan
- Bentuk akhir: hasil transformasi melalui beberapa langkah matriks

Catatan:
- Transformasi bisa mengubah bentuk (meregang, memutar, mencerminkan)
- Tujuan: memahami mengapa dan bagaimana garis lurus tetap lurus setelah transformasi, dan bagaimana matriks berhubungan dengan operasi ini.

## D. Tugas

### **Soal 1**
Diketahui:
- Matriks 

$$
A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix}
$$

- Vektor 

$$
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

dan 

$$
\vec{y} = \begin{bmatrix} -1 \\ 2 \end{bmatrix}
$$


Hitung:

- 
$$
A\vec{x} = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 1 - 1 \\ 2 + 3 \end{bmatrix} = \begin{bmatrix} 0 \\ 5 \end{bmatrix}
$$

-
$$
A\vec{y} = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix} \begin{bmatrix} -1 \\ 2 \end{bmatrix} = \begin{bmatrix} -1 - 2 \\ -2 + 6 \end{bmatrix} = \begin{bmatrix} -3 \\ 4 \end{bmatrix}
$$

---

### **Soal 2**
Diketahui:
- Matriks 

$$
A = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix}
$$

- Vektor 
$$
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
$$

dan 

$$
\vec{y} = \begin{bmatrix} -1 \\ 2 \end{bmatrix}
$$

Hitung:

- 
$$
A\vec{x} = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix} \begin{bmatrix} 1 \\ 1 \end{bmatrix} = \begin{bmatrix} 2 \\ -1 + 3 \end{bmatrix} = \begin{bmatrix} 2 \\ 2 \end{bmatrix}
$$

-
$$
A\vec{y} = \begin{bmatrix} 2 & 0 \\ -1 & 3 \end{bmatrix} \begin{bmatrix} -1 \\ 2 \end{bmatrix} = \begin{bmatrix} -2 \\ 1 + 6 \end{bmatrix} = \begin{bmatrix} -2 \\ 5 \end{bmatrix}
$$

---

### **Soal 5**
Gambar menunjukkan transformasi dari bujur sangkar satuan menjadi jajar genjang.

Transformasi bujur sangkar satuan dengan vektor basis:
-
$$
\vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix}
$$

dipetakan ke 

$$
\begin{bmatrix} 1 \\ 2 \end{bmatrix}
$$

- 
$$
\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}
$$

dipetakan ke 

$$
\begin{bmatrix} -1 \\ 3 \end{bmatrix}
$$

Maka matriks transformasi $A$ adalah:

$$
A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix}
$$

---

### **Soal 6**
Transformasi bujur sangkar satuan menjadi jajar genjang yang berotasi dan diputar.
Dari gambar:

- 
$$
\vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix}
$$

dipetakan ke 

$$
\begin{bmatrix} 0 \\ 1 \end{bmatrix}
$$

-
$$
\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}
$$

dipetakan ke 

$$
\begin{bmatrix} -1 \\ 1 \end{bmatrix}
$$

Maka matriks transformasi $A$ adalah:

$$
A = \begin{bmatrix} 0 & -1 \\ 1 & 1 \end{bmatrix}
$$
