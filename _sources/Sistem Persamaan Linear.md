---
title: Sistem Persamaan Linear

---

# Sistem Persamaan Linear

## A. Pengertian
Sistem persamaan linear adalah kumpulan persamaan linear yang terdiri dari beberapa variabel. Persamaan linear adalah persamaan aljabar yang dapat digambarkan sebagai garis lurus pada koordinat kartesius. 

## B. Menyelesaikan Sistem Persamaan Linear Menggunakan Eliminasi Gauss

### 1. Konsep Dasar Matriks

#### a. Definisi Matriks:
Matriks adalah kumpulan bilangan yang disusun dalam baris dan kolom.
Contoh:

$$
A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}
$$

#### b. Notasi:
- $R_1, R_2, R_3$ untuk baris pertama, kedua, dan ketiga.

---

### 2. Tiga Jenis Operasi Baris Elementer

#### a. Menukar Dua Baris
- **Notasi:** $R_i \leftrightarrow R_j$
- **Contoh:** Menukar baris pertama $R_1$ dengan baris kedua $R_2$

#### b. Mengalikan Baris dengan Skalar Non-Nol
- **Notasi:** $R_i \to k \cdot R_i$ di mana $k \neq 0$
- **Contoh:** Mengalikan baris pertama dengan 2 jadi $2R_1$

#### c. Menambahkan Kelipatan Satu Baris ke Baris Lain
- **Notasi:** $R_i \to R_i + k \cdot R_j$
- **Contoh:** Menambahkan dua kali baris kedua ke baris pertama $R_1 \to R_1 + 2R_2$

---

### 3. Contoh Operasi Baris Elementer

#### a. Matriks Awal:
$$
A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}
$$

#### b. Langkah 1: Menukar $R_1$ dan $R_2$
$$
\begin{bmatrix} 4 & 5 & 6 \\ 1 & 2 & 3 \\ 7 & 8 & 9 \end{bmatrix}
$$

#### c. Langkah 2: Mengalikan $R_2$ dengan 2
$$
\begin{bmatrix} 4 & 5 & 6 \\ 2 & 4 & 6 \\ 7 & 8 & 9 \end{bmatrix}
$$

#### d. Langkah 3: Menambahkan $-2R_1$ ke $R_3$
$$
\begin{bmatrix} 7 & 8 & 9 \\ 8 & 12 & 12 \\ -13 & -14 & -15 \end{bmatrix}
$$

---

### 4. Bentuk Eselon Baris dan Eselon Baris Tereduksi

#### a. Bentuk Eselon Baris:
- Baris nol berada di bawah baris non-nol.
- Elemen pivot (elemen pertama non-nol pada suatu baris) harus berada di sebelah kanan pivot pada baris sebelumnya.

#### b. Bentuk Eselon Baris Tereduksi:
- Memenuhi semua syarat bentuk eselon baris.
- Setiap elemen pivot bernilai 1.
- Kolom yang mengandung elemen pivot hanya memiliki satu elemen non-nol (yaitu pivot).

---

### 5. Langkah-langkah Eliminasi Gauss

#### a. Langka 1. Tulis Matriks Augmentasi
- Ubah SPL menjadi matriks augmentasi.
- Contoh:

$$\begin{aligned}
x + 2y + z &= 9 \\
2x + y - z &= 3 \\
3x - y + 2z &= 8
\end{aligned}$$


$$
  \begin{bmatrix} 1 & 2 & 1 & 9 \\
                   2 & 1 & -1 & 3 \\
                   3 & -1 & 2 & 8 \end{bmatrix}
  $$

### b. Langkah 2 - Bentuk Eselon Baris
- Gunakan Operasi Baris Elementer (OBE) untuk menghasilkan bentuk eselon baris:
  - Elemen pivot harus berada di kanan elemen pivot sebelumnya.
  - Baris nol (jika ada) berada di bawah baris non-nol.
#### **Langkah 2.1** : Jadikan elemen pivot pertama (baris 1, kolom 1) bernilai 1.
- Sudah bernilai 1, jadi tidak perlu diubah.

#### **Langkah 2.2** : Nolkan elemen di bawah pivot pertama $R_2$ dan $R_3$ :
- $$ R_2 \to R_2 - 2R_1 $$

$$
\begin{bmatrix} 
1 & 2 & 1 & | 9 \\ 
2 & 1 & -1 & | 3 \\ 
3 & -1 & 2 & | 8 
\end{bmatrix}
\rightarrow
\begin{bmatrix} 
1 & 2 & 1 & | 9 \\ 
0 & -3 & -3 & | -15 \\ 
3 & -1 & 2 & | 8 
\end{bmatrix}
$$

- $$ R_3 \to R_3 - 3R_1 $$

$$
\begin{bmatrix} 
1 & 2 & 1 & | 9 \\ 
0 & -3 & -3 & | -15 \\ 
0 & -7 & -1 & | -19 
\end{bmatrix}
$$

#### **Langkah 2.3**: Jadikan elemen pivot kedua (baris 2, kolom 2) bernilai 1.
- $$ R_2 \to \frac{-1}{3} R_2 $$

$$
\begin{bmatrix} 
1 & 2 & 1 & | 9 \\ 
0 & 1 & 1 & | 5 \\ 
0 & -7 & -1 & | -19 
\end{bmatrix}
$$


#### **Langkah 2.4**: Nolkan elemen di bawah pivot kedua $R_3$
- $$ R_3 \to R_3 + 7R_2 $$

$$
\begin{bmatrix} 1 & 2 & 1 & 9 \\
                   0 & 1 & 1 & 5 \\
                   0 & 0 & 1 & 16 \end{bmatrix}
$$

#### **Langkah 2.5**: Jadikan elemen pivot ketiga (baris 3, kolom 3) bernilai 1
- $$ R_3 \to \frac{1}{6} R_3 $$

$$
\begin{bmatrix} 1 & 2 & 1 & 9 \\
                   0 & 1 & 1 & 5 \\
                   0 & 0 & 1 & \frac{8}{3} \end{bmatrix}
$$

### c. Langkah 3 Substitusi Balik

#### **Langkah 3.1**: Dari baris terakhir:
$$
 z = \frac{8}{3} 
$$

#### **Langkah 3.2**: Substitusi $z$  ke baris kedua:
$$
 y + z = 5 \Rightarrow y + \frac{8}{3} = 5 \Rightarrow y = \frac{7}{3}
$$

#### **Langkah 3.3**: Substitusi $y$ dan $z$ ke baris pertama:
$$
 x + 2y + z = 9 \Rightarrow x + 2(\frac{7}{3}) + \frac{8}{3} = 9 \Rightarrow x = \frac{5}{3}
$$

### d. Solusi Akhir:
$$
 x = \frac{5}{3}, \quad y = \frac{7}{3}, \quad z = \frac{8}{3}
$$

---

## C. Tugas
#### a. Sistem Persamaan Dua Variabel
##### 1. Memiliki 1 Titik Potong
$$
\begin{aligned}
y = 2x + 1 \\
y = -x + 4 \\
\end{aligned}
$$

<iframe src="https://www.geogebra.org/graphing/mprzavhw" width="800" height="600" style="border:0;"></iframe>

##### 2. Memiliki Banyak Titik Potong
$$
\begin{aligned}
y = 3x - 2 \\
2y = 6x - 4 \\
\end{aligned}
$$

<iframe src="https://www.geogebra.org/graphing/ydme3cuu" width="800" height="600" style="border:0;"></iframe>

##### 3. Tidak Memiliki  Titik Potong
$$
\begin{aligned}
y = 2x + 3 \\
y = 2x - 1 \\
\end{aligned}
$$

<iframe src="https://www.geogebra.org/graphing/yrexaspt" width="800" height="600" style="border:0;"></iframe>

#### b. Sistem Persamaan Tiga Variabel
##### 1. Memiliki 1 Titik Potong
$$
\begin{aligned}
x + y + z &= 6 \\
2x - y + 3z &= 14 \\
-x + 2y - z &= -2
\end{aligned}
$$

<iframe src="https://www.geogebra.org/3d/hed8kshm" width="800" height="600" style="border:0;"></iframe>

##### 2. Memiliki Banyak Titik Potong
$$
\begin{aligned}
x + y + z &= 6 \\
2x + 2y + 2z &= 12 \\
3x + 3y + 3z &= 18
\end{aligned}
$$

<iframe src="https://www.geogebra.org/3d/qpqra5sr" width="800" height="600" style="border:0;"></iframe>

##### 3. Tidak Memiliki Titik Potong
$$
\begin{aligned}
x + y + z &= 6 \\
x + y + z &= 8 \\
x + y + z &= 10
\end{aligned}
$$

<iframe src="https://www.geogebra.org/3d/repkbdzz" width="800" height="600" style="border:0;"></iframe>

## D. Referensi
- https://linearalgebra.math.umanitoba.ca/math1220/section-11.html







