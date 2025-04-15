---
title: Transformasi Matriks

---

# Transformasi Matriks

## A. Transformasi Matriks

Definisi aljabar dari perkalian matriks tampak aneh pada awalnya, kita akan melihat bahwa definisi tersebut memungkinkan kita menggunakan matriks untuk mendefinisikan fungsi yang mengubah satu vektor menjadi vektor lain, seperti halnya fungsi-fungsi yang kamu kenal dari kalkulus. Kita kemudian akan memvisualisasikan matriks dan perkalian matriks dalam hal efeknya pada vektor.

Diberikan matriks $A$ berukuran $m \times n$, kita dapat mendefinisikan suatu fungsi $T$ yang menerima vektor kolom $\vec{x} \in \mathbb{R}^n$ sebagai input dan menghasilkan vektor kolom $\vec{y} \in \mathbb{R}^m$ sebagai output, menurut relasi berikut:

$$
\vec{y} = T(\vec{x}) = A\vec{x}
$$

Fungsi semacam ini disebut **transformasi matriks**; ini adalah contoh dari kelas fungsi yang lebih umum dari ruang vektor ke ruang vektor yang dikenal sebagai **transformasi linier**.

Representasi grafis dari vektor memungkinkan kita untuk memvisualisasikan transformasi matriks (setidaknya dalam dimensi rendah). Visualisasi ini memainkan peran penting dalam aplikasi seperti grafik komputer. Kita juga akan melihat bahwa keinginan untuk mendefinisikan fungsi menggunakan perkalian matriks memberikan pembenaran atas mengapa perkalian matriks didefinisikan seperti itu.

## B. Perkalian Matriks – Vektor

Untuk menyederhanakan diskusi, dan untuk memudahkan kita melihat apa yang sedang terjadi, kita akan membatasi diri (untuk sekarang) ke vektor di $\mathbb{R}^2$. Kita ingin memvisualisasikan hasil dari mengalikan sebuah vektor oleh matriks. Untuk mengalikan vektor 2D dengan matriks $2 \times 2$, kedua objek harus memiliki ukuran yang kompatibel: vektor 2D dapat dikalikan dengan matriks $2 \times 2$. 
Dengan beberapa vektor dan beberapa matriks, kita akan memplot vektor-vektor tersebut sebelum dan sesudah dikalikan. Dan seperti yang akan kita pelajari...

---

### **Contoh 1. Mengalikan vektor dengan matriks**

Misalkan $A$ adalah sebuah matriks, dan $\vec{x}, \vec{y}, \vec{z}$ adalah vektor-vektor seperti yang diberikan di bawah ini.

$$
A = \begin{bmatrix} 1 & 4 \\ 2 & 3 \end{bmatrix}, \quad
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\vec{y} = \begin{bmatrix} -1 \\ 1 \end{bmatrix}, \quad
\vec{z} = \begin{bmatrix} 3 \\ -1 \end{bmatrix}.
$$

Gambarkan $\vec{x}, \vec{y}$, dan $\vec{z}$, serta $A\vec{x}, A\vec{y}$, dan $A\vec{z}$.

**Penyelesaian.** Perhitungan berikut cukup langsung:

$$
A\vec{x} = \begin{bmatrix} 5 \\ 5 \end{bmatrix}, \quad
A\vec{y} = \begin{bmatrix} 3 \\ 1 \end{bmatrix}, \quad
A\vec{z} = \begin{bmatrix} -1 \\ 3 \end{bmatrix}.
$$

Vektor-vektor tersebut digambarkan dalam gambar berikut

![Screenshot 2025-04-14 081618](https://hackmd.io/_uploads/rJYbGJq0ke.png)


---

Ada beberapa hal yang perlu diperhatikan. Ketika setiap vektor dikalikan oleh $A$, hasilnya adalah vektor dengan panjang berbeda (dalam contoh ini, selalu lebih panjang), dan dalam dua dari tiga kasus (untuk $\vec{j}$ dan $\vec{z}$), vektor hasilnya menunjuk ke arah yang berbeda.

Ini mengejutkan. Dalam bagian sebelumnya kita belajar bahwa perkalian matriks adalah proses yang sangat sistematis dan dapat diprediksi. Haruskah kita mengharapkan beberapa pola segera terlihat dari perkalian oleh $A$? Jawabannya adalah "tidak selalu". 
Beberapa vektor tidak berubah arah, beberapa berubah arah tapi tetap di jalur yang sama (alias menjadi negatif), dan lainnya menyimpang dari arah aslinya.

---

### **Contoh 2. Menggabungkan penjumlahan dan perkalian matriks**

Misalkan $A$ adalah sebuah matriks dan $\vec{x} \) serta \( \vec{y}$ adalah vektor-vektor seperti yang diberikan di bawah ini.

$$
A = \begin{bmatrix} 1 & 1 \\ 2 & 2 \end{bmatrix}, \quad
\vec{x} = \begin{bmatrix} 2 \\ 1 \end{bmatrix}, \quad
\vec{y} = \begin{bmatrix} -1 \\ 1 \end{bmatrix}.
$$

Gambarkan $\vec{x} + \vec{y}, A\vec{x}, A\vec{y}$, dan $A(\vec{x} + \vec{y})$.

**Penyelesaian.** Perhitungan berikut cukup langsung:

$$
\vec{x} + \vec{y} = \begin{bmatrix} 1 \\ 2 \end{bmatrix}, \quad
A\vec{x} = \begin{bmatrix} 3 \\ 4 \end{bmatrix}, \quad
A\vec{y} = \begin{bmatrix} 0 \\ 1 \end{bmatrix}, \quad
A(\vec{x} + \vec{y}) = \begin{bmatrix} 3 \\ 5 \end{bmatrix}.
$$

Berikut adalah visualisasi gambarnya:

![Screenshot 2025-04-14 082413](https://hackmd.io/_uploads/BJzxNJ9R1g.png)

---

### **Contoh 3. Menggambarkan efek dari perkalian matriks**

Misalkan $A, \vec{x}, \vec{y}$, dan $\vec{z}$ diberikan seperti di bawah ini.

$$
A = \begin{bmatrix} 1 & -1 \\ 1 & -1 \end{bmatrix}, \quad
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\vec{y} = \begin{bmatrix} -1 \\ 1 \end{bmatrix}, \quad
\vec{z} = \begin{bmatrix} 4 \\ 1 \end{bmatrix}.
$$

Gambarkan $\vec{x}, \vec{y}$, dan $\vec{z}$, serta $A\vec{x}, A\vec{y}, A\vec{z}$.

**Penyelesaian.** Perhitungan berikut cukup langsung:

$$
A\vec{x} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}, \quad
A\vec{y} = \begin{bmatrix} -2 \\ -2 \end{bmatrix}, \quad
A\vec{z} = \begin{bmatrix} 3 \\ 3 \end{bmatrix}.
$$

Berikut visualisasi gambarnya:

![Screenshot 2025-04-14 082954](https://hackmd.io/_uploads/B1YXSJ9RJg.png)

## C. Transformasi pada Bidang Kartesius

Karena sifat Distributif, kita tahu bahwa bidang Kartesius akan ditransformasi secara sistematis: garis lurus akan tetap menjadi garis lurus (tidak akan menjadi lengkung, bergelombang, atau putus-putus).

### **Contoh 1. Memvisualisasikan transformasi matriks menggunakan vektor**

Gambarkan vektor-vektor dari satuan persegi sebelum dan sesudah dikalikan dengan matriks $A$, di mana

$$
A = \begin{bmatrix} 1 & 4 \\ 2 & 3 \end{bmatrix}.
$$

**Penyelesaian.** Empat sudut dari persegi satuan dapat direpresentasikan oleh vektor-vektor:

$$
\begin{bmatrix} 0 \\ 0 \end{bmatrix}, \quad
\begin{bmatrix} 1 \\ 0 \end{bmatrix}, \quad
\begin{bmatrix} 1 \\ 1 \end{bmatrix}, \quad
\begin{bmatrix} 0 \\ 1 \end{bmatrix}.
$$

Mengalikan masing-masing dengan $A$ menghasilkan vektor-vektor:

$$
\begin{bmatrix} 0 \\ 0 \end{bmatrix}, \quad
\begin{bmatrix} 1 \\ 2 \end{bmatrix}, \quad
\begin{bmatrix} 5 \\ 5 \end{bmatrix}, \quad
\begin{bmatrix} 4 \\ 3 \end{bmatrix},
$$

masing-masing.

(Hint: Salah satu cara cepat menggunakan kalkulator untuk menghitung ini adalah dengan membuat matriks 2 × 4 yang kolom-kolomnya adalah keempat vektor tersebut. Dalam hal ini, buat matriks

$$
B = \begin{bmatrix} 0 & 1 & 1 & 0 \\ 0 & 0 & 1 & 1 \end{bmatrix}.
$$

Lalu kalikan $B$ dengan $A$, dan baca hasil transformasi dari kolom-kolom hasilnya:

$$
AB = \begin{bmatrix} 0 & 1 & 5 & 4 \\ 0 & 2 & 5 & 3 \end{bmatrix}.
$$

Ini menghemat waktu, terutama jika kamu melakukan prosedur serupa untuk beberapa matriks $A$. Tentu saja, kita bisa menghemat waktu lebih banyak dengan melewatkan kolom pertama; karena itu adalah kolom nol, maka hasil kali dengan $A$ juga akan tetap nol.

Persegi satuan dan transformasinya digambarkan pada Gambar berikut, 

![Screenshot 2025-04-14 084310](https://hackmd.io/_uploads/rybSOy9Akg.png)


di mana titik-titik sudut yang berbentuk tertentu saling berkorespondensi antara kedua grafik tersebut.
Perhatikan bagaimana persegi tersebut berubah menjadi semacam segi empat (sebenarnya merupakan jajar genjang).
Hal yang menarik adalah bagaimana titik-titik sudut berbentuk segitiga dan persegi tampaknya saling bertukar tempat — seolah-olah
persegi tersebut, selain mengalami perubahan bentuk, juga dibalik.

Untuk menekankan bahwa "garis lurus tetap menjadi garis lurus setelah ditransformasikan," perhatikan Gambar berikut.

![Screenshot 2025-04-14 084449](https://hackmd.io/_uploads/SJRjdJqRJx.png)


Di sini, persegi satuan memiliki beberapa titik tambahan yang digambarkan, yang berkorespondensi dengan titik-titik berwarna pada jajar genjang hasil transformasi.
Perhatikan juga bagaimana jarak relatif tetap terjaga; titik yang berada di tengah-tengah antara titik hitam dan titik persegi ditransformasikan ke posisi di sepanjang garis, tepat di tengah-tengah antara titik hitam dan titik persegi.

---

### **Contoh 2. Memvisualisasikan transformasi matriks pada suatu daerah**

Gambarkan persegi satuan yang telah ditransformasikan oleh matriks $A$, di mana

$$
A = \begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}.
$$

**Penyelesaian.** Kita akan meletakkan vektor-vektor yang merepresentasikan setiap sudut dari persegi satuan ke dalam sebuah matriks \( B \) seperti sebelumnya, lalu mengalikan \( B \) dari kiri dengan \( A \). Dengan demikian diperoleh:

$$
AB = 
\begin{bmatrix} 0 & -1 \\ 1 & 0 \end{bmatrix}
\begin{bmatrix} 0 & 1 & 0 & 1 \\ 0 & 0 & 1 & 1 \end{bmatrix}=
\begin{bmatrix} 0 & -1 & -1 & -2 \\ 0 & 0 & 1 & 1 \end{bmatrix}.
$$

(Di gambar berikut, persegi satuan digambarkan kembali bersama dengan hasil transformasinya oleh $A$.)

![Screenshot 2025-04-14 085003](https://hackmd.io/_uploads/SJH19J5Akl.png)

Kita melihat bahwa persegi satuan tidak hanya “bergeser ke kiri”, melainkan telah **berotasi**. Dalam hal ini, bentuk dari suatu objek tidak berubah: hanya orientasinya yang berubah.

---

Kita telah membahas bagaimana bidang Kartesius dapat ditransformasikan melalui perkalian dengan matriks $A$ berukuran $2 \times 2.$

Kita telah melihat beberapa contoh sejauh ini, dan intuisi kita tentang bagaimana bidang ini berubah dibentuk oleh pengamatan terhadap perubahan yang terjadi pada satuan persegi. Mari kita eksplorasi lebih jauh dengan dua pertanyaan berikut:

1. Misalnya kita ingin mentransformasikan bidang Kartesius dengan cara tertentu (seperti memutar bidang berlawanan arah jarum jam sebesar $180^\circ$). Bagaimana kita menemukan matriks (jika ada) yang melakukan transformasi tersebut?

2. Bagaimana pengetahuan kita tentang bagaimana satuan persegi berubah bisa membantu kita memahami bagaimana seluruh bidang ditransformasikan?

Kedua pertanyaan ini saling berkaitan, dan saat kita menjawab satu, kita juga akan menjawab yang lainnya.

Untuk memulai dengan pertanyaan pertama, coba lihat kembali Contoh 1 dan Contoh 2 dan pertimbangkan lagi bagaimana satuan persegi ditransformasikan.

Apakah ada korelasi antara di mana titik-titik pojok akhirnya berada dengan entri dalam matriks $A$?

Jika kamu baru membaca ini sekarang, dan belum benar-benar melihat contohnya, sebaiknya kamu melihatnya dulu dan coba cari koneksi tersebut.

Kalau tidak, kamu mungkin menyadari beberapa hal seperti berikut ini:

1. Vektor nol ($\vec{0}$, atau "pojok hitam") tidak pernah bergerak. Itu masuk akal, karena: $A \vec{0} = \vec{0}$

2. Pojok "persegi", yaitu pojok yang sesuai dengan vektor $\begin{bmatrix} 1 \\ 0 \end{bmatrix}$ selalu ditransformasikan ke vektor di kolom pertama matriks $A$.

3. Demikian juga, pojok "segitiga", yaitu pojok yang sesuai dengan vektor $\begin{bmatrix} 0 \\ 1 \end{bmatrix}$ selalu ditransformasikan ke kolom kedua dari $A$.

4. Pojok "putih" selalu ditransformasikan ke jumlah dari dua vektor kolom pada $A$. (Hal ini sedikit lebih samar dari dua poin sebelumnya, namun dapat dipahami jika kita ingat bahwa pojok ini merupakan "jumlah" dari dua pojok lainnya.)

Sekarang mari kita pahami poin-poin ini. Poin pertama seharusnya jelas: $\vec{0}$ selalu ditransformasikan ke $\vec{0}$ melalui perkalian matriks.

Kita bisa memahami poin ke-2 dan ke-3 secara bersamaan. Misalkan:

$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}, \quad \vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix}, \quad \vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}
$$

Maka:

$$
A \vec{e}_1 = \begin{bmatrix} a & b \\ c & d \end{bmatrix} \begin{bmatrix} 1 \\ 0 \end{bmatrix} = \begin{bmatrix} a \\ c \end{bmatrix}, \quad A \vec{e}_2 = \begin{bmatrix} a & b \\ c & d \end{bmatrix} \begin{bmatrix} 0 \\ 1 \end{bmatrix} = \begin{bmatrix} b \\ d \end{bmatrix}
$$

Jadi secara mekanis melalui perkalian matriks, pojok persegi $\vec{e}_1$ ditransformasikan ke kolom pertama $A$, dan pojok segitiga $\vec{e}_2$ ke kolom kedua $A$.

Dengan argumen serupa, pojok putih (yaitu $\vec{e}_1 + \vec{e}_2$) akan ditransformasikan ke jumlah dari kolom-kolom $A$.

Cara lain untuk melihat $A$ adalah: Apa itu $A$? Ia hanyalah matriks yang berisi vektor $A$ $\vec{e}_1$ dan $A$ $\vec{e}_2$ sebagai kolom-kolomnya.

Dengan kata lain: Apa isi dari kolom 1 dan kolom 2 dari $A$? Jawabannya: $A$ $\vec{e}_1$ dan $A \vec{e}_2$.

Maka jika kita diberi tahu posisi akhir dari $\vec{e}_1$ dan $\vec{e}_2$ setelah transformasi, kita bisa menyusun matriks $A$ hanya dengan menaruh hasil tersebut sebagai kolom-kolomnya.

---

### **Contoh 3. Menentukan suatu transformasi matriks**

Tentukan matriks $A$ yang mencerminkan bidang Kartesius terhadap sumbu $x$, lalu meregangkan bidang secara horizontal dengan faktor dua.

**Penyelesaian.** Kita mulai dengan mempertimbangkan $\vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix}$ .Ke manakah sudut ini berpindah di bawah transformasi tersebut? Mencerminkan bidang terhadap sumbu $x$ **tidak** mengubah $\vec{e}_1$; meregangkan bidang mengubah $\vec{e}_1$ menjadi: $\vec{e}_1 \rightarrow \begin{bmatrix} 2 \\ 0 \end{bmatrix}$ Maka, kolom pertama dari $A$ adalah: $\begin{bmatrix} 2 \\ 0 \end{bmatrix}.$ Sekarang kita perhatikan $\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}$ Mencerminkan bidang terhadap sumbu $x$ mengubahnya menjadi: $\begin{bmatrix} 0 \\ -1 \end{bmatrix},$ dan peregangan horizontal **tidak** memengaruhi vektor ini. Maka, kolom kedua dari $A$ adalah: $\begin{bmatrix} 0 \\ -1 \end{bmatrix}.$

Jika digabungkan, kita peroleh:

$$
A = \begin{bmatrix} 2 & 0 \\ 0 & -1 \end{bmatrix}.
$$

(Untuk membantu memvisualisasikannya, lihat gambar berikut, di mana sebuah bentuk mengalami transformasi dengan matriks ini: dibalik terhadap sumbu $x$ dan diregangkan dua kali ke arah horizontal.)

![Screenshot 2025-04-15 095453](https://hackmd.io/_uploads/Sy3o9HjAkl.png)

Sebelumnya kita telah mengajukan dua pertanyaan. Yang pertama adalah: "Bagaimana kita menemukan matriks yang melakukan transformasi tertentu?" Kita baru saja menjawab pertanyaan itu. Pertanyaan kedua adalah: "Bagaimana pengetahuan tentang bagaimana persegi satuan ditransformasikan membantu kita memahami bagaimana seluruh bidang Kartesius ditransformasikan?"

Pertimbangkan Gambar berikut

![Screenshot 2025-04-15 100223](https://hackmd.io/_uploads/S1nd3BsC1e.png)


di mana persegi satuan (dengan titik-titik sudut) telah ditransformasikan oleh matriks yang **tidak diketahui**. Bagaimana gambar ini membantu kita memahami bagaimana titik $(3,1)$ akan ditransformasikan? Sebagai contoh, bagaimana kita bisa menggunakan gambar tersebut untuk mencari tahu ke mana titik $(3,1)$ ditransformasikan?

Ada dua cara untuk menyelesaikan soal ini. Pertama, kita tahu bahwa untuk menghitung matriks transformasi, posisi baru dari $\vec{e}_1$ menjadi kolom pertama dari $A$, dan posisi baru dari $\vec{e}_2$ menjadi kolom kedua dari $A$. Maka dari gambar, kita simpulkan bahwa:

$$
A = \begin{bmatrix} 1 & -1 \\ 2 & 2 \end{bmatrix}.
$$

Untuk menemukan ke mana titik $(3,1)$ dipetakan, cukup kalikan:

$$
\begin{bmatrix} 1 & -1 \\ 2 & 2 \end{bmatrix}
\begin{bmatrix} 3 \\ 1 \end{bmatrix}=
\begin{bmatrix} 2 \\ 8 \end{bmatrix}.
$$

Ada juga cara lain yang lebih intuitif (dan tidak melibatkan perhitungan matriks eksplisit). Pertimbangkan persamaan berikut:

$$
\begin{bmatrix} 3 \\ 1 \end{bmatrix}
= 2 \begin{bmatrix} 1 \\ 2 \end{bmatrix} + 1 \begin{bmatrix} -1 \\ 2 \end{bmatrix}
= 2\vec{e}_1' + \vec{e}_2'.
$$

Persamaan ini menyatakan hal yang cukup jelas: untuk mencapai vektor $\begin{bmatrix} 3 \\ 1 \end{bmatrix}$ , kita harus bergerak 2 unit ke arah $\vec{e}_1'$ , dan 1 unit ke arah $\vec{e}_2'$.

(Jadi, untuk mengetahui ke mana titik $(2,3)$ dipetakan oleh transformasi, cukup lihat berapa banyak unit $\vec{e}_1'$ dan $\vec{e}_2'$ yang dibutuhkan untuk membentuk kombinasi tersebut. Gambar berikut memberikan visualisasi proses ini.)

![Screenshot 2025-04-15 100359](https://hackmd.io/_uploads/HJZ2hro0yl.png)

---

### **Contoh 4. Menentukan dan menganalisis transformasi matriks**

Tentukan matriks $A$ yang mentransformasikan bidang Kartesius dengan cara:
- meregangkannya secara vertikal dengan faktor 1.5,
- meregangkannya secara horizontal dengan faktor 0.5,
- kemudian memutarnya searah jarum jam sebesar 90°.

Selanjutnya, gunakan posisi baru dari $\vec{e}_1$ dan $\vec{e}_2$ untuk menentukan posisi hasil transformasi dari titik $(-1, 2)$.

**Penyelesaian.** Untuk menemukan $A$, kita mulai dengan mencari posisi baru dari $\vec{e}_1$. 

- Peregangan vertikal **tidak** memengaruhi $\vec{e}_1$
- Peregangan horizontal dengan faktor 0.5 mengubahnya menjadi:

$$
\begin{bmatrix} \frac{1}{2} \\ 0 \end{bmatrix}
$$

- Memutar 90° searah jarum jam mengubahnya menjadi:

$$
\begin{bmatrix} 0 \\ -\frac{1}{2} \end{bmatrix}
$$

Ini adalah kolom pertama dari $A$.

Sekarang, posisi baru dari $\vec{e}_2$:

- Peregangan vertikal dengan faktor 1.5 mengubahnya menjadi:

$$
\begin{bmatrix} 0 \\ \frac{3}{2} \end{bmatrix}
$$

- Peregangan horizontal tidak memengaruhi,
- Rotasi 90° searah jarum jam mengubahnya menjadi:

$$
\begin{bmatrix} \frac{3}{2} \\ 0 \end{bmatrix}
$$

Ini adalah kolom kedua dari $A$. Jadi:

$$
A = \begin{bmatrix}
0 & \frac{3}{2} \\
-\frac{1}{2} & 0
\end{bmatrix}
$$

Untuk menentukan ke mana titik $(-1, 2)$ ditransformasikan, kita kalikan:

$$
\begin{bmatrix}
0 & \frac{3}{2} \\
-\frac{1}{2} & 0
\end{bmatrix}
\begin{bmatrix}
-1 \\
2
\end{bmatrix}=
\begin{bmatrix}
3 \\
\frac{1}{2}
\end{bmatrix}
$$

Jadi, titik $(-1, 2)$ dipetakan ke $\begin{bmatrix} 3 \\ \frac{1}{2} \end{bmatrix}$ . Hasil ini juga dapat diverifikasi secara komputasional seperti yang ditunjukkan pada Gambar berikut.

![Screenshot 2025-04-15 101432](https://hackmd.io/_uploads/rknEJIj0kx.png)

## D. Transformasi Matriks 2D

### Contoh 1: Transformasi Matriks pada Bidang Kartesius

- Peregangan Horizontal dengan faktor 𝑘

$$
\begin{bmatrix}
k & 0 \\
0 & 1
\end{bmatrix}
$$

![Screenshot 2025-04-15 102755](https://hackmd.io/_uploads/S1W8zUs0kl.png)

- Peregangan Vertikal dengan faktor 𝑘

$$
\begin{bmatrix}
1 & 0 \\
0 & k
\end{bmatrix}
$$

![Screenshot 2025-04-15 102918](https://hackmd.io/_uploads/BJZoMUjA1g.png)

- Geseran Horizontal dengan faktor 𝑘

$$
\begin{bmatrix}
1 & k \\
0 & 1
\end{bmatrix}
$$

![image](https://hackmd.io/_uploads/H1qCGUjA1g.png)

- Geseran Vertikal dengan faktor 𝑘

$$
\begin{bmatrix}
1 & 0 \\
k & 1
\end{bmatrix}
$$

![Screenshot 2025-04-15 103529](https://hackmd.io/_uploads/SJ4FVLoAyx.png)


- Refleksi Horizontal terhadap sumbu-y

$$
\begin{bmatrix}
-1 & 0 \\
0 & 1
\end{bmatrix}
$$

![Screenshot 2025-04-15 103545](https://hackmd.io/_uploads/rJnj4Li0yg.png)


- Refleksi Vertikal terhadap sumbu-x

$$
\begin{bmatrix}
1 & 0 \\
0 & -1
\end{bmatrix}
$$

![Screenshot 2025-04-15 103602](https://hackmd.io/_uploads/rk63VIsCyl.png)


- Refleksi Diagonal terhadap garis $y=x$

$$
\begin{bmatrix}
0 & 1 \\
1 & 0
\end{bmatrix}
$$

![Screenshot 2025-04-15 103614](https://hackmd.io/_uploads/rJh648jCke.png)


- Rotasi terhadap titik asal sebesar sudut 𝜃

$$
\begin{bmatrix}
\cos \theta & -\sin \theta \\
\sin \theta & \cos \theta
\end{bmatrix}
$$

![Screenshot 2025-04-15 103632](https://hackmd.io/_uploads/Bk0RV8iAkl.png)


- Proyeksi ke sumbu-x

$$
\begin{bmatrix}
1 & 0 \\
0 & 0
\end{bmatrix}
$$

![Screenshot 2025-04-15 103643](https://hackmd.io/_uploads/ryexHUiCkg.png)


- Proyeksi ke sumbu-y

$$
\begin{bmatrix}
0 & 0 \\
0 & 1
\end{bmatrix}
$$

![Screenshot 2025-04-15 103655](https://hackmd.io/_uploads/rJmZH8sRyl.png)

Sekarang setelah kita melihat berbagai transformasi yang dapat dilakukan pada bidang Kartesius, mari kita berlatih beberapa kali lagi dalam membuat matriks 
yang menghasilkan transformasi yang diinginkan. Dalam contoh berikut, kita akan mengembangkan pemahaman kita satu langkah penting lebih jauh.

---

### Contoh 2: Menentukan matriks dari suatu transformasi.

Temukan matriks $A$ yang mentransformasikan bidang Kartesius dengan melakukan operasi berikut secara berurutan:

1. Geseran vertikal dengan faktor 0.5  
2. Rotasi berlawanan arah jarum jam sebesar sudut $30^\circ$  
3. Peregangan horizontal dengan faktor 2  
4. Refleksi diagonal terhadap garis $y = -x$

---

Solusi: Kita sudah tahu bagaimana melakukan ini — semacam. Kita tahu bahwa kita bisa menemukan kolom-kolom dari $A$  dengan menelusuri ke mana $\vec{e}_1$ dan $\vec{e}_2$ berakhir, tetapi ini juga tampak sulit. Ada begitu banyak hal yang terjadi. Untungnya, kita dapat menyelesaikannya dengan cukup mudah dengan menggunakan pendekatan sistematik.

Pertama, kita lakukan geseran vertikal. Matriks yang melakukan ini adalah:

$$
A_1 = \begin{bmatrix} 1 & 0 \\ 0.5 & 1 \end{bmatrix}
$$

Setelah itu, kita ingin memutar semuanya searah jarum jam sebesar  $30^\circ$ . Untuk melakukannya, kita gunakan:

$$
A_2 = \begin{bmatrix} \cos 30^\circ & -\sin 30^\circ \\ \sin 30^\circ & \cos 30^\circ \end{bmatrix} = \begin{bmatrix} \sqrt{3}/2 & -1/2 \\ 1/2 & \sqrt{3}/2 \end{bmatrix}
$$

Untuk melakukan semua operasi ini secara berurutan, kita kalikan $A_2 A_1.$

Pertimbangkan ini dengan seksama. Misalnya, saya ingin tahu di mana sebuah vektor $\vec{x}$ akan berakhir.
Kita bisa mendapatkan jawabannya dengan mengalikan $A\vec{x}$. Mengapa ini berhasil? Pertimbangkan:

$A \vec{x} = A_4 A_3 A_2 A_1 \vec{x}$

$= A_4 A_3 A_2 (A_1 \vec{x}) \quad \text{(melakukan geseran vertikal)}$

$= A_4 A_3 (A_2 (A_1 \vec{x})) \quad \text{(melakukan rotasi)}$

$= A_4 (A_3 (A_2 (A_1 \vec{x}))) \quad \text{(melakukan peregangan horizontal)}$

$= A_4 (\cdots) \quad \text{(melakukan refleksi diagonal)}$

$= \vec{x}_1 \quad \text{(hasil dari mentransformasikan } \vec{x} \text{)}$

***Catatan*** : Ingat kembali bahwa perkalian matriks tidak komutatif.

$$
A_1 A_2 \ne A_2 A_1 \quad \Rightarrow \quad A_2 (A_1 \vec{x}) \ne A_1 (A_2 \vec{x})
$$

Jika ditafsirkan sebagai transformasi bidang, hal ini juga masuk akal secara visual. Misalnya, dalam kebanyakan kasus, refleksi diikuti dengan rotasi tidak akan menghasilkan hasil yang sama seperti rotasi terlebih dahulu lalu refleksi.
Disarankan untuk bereksperimen dengan beberapa contoh untuk melihat apa yang terjadi jika urutannya dibalik.
Untuk melakukan dua operasi terakhir, kita ambil:

$$
A_3 = \begin{bmatrix} 2 & 0 \\ 0 & 1 \end{bmatrix} \quad \text{dan} \quad A_4 = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
$$

yang melakukan peregangan horizontal dan refleksi diagonal, secara berurutan. Maka untuk melakukan seluruh operasi sekaligus, kita kalikan:

$$
A = A_4 A_3 A_2 A_1
$$

$$= 
\begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}
\begin{bmatrix} 2 & 0 \\ 0 & 1 \end{bmatrix}
\begin{bmatrix} \sqrt{3}/2 & -1/2 \\ 1/2 & \sqrt{3}/2 \end{bmatrix}
\begin{bmatrix} 1 & 0 \\ 0.5 & 1 \end{bmatrix}
$$

$$= 
\begin{bmatrix}
((\sqrt{3} - 2)/4) & \sqrt{3}/2 \\
((2\sqrt{3} - 1)/2) & -1
\end{bmatrix}
$$

$$
\approx
\begin{bmatrix}
0.933 & 0.866 \\
1.232 & -1
\end{bmatrix}
$$

Sebagian besar pembaca tidak dapat membayangkan secara tepat apa yang dilakukan oleh daftar operasi yang diberikan terhadap bidang Kartesius. 
Pada Gambar berikut, kita menggambarkan persegi satuan yang telah ditransformasikan; 

![Screenshot 2025-04-15 110955](https://hackmd.io/_uploads/BJs7hIiRJg.png)

sedangkan pada Gambar berikut, kita menggambarkan sebuah bentuk dan hasil transformasinya.

![Screenshot 2025-04-15 111039](https://hackmd.io/_uploads/Hk7LhIsC1g.png)

Setelah kita mengetahui matriks-matriks yang melakukan transformasi dasar (atau tahu di mana menemukannya), melakukan transformasi kompleks pada bidang Kartesius sebenarnya tidaklah begitu... kompleks. 
Intinya hanyalah mengalikan dengan serangkaian matriks. 

Kita telah melihat banyak contoh transformasi yang bisa dilakukan, dan kita juga telah menyebutkan beberapa yang tidak bisa — misalnya, kita tidak bisa mengubah sebuah persegi menjadi lingkaran. 
Mengapa tidak? Mengapa garis lurus selalu berubah menjadi garis lurus? 

Semua pertanyaan ini menuntut kita untuk berpikir seperti seorang matematikawan — kita diminta untuk mempelajari sifat-sifat dari suatu objek yang baru saja kita pelajari dan hubungannya dengan konsep-konsep yang telah kita pelajari sebelumnya. 
Kita akan melakukan semua ini (dan lebih banyak lagi!) di bagian berikutnya.

## E. Tugas

### **Soal 1**
Diketahui:

- Matriks 

$$
A = \begin{bmatrix} 1 & -1 \\ 2 & 3 \end{bmatrix}
$$

- Vektor 

$$
\vec{x} = \begin{bmatrix} 1 \\ 1 \end{bmatrix}
\quad dan \quad
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
\quad dan \quad
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
Transformasi dari bujur sangkar satuan menjadi jajar genjang.

Transformasi bujur sangkar satuan dengan vektor basis:

-
$$
\vec{e}_1 = \begin{bmatrix} 1 \\ 0 \end{bmatrix}
\quad dipetakan \quad ke \quad
\begin{bmatrix} 1 \\ 2 \end{bmatrix}
$$

- 
$$
\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix} \quad
dipetakan \quad ke \quad
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
\quad dipetakan \quad ke \quad
\begin{bmatrix} 0 \\ 1 \end{bmatrix}
$$

-
$$
\vec{e}_2 = \begin{bmatrix} 0 \\ 1 \end{bmatrix}
\quad dipetakan \quad ke \quad
\begin{bmatrix} -1 \\ 1 \end{bmatrix}
$$

Maka matriks transformasi $A$ adalah:

$$
A = \begin{bmatrix} 0 & -1 \\ 1 & 1 \end{bmatrix}
$$
