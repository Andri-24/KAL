---
title: Transformasi Linear

---

# Transformasi Linear

## 1 Pengantar Transformasi Linier

Fungsi $T$ yang memetakan ruang vektor $V$ ke ruang vektor $W$:

$$
T: V \rightarrow W, \quad V,W: \text{ruang vektor}
$$

- $V$: domain $T$
- $W$: kodomain $T$

Diagram:

 ![image](https://hackmd.io/_uploads/HJXNIUIgee.png)
 

- Suatu fungsi dari $\mathbb{R}^2$ ke $\mathbb{R}^2$

$$
T : \mathbb{R}^2 \rightarrow \mathbb{R}^2 \quad \mathbf{v} = (v_1, v_2) \in \mathbb{R}^2
$$

$$
T(v_1, v_2) = (v_1 - v_2, v_1 + 2v_2)
$$

**(a)** Cari bayangan $\mathbf{v} = (-1, 2)$.  
**(b)** Cari prabayangan $\mathbf{w} = (-1, 11)$.

### Solusi:

**(a)** 
$$
\mathbf{v} = (-1, 2) \\
\Rightarrow T(\mathbf{v}) = T(-1, 2) = (-1 - 2, -1 + 2 \times 2) = (-3, 3)
$$

**(b)** 
$$
T(\mathbf{v}) = \mathbf{w} = (-1, 11) \\
T(v_1, v_2) = (v_1 - v_2, v_1 + 2v_2) = (-1, 11) \\
\Rightarrow \begin{cases}
v_1 - v_2 = -1 \\
v_1 + 2v_2 = 11
\end{cases} \\
\Rightarrow v_1 = 3, \, v_2 = 4 \quad \text{Sehingga } \{(3, 4)\} \text{ adalah prabayangan dari } \mathbf{w} = (-1, 11).
$$

Misalkan $V$ dan $W$ adalah ruang vektor.  
Sebuah fungsi $T: V \rightarrow W$ disebut **transformasi linear** dari $V$ ke $W$ jika memenuhi dua syarat berikut:

1. **Sifat Penjumlahan**  
   $$T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v}), \quad \forall \mathbf{u}, \mathbf{v} \in V$$

2. **Sifat Perkalian Skalar**  
   $$T(c\mathbf{u}) = cT(\mathbf{u}), \quad \forall c \in \mathbb{R}$$

Diberikan transformasi:
$$
T(v_1, v_2) = (v_1 - v_2, v_1 + 2v_2)
$$

### Bukti Sifat Linear

Misalkan:
- $\mathbf{u} = (u_1, u_2) \in \mathbb{R}^2$
- $\mathbf{v} = (v_1, v_2) \in \mathbb{R}^2$ 
- $c \in \mathbb{R}$ (bilangan real)

#### 1. Mempertahankan Penjumlahan Vektor

$$
\begin{aligned}
\mathbf{u} + \mathbf{v} &= (u_1 + v_1, u_2 + v_2) \\
T(\mathbf{u} + \mathbf{v}) &= T(u_1 + v_1, u_2 + v_2) \\
&= \big((u_1 + v_1) - (u_2 + v_2),\ (u_1 + v_1) + 2(u_2 + v_2)\big) \\
&= \big((u_1 - u_2) + (v_1 - v_2),\ (u_1 + 2u_2) + (v_1 + 2v_2)\big) \\
&= (u_1 - u_2, u_1 + 2u_2) + (v_1 - v_2, v_1 + 2v_2) \\
&= T(\mathbf{u}) + T(\mathbf{v})
\end{aligned}
$$

#### 2. Mempertahankan Perkalian Skalar

$$
\begin{aligned}
c\mathbf{u} &= c(u_1, u_2) = (cu_1, cu_2) \\
T(c\mathbf{u}) &= T(cu_1, cu_2) \\
&= (cu_1 - cu_2, cu_1 + 2cu_2) \\
&= c(u_1 - u_2, u_1 + 2u_2) \\
&= cT(\mathbf{u})
\end{aligned}
$$

### Kesimpulan
Karena $T$ memenuhi kedua sifat:
1. $T(\mathbf{u} + \mathbf{v}) = T(\mathbf{u}) + T(\mathbf{v})$
2. $T(c\mathbf{u}) = cT(\mathbf{u})$

maka $T$ **adalah transformasi linear** dari $\mathbb{R}^2$ ke $\mathbb{R}^2$.

## 2. Tugas 

### 1. Refleksi Terhadap Sumbu X
**Matriks Transformasi:**

$$
\begin{pmatrix}
1 & 0 \\
0 & -1 \\
\end{pmatrix}
$$

**Contoh Perhitungan:**
- Titik $A(2, 3)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  1 & 0 \\
  0 & -1 \\
  \end{pmatrix}
  \begin{pmatrix}
  2 \\ 3
  \end{pmatrix} =
  \begin{pmatrix}
  2 \\ -3
  \end{pmatrix} \Rightarrow A'(2, -3)
  $$
  
<iframe src="https://www.geogebra.org/calculator/tmchhnd4" width="800" height="600" style="border:0px;"> </iframe>

- Titik $A(-1, 4)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  1 & 0 \\
  0 & -1 \\
  \end{pmatrix}
  \begin{pmatrix}
  -1 \\ -4
  \end{pmatrix} =
  \begin{pmatrix}
  -1 \\ -4
  \end{pmatrix} \Rightarrow A'(-1, -4)
  $$

<iframe src="https://www.geogebra.org/calculator/hrt2xack" width="800" height="600" style="border:0px;"> </iframe>

---

### 2. Refleksi Terhadap Sumbu Y
**Matriks Transformasi:**

$$
\begin{pmatrix}
-1 & 0 \\
0 & 1 \\
\end{pmatrix}
$$

**Contoh Perhitungan:**
- Titik $B(-1, 4)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  -1 & 0 \\
  0 & 1 \\
  \end{pmatrix}
  \begin{pmatrix}
  -1 \\ 4
  \end{pmatrix} =
  \begin{pmatrix}
  1 \\ 4
  \end{pmatrix} \Rightarrow B'(1, 4)
  $$

<iframe src="https://www.geogebra.org/calculator/wgq6psq7" width="800" height="600" style="border:0px;"> </iframe>

- Titik $B(-3, -6)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  -1 & 0 \\
  0 & 1 \\
  \end{pmatrix}
  \begin{pmatrix}
  -3 \\ -6
  \end{pmatrix} =
  \begin{pmatrix}
  3 \\ -6
  \end{pmatrix} \Rightarrow B'(3, -6)
  $$

<iframe src="https://www.geogebra.org/calculator/zd43ktct" width="800" height="600" style="border:0px;"> </iframe>

---

### 3. Refleksi Terhadap Garis $y = x$
**Matriks Transformasi:**

$$
\begin{pmatrix}
0 & 1 \\
1 & 0 \\
\end{pmatrix}
$$

**Contoh Perhitungan:**
- Titik $C(5, -2)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  0 & 1 \\
  1 & 0 \\
  \end{pmatrix}
  \begin{pmatrix}
  5 \\ -2
  \end{pmatrix} =
  \begin{pmatrix}
  -2 \\ 5
  \end{pmatrix} \Rightarrow C'(-2, 5)
  $$
  
<iframe src="https://www.geogebra.org/calculator/xayzh8yj" width="800" height="600" style="border:0px;"> </iframe>
  
- Titik $C(1, 4)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  0 & 1 \\
  1 & 0 \\
  \end{pmatrix}
  \begin{pmatrix}
  1 \\ 4
  \end{pmatrix} =
  \begin{pmatrix}
  4 \\ 1
  \end{pmatrix} \Rightarrow C'(4, 1)
  $$
  
<iframe src="https://www.geogebra.org/calculator/c3je9qen" width="800" height="600" style="border:0px;"> </iframe>

---

### 4. Refleksi Terhadap Garis $y = -x$
**Matriks Transformasi:**

$$
\begin{pmatrix}
0 & -1 \\
-1 & 0 \\
\end{pmatrix}
$$

**Contoh Perhitungan:**
- Titik $D(-3, -6)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  0 & -1 \\
  -1 & 0 \\
  \end{pmatrix}
  \begin{pmatrix}
  -3 \\ -6
  \end{pmatrix} =
  \begin{pmatrix}
  6 \\ 3
  \end{pmatrix} \Rightarrow D'(6, 3)
  $$
  
<iframe src="https://www.geogebra.org/calculator/yajftrph" width="800" height="600" style="border:0px;"> </iframe>
  
- Titik $D(-4, 1)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  0 & -1 \\
  -1 & 0 \\
  \end{pmatrix}
  \begin{pmatrix}
  -4 \\ 1
  \end{pmatrix} =
  \begin{pmatrix}
  -1 \\ 4
  \end{pmatrix} \Rightarrow D'(-1, 4)
  $$
  
<iframe src="https://www.geogebra.org/calculator/tydkbqn4" width="800" height="600" style="border:0px;"> </iframe>

---

### 5. Refleksi Terhadap Titik Asal $(0,0)$
**Matriks Transformasi:**

$$
\begin{pmatrix}
-1 & 0 \\
0 & -1 \\
\end{pmatrix}
$$

**Contoh Perhitungan:**
- Titik $E(2, -3)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  -1 & 0 \\
  0 & -1 \\
  \end{pmatrix}
  \begin{pmatrix}
  2 \\ -3
  \end{pmatrix} =
  \begin{pmatrix}
  -2 \\ 3
  \end{pmatrix} \Rightarrow E'(-2, 3)
  $$
  
<iframe src="https://www.geogebra.org/calculator/vwvuu2ze" width="800" height="600" style="border:0px;"> </iframe>
  
- Titik $E(-5, -7)$:

  $$
  \begin{pmatrix}
  x' \\ y'
  \end{pmatrix} = 
  \begin{pmatrix}
  -1 & 0 \\
  0 & -1 \\
  \end{pmatrix}
  \begin{pmatrix}
  -5 \\ -7
  \end{pmatrix} =
  \begin{pmatrix}
  5 \\ 7
  \end{pmatrix} \Rightarrow E'(5, 7)
  $$

<iframe src="https://www.geogebra.org/calculator/bsnhbfrh" width="800" height="600" style="border:0px;"> </iframe>