---
title: Aljabar Matriks

---

# Aljabar Matriks
$$
\textbf{Sifat-Sifat Operasi Matriks, Invers Aditif, dan Matriks Identitas}
$$

Matriks adalah sekumpulan bilangan yang disusun dalam bentuk baris dan kolom. Operasi pada matriks memiliki sifat-sifat khusus yang perlu diperhatikan.

---

## 1. Sifat Penjumlahan Matriks
Jika $A, B, C$ adalah matriks dengan ukuran yang sama, maka berlaku sifat-sifat berikut:

- **Asosiatif**: 
  $(A + B) + C = A + (B + C)$
  Artinya, urutan pengelompokan tidak mempengaruhi hasil penjumlahan.

- **Komutatif**: 
  $A + B = B + A$
  Artinya, urutan penjumlahan tidak mempengaruhi hasilnya.

- **Elemen Identitas** (Matriks Nol):
  $A + O = A$ 
  dengan $O$ adalah matriks nol, yaitu matriks yang semua elemennya nol.

- **Elemen Invers** (Invers Aditif): 
  $A + (-A) = O$
  dengan $-A$ adalah matriks yang elemennya merupakan negatif dari elemen-elemen $A$.

---

## 2. Sifat Perkalian Matriks
Jika $A, B, C$ adalah matriks dengan ukuran yang sesuai untuk operasi perkalian, maka berlaku:

- **Asosiatif**:
  $(A \cdot B) \cdot C = A \cdot (B \cdot C)$
  Artinya, urutan pengelompokan tidak mempengaruhi hasil perkalian.

- **Distributif terhadap Penjumlahan**:
  $A \cdot (B + C) = A \cdot B + A \cdot C$ 
  dan 
  $(A + B) \cdot C = A \cdot C + B \cdot C$
  Perkalian matriks dapat didistribusikan terhadap penjumlahan matriks.

- **Elemen Identitas** (Matriks Identitas):
  $A \cdot I = A$
  dengan $I$ adalah matriks identitas, yaitu matriks persegi dengan elemen diagonal utama bernilai 1 dan elemen lainnya nol.

- **Tidak Komutatif** (Perkalian Tidak Bersifat Komutatif):
  $A \cdot B \neq B \cdot A$
  Dalam banyak kasus, hasil perkalian dua matriks tergantung pada urutannya.

---

## 3. Sifat Perkalian Skalar
Jika $A$ adalah matriks dan $c, d$ adalah skalar (bilangan real atau kompleks), maka:

- **Distribusi terhadap Penjumlahan**:
  $c(A + B) = cA + cB$
  Artinya, perkalian skalar dapat didistribusikan terhadap penjumlahan matriks.

- **Distribusi terhadap Skalar**:
  $(c + d)A = cA + dA$
  Artinya, jumlah dua skalar yang dikalikan dengan matriks sama dengan jumlah hasil perkalian masing-masing skalar dengan matriks tersebut.

- **Asosiatif Skalar**:
  $c(dA) = (cd)A$
  Perkalian dua skalar dengan suatu matriks bisa dilakukan secara bertahap tanpa mengubah hasil.

---

## 4. Invers Aditif
Untuk setiap matriks $A$, terdapat matriks $-A$ yang disebut invers aditif, yang memenuhi:
  $A + (-A) = O$
  dengan $-A$ adalah matriks yang semua elemennya merupakan negatif dari elemen $A$.

---

## 5. Matriks Identitas
Matriks identitas, dilambangkan dengan $I$, adalah matriks persegi yang memiliki elemen 1 di diagonal utama dan 0 di luar diagonal utama. Contoh:

  $$
  I_2 = \begin{bmatrix} 
  1 & 0 \\ 
  0 & 1 
  \end{bmatrix}, \quad
  I_3 = \begin{bmatrix} 
  1 & 0 & 0 \\ 
  0 & 1 & 0 \\ 
  0 & 0 & 1 
  \end{bmatrix}
  $$

Matriks identitas memiliki sifat:
  $A \cdot I = A$
  untuk setiap matriks $A$ dengan ukuran yang sesuai.

---

## 6. Menghitung Invers Matriks
Matriks persegi $A$ memiliki invers $A^{-1}$ jika memenuhi:
  $A \cdot A^{-1} = A^{-1} \cdot A = I$
  Artinya, perkalian antara matriks dan inversnya menghasilkan matriks identitas.

**Syarat suatu matriks memiliki invers:**
1. Matriks harus berbentuk **persegi** (jumlah baris sama dengan jumlah kolom).
2. Determinan matriks tidak boleh nol, yaitu:
   $\det(A) \neq 0$

---

## 7. Menghitung Invers dengan OBE (Operasi Baris Elementer)
Metode OBE digunakan untuk menghitung invers suatu matriks. Langkah-langkahnya:

1. Susun matriks augmented:
   $[ A \ | \ I ]$
   yaitu menggabungkan matriks $A$ dengan matriks identitas $I$.

2. Lakukan operasi baris elementer (OBE) hingga sisi kiri menjadi matriks identitas:
   $[ I \ | \ A^{-1} ]$

3. Matriks di sisi kanan $( A^{-1})$ adalah invers dari $( A)$.

Sebagai contoh, misalkan:

$$A = \begin{bmatrix} 
2 & 1 \\ 
3 & 4 
\end{bmatrix}$$

Maka inversnya dihitung dengan metode OBE atau rumus umum untuk matriks $2 \times 2$:

  $$
  A^{-1} = \frac{1}{\det(A)}
  \begin{bmatrix} 
  d & -b \\ 
  -c & a 
  \end{bmatrix}
  $$

dengan $\det(A) = ad - bc$. Jika $\det(A) \neq 0$, maka invers dapat dihitung.

---

### **Kesimpulan**
- Operasi matriks memiliki sifat **penjumlahan, perkalian, dan perkalian skalar** yang mengikuti aturan tertentu.
- **Matriks identitas** berperan sebagai elemen netral dalam perkalian matriks.
- **Invers matriks** hanya ada jika determinannya tidak nol, dan dapat dihitung menggunakan **OBE** atau rumus tertentu.

## 8. Tugas
1. Contoh persamaan 3 variabel dengan hasil invers 1, 0, 0
Jawaban:
### Persamaan:

$$\begin{aligned}
4x + 2y + z &= 4 \\
5x + y + 3z &= 5 \\
2x + y + 5z &= 2
\end{aligned}$$

### Langkah-Langkah

**1. Ubah Menjadi Bentuk Matrix**

$$\begin{aligned}
4x + 2y + z &= 4 \\
5x + y + 3z &= 5 \\
2x + y + 5z &= 2
\end{aligned}$$

$$
  \begin{bmatrix} 4 & 2 & 1 & 4 \\
                   5 & 1 & 3 & 5 \\
                   2 & 1 & 5 & 2 \end{bmatrix}
  $$
 
**2. Tulis Matriks Utamanya**

$$\begin{bmatrix} 
4 & 2 & 1\\
5 & 1 & 3\\
2 & 1 & 5
\end{bmatrix}$$

**3. Tulis matriks identitasnya disamping matriksnya**

$$\begin{bmatrix} 
4 & 2 & 1 & | 1 & 0 & 0\\
5 & 1 & 3 & | 0 & 1 & 0\\
2 & 1 & 5 & | 0 & 0 & 1
\end{bmatrix}$$

**4. Gunakan Eliminasi Gauss**
*Langkah 4.1 Jadikan baris 1, kolom 1 bernilai 1*

$$\frac{R_1}{4}$$

$$\begin{bmatrix} 
\frac{4}{4} & \frac{2}{4} & \frac{1}{4} & | \frac{1}{4} & 0 & 0\\
5 & 1 & 3 & | 0 & 1 & 0\\
2 & 1 & 5 & | 0 & 0 & 1
\end{bmatrix}$$

Hasil

$$\begin{bmatrix} 
1 & \frac{1}{2} & \frac{1}{4} & | \frac{1}{4} & \frac{0}{4} & \frac{0}{4}\\
5 & 1 & 3 & | 0 & 1 & 0\\
2 & 1 & 5 & | 0 & 0 & 1
\end{bmatrix}$$

*Langkah 4.2 Ubah baris 2 kolom 1 dan baris 3 kolom 1 menjadi 0*
 
- $$ R_2 \to R_2 - \frac{5}{4}R_1 $$

$$
\begin{bmatrix} 
1 & \frac{1}{2} & \frac{1}{4} & | \frac{1}{4} & 0 & 0\\
5 & 1 & 3 & | 0 & 1 & 0\\
2 & 1 & 5 & | 0 & 0 & 1
\end{bmatrix}
\rightarrow
\begin{bmatrix} 
1 & \frac{1}{2} & \frac{1}{4} & | \frac{1}{4} & 0 & 0\\
(5-\frac{5}{4}.4) & (1-\frac{5}{4}.2) & (3-\frac{5}{4}.1) & | (0-\frac{5}{4}.1)  & (1-\frac{5}{4}.0)  & (0-\frac{5}{4}.0)\\
2 & 1 & 5 & | 0 & 0 & 1
\end{bmatrix}
$$

Hasil dari $R_2$

$$\begin{bmatrix} 
1 & \frac{1}{2} & \frac{1}{4} & | \frac{1}{4} & 0 & 0\\
0 & \frac{-3}{2} & \frac{7}{4} & | \frac{-5}{4} & 1 & 0\\
2 & 1 & 5 & | 0 & 0 & 1
\end{bmatrix}$$

- $$ R_3 \to R_3 - \frac{1}{2}R_1 $$

$$\begin{bmatrix} 
1 & \frac{1}{2} & \frac{1}{4} & | \frac{1}{4} & 0 & 0\\
0 & \frac{-3}{2} & \frac{7}{4} & | \frac{-5}{4} & 1 & 0\\
(2-\frac{1}{2}.4) & (1-\frac{1}{2}.2) & (5-\frac{1}{2}.1) & | (0-\frac{1}{2}.1) & (0-\frac{1}{2}.0) & (1-\frac{1}{2}.0)
\end{bmatrix}$$

Hasil dari $R_3$

$$\begin{bmatrix} 
1 & \frac{1}{2} & \frac{1}{4} & | \frac{1}{4} & 0 & 0\\
0 & \frac{-3}{2} & \frac{7}{4} & | \frac{-5}{4} & 1 & 0\\
0 & 0 & \frac{9}{2} & | \frac{-1}{2} & 0 & 1
\end{bmatrix}$$

*Langkah 4.3 Jadikan baris 2 kolom 2 bernilai 1*

- $$ R_2 \to \frac{R_2}{\frac{-3}{2}} $$

$$\begin{bmatrix} 
1 & \frac{1}{2} & \frac{1}{4} & | \frac{1}{4} & 0 & 0\\
0 & \frac{\frac{-3}{2}}{\frac{-3}{2}} & \frac{\frac{7}{4}}{\frac{-3}{2}} & | \frac{\frac{-5}{4}}{\frac{-3}{2}} & \frac{1}{\frac{-3}{2}} & \frac{0}{\frac{-3}{2}}\\
0 & 0 & \frac{9}{2} & | \frac{-1}{2} & 0 & 1
\end{bmatrix}$$

Hasil

$$\begin{bmatrix} 
1 & \frac{1}{2} & \frac{1}{4} & | \frac{1}{4} & 0 & 0\\
0 & 1 & \frac{-7}{6} & | \frac{5}{6} & \frac{-2}{3} & 0\\
0 & 0 & \frac{9}{2} & | \frac{-1}{2} & 0 & 1
\end{bmatrix}$$

*Langkah 4.4 Ubah baris 1 kolom 2 menjadi 0*

$$\begin{bmatrix} 
1 & (\frac{1}{2}-\frac{1}{2}.1) & (\frac{1}{4}-\frac{1}{2}.\frac{-7}{6}) & | (\frac{1}{4}-\frac{1}{2}.\frac{5}{6}) & (0-\frac{1}{2}.\frac{-2}{3}) & (0-0)\\
0 & 1 & \frac{-7}{6} & | \frac{5}{6} & \frac{-2}{3} & 0\\
0 & 0 & \frac{9}{2} & | \frac{-1}{2} & 0 & 1
\end{bmatrix}$$

Hasil

$$\begin{bmatrix} 
1 & 0 & \frac{5}{6} & | \frac{-1}{6} & \frac{1}{3} & 0\\
0 & 1 & \frac{-7}{6} & | \frac{5}{6} & \frac{-2}{3} & 0\\
0 & 0 & \frac{9}{2} & | \frac{-1}{2} & 0 & 1
\end{bmatrix}$$

*Langkah 4.5 Ubah baris 3 kolom 3 menjadi 1*

- $$ R_3 \to \frac{R_3}{\frac{9}{2}} $$

$$\begin{bmatrix} 
1 & 0 & \frac{5}{6} & | \frac{-1}{6} & \frac{1}{3} & 0\\
0 & 1 & \frac{-7}{6} & | \frac{5}{6} & \frac{-2}{3} & 0\\
0 & 0 & \frac{\frac{9}{2}}{\frac{9}{2}} & | \frac{\frac{-1}{2}}{\frac{9}{2}} & \frac{0}{\frac{9}{2}} & \frac{1}{\frac{9}{2}}
\end{bmatrix}$$

Hasil

$$\begin{bmatrix} 
1 & 0 & \frac{5}{6} & | \frac{-1}{6} & \frac{1}{3} & 0\\
0 & 1 & \frac{-7}{6} & | \frac{5}{6} & \frac{-2}{3} & 0\\
0 & 0 & 1 & | \frac{-1}{9} & 0 & \frac{2}{9}
\end{bmatrix}$$

*Langkah 4.6 Ubah baris 1 kolom 3 menjadi 0*

- $$ R_1 \to R_1 - \frac{5}{6}R_3 $$

$$\begin{bmatrix} 
1 & 0 & (\frac{5}{6}-\frac{5}{6}.1) & | (\frac{-1}{6}- \frac{5}{6}.\frac{-1}{9}) & (\frac{1}{3}-\frac{5}{6}.0) & (0-\frac{5}{6}.\frac{2}{9})\\
0 & 1 & \frac{-7}{6} & | \frac{5}{6} & \frac{-2}{3} & 0\\
0 & 0 & 1 & | \frac{-1}{9} & 0 & \frac{2}{9}
\end{bmatrix}$$

Hasil

$$\begin{bmatrix} 
1 & 0 & 0 & | \frac{-2}{27} & \frac{1}{3} & \frac{-5}{27}\\
0 & 1 & \frac{-7}{6} & | \frac{5}{6} & \frac{-2}{3} & 0\\
0 & 0 & 1 & | \frac{-1}{9} & 0 & \frac{2}{9}
\end{bmatrix}$$

*Langkah 4.7 Ubah baris 2 kolom 3 menjadi 0*

- $$ R_2 \to R_2 - \frac{-7}{6}R_3 $$

$$\begin{bmatrix} 
1 & 0 & 0 & | \frac{-2}{27} & \frac{1}{3} & \frac{-5}{27}\\
0 & 1 & (\frac{-7}{6}-\frac{-7}{6}.1) & | (\frac{5}{6}-\frac{-7}{6}.\frac{-1}{9}) & (\frac{-2}{3}-\frac{-7}{6}.0) & (0-\frac{-7}{6}.\frac{2}{9})\\
0 & 0 & 1 & | \frac{-1}{9} & 0 & \frac{2}{9}
\end{bmatrix}$$

Hasil

$$\begin{bmatrix} 
1 & 0 & 0 & | \frac{-2}{27} & \frac{1}{3} & \frac{-5}{27}\\
0 & 1 & 0 & | \frac{19}{27} & \frac{-2}{3} & \frac{7}{27}\\
0 & 0 & 1 & | \frac{-1}{9} & 0 & \frac{2}{9}
\end{bmatrix}$$

Hasil akhir

$$\begin{bmatrix} 
\frac{-2}{27} & \frac{1}{3} & \frac{-5}{27}\\
\frac{19}{27} & \frac{-2}{3} & \frac{7}{27}\\
\frac{-1}{9} & 0 & \frac{2}{9}
\end{bmatrix}$$

**5. Setelah itu Gunakan Rumus $Ax=B$**

$$\begin{aligned}
Ax=B\\
A^{-1}Ax=A^{-1}B\\
Ix=A^{-1}B\\
x=A^{-1}B\end{aligned}$$

$$\begin{bmatrix} 
x\\
y\\
z\end{bmatrix}
= \begin{bmatrix} 
\frac{-2}{27} & \frac{1}{3} & \frac{-5}{27}\\
\frac{19}{27} & \frac{-2}{3} & \frac{7}{27}\\
\frac{-1}{9} & 0 & \frac{2}{9}
\end{bmatrix}
\begin{bmatrix} 
4\\
5\\
2\end{bmatrix}
=\begin{bmatrix} 
(\frac{-2}{27}.4) + (\frac{1}{3}.5) + (\frac{-5}{27}.2)\\
(\frac{19}{27}.4) + (\frac{-2}{3}.5) + (\frac{7}{27}.2)\\
(\frac{-1}{9}.4) + (0.5) + (\frac{2}{9}.2)
\end{bmatrix}
=\begin{bmatrix} 
1\\
0\\
0\end{bmatrix}$$
