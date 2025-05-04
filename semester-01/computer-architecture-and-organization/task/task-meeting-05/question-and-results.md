# Aljabar Boolean dan Gerbang Logika Questions:
# [Boolean-Algebra-and-Logic-Gates-13102024.pdf]
# (./Boolean-Algebra-and-Logic-Gates-13102024.pdf)
# Results:
# ['TUGAS PERTEMUAN KE-5.docx']
# (./'TUGAS PERTEMUAN KE-5.docx')


Kelompok:

Shifi Amalia Zein

Nabilaturohmah

Bilal

M. Ma’rufil Kurhi

Abdullah Mubarak Maspeke

1. Kombinasi Gerbang Logika
a. Soal 1:
Dua input dimasukkan ke gerbang AND, kemudian hasilnya masuk ke gerbang NOT.
Rumus: F = (A . B)'

A	B	A . B	(A . B)'
0	0	0	1
0	1	0	1
1	0	0	1
1	1	1	0

Penjelasan:
AND menghasilkan 1 hanya jika keduanya 1. NOT membalik hasil AND.

b. Soal 2:
Dua input dimasukkan ke gerbang OR, kemudian hasilnya masuk ke gerbang NOT.
Rumus: F = (A + B)'

A	B	A + B	(A + B)'
0	0	0	1
0	1	1	0
1	0	1	0
1	1	1	0

Penjelasan:
OR menghasilkan 1 jika salah satu bernilai 1. NOT membalik hasil OR.

2. Fungsi Boolean dan Tabel Kebenaran
a. Fungsi: F = A . B'
B' artinya B dibalik menggunakan NOT.
A dan B' kemudian masuk ke gerbang AND.

A	B	B'	A . B'
0	0	1	0
0	1	0	0
1	0	1	1
1	1	0	0

b. Fungsi: F = A + B'
B' adalah NOT dari B. A dan B' masuk ke gerbang OR.

A	B	B'	A + B'
0	0	1	1
0	1	0	0
1	0	1	1
1	1	0	1

3. Implementasi Fungsi Boolean
a. Fungsi: F = (A + B) . C
A	B	C	A + B	F = (A + B).C
0	0	0	0	0
0	1	0	1	0
1	0	0	1	0
1	1	0	1	0
0	0	1	0	0
0	1	1	1	1
1	0	1	1	1
1	1	1	1	1

b. Fungsi: F = A.B + B.C + A.C
Tiga buah gerbang AND dan dua OR untuk menggabungkan hasil.

A	B	C	A.B	B.C	A.C	F = A.B + B.C + A.C
0	0	0	0	0	0	0
0	0	1	0	0	0	0
0	1	0	0	0	0	0
0	1	1	0	1	0	1
1	0	0	0	0	0	0
1	0	1	0	0	1	1
1	1	0	1	0	0	1
1	1	1	1	1	1	1

4. Penyederhanaan Gerbang Logika
a. Fungsi Kompleks: F = (A+B)'.(A+C)'.(B+C)'
Disederhanakan menjadi:
F = (A'.B').(A'.C').(B'.C') = A'.B'.C'

A	B	C	A+B	A+C	B+C	(A+B)'	(A+C)'	(B+C)'	F = A'.B'.C'
0	0	0	0	0	0	1	1	1	1
0	0	1	0	1	1	1	0	0	0
0	1	0	1	0	1	0	1	0	0
0	1	1	1	1	1	0	0	0	0
1	0	0	1	1	0	0	0	1	0
1	0	1	1	1	1	0	0	0	0
1	1	0	1	1	1	0	0	0	0
1	1	1	1	1	1	0	0	0	0

✅ Kesimpulan
Dokumen ini membahas:

Kombinasi dasar gerbang logika (AND, OR, NOT)

Penyusunan tabel kebenaran untuk fungsi Boolean

Implementasi fungsi logika dalam bentuk kombinasi gerbang

Penyederhanaan logika menggunakan identitas Boolean

Dokumen ini penting untuk memahami implementasi logika digital dalam desain sirkuit komputer.
