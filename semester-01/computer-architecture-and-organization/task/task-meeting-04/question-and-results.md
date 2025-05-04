**Operasi Aritmetika Biner & Representasi Floating Point  
# Questions:
# ['TUGAS PERTEMUAN KE-4_ Operasi Aritmatika Biner Dan Representasi Floating Point.pdf']
# (./'TUGAS PERTEMUAN KE-4_ Operasi Aritmatika Biner Dan Representasi Floating Point.pdf')
# Results:
# ['TUGAS PERTEMUAN KE-4-SISTEM PENGUKURAN SUHU.docx']
# (./'TUGAS PERTEMUAN KE-4-SISTEM PENGUKURAN SUHU.docx')

## 📌 Soal

Diketahui sebuah ruang server menyimpan data suhu dalam format **biner 8-bit**, dan suhu optimal adalah **20°C – 25°C**. Pencatatan suhu selama 3 jam adalah:

1. Jam 1: 23,5°C  
2. Jam 2: 26,75°C  
3. Jam 3: 22,25°C

### Pertanyaan:
1. Bagaimana cara mengkonversi semua suhu ke **floating point** (IEEE 754 32-bit)?  
2. Bagaimana cara menghitung **rata-rata suhu** dalam floating point?  
3. Bagaimana cara menganalisis apakah suhu rata-rata dalam **rentang optimal**?

---

## ✅ Jawaban dan Pembahasan

### 1. Konversi Suhu ke IEEE 754 Floating Point (32-bit)

IEEE 754 format:  
| 1 bit sign | 8 bit exponent | 23 bit fraction |

#### a. Jam 1: 23.5°C  
- **Desimal → Biner**:  
  23 = `10111`, 0.5 = `0.1` → 23.5 = `10111.1`  
- **Normalisasi**: `1.01111 × 2^4`  
- **Eksponen**: 4 + bias (127) = **131** → `10000011`  
- **Fraction**: `01111000000000000000000`  
- **Hasil IEEE 754**:  
  `0 10000011 01111000000000000000000` → **0x41BC0000**

#### b. Jam 2: 26.75°C  
- 26 = `11010`, 0.75 = `0.11` → 26.75 = `11010.11`  
- Normalisasi: `1.101011 × 2^4`  
- Eksponen: 4 + 127 = **131** → `10000011`  
- Fraction: `10101100000000000000000`  
- IEEE 754:  
  `0 10000011 10101100000000000000000` → **0x41D60000**

#### c. Jam 3: 22.25°C  
- 22 = `10110`, 0.25 = `0.01` → 22.25 = `10110.01`  
- Normalisasi: `1.011001 × 2^4`  
- Eksponen: 4 + 127 = **131** → `10000011`  
- Fraction: `01100100000000000000000`  
- IEEE 754:  
  `0 10000011 01100100000000000000000` → **0x41B20000**

---

### 2. Menghitung Rata-rata Suhu dalam Floating Point

Suhu dalam desimal:
- 23.5 + 26.75 + 22.25 = **72.5**

Rata-rata:
- 72.5 ÷ 3 = **24.16666...**

#### Konversi ke IEEE 754:
- 24 = `11000`, 0.1666... ≈ `0.001010101010...`  
- Normalisasi: `1.100010101010101... × 2^4`  
- Eksponen: 4 + 127 = **131** → `10000011`  
- Fraction: `10001010101010101010101`  
- IEEE 754:  
  `0 10000011 10001010101010101010101` → **0x41C55555 (approx)**

---

### 3. Analisis: Apakah Rata-rata Suhu Dalam Rentang Optimal?

- Rata-rata: **24.17°C**  
- Rentang optimal: **20.0 – 25.0°C**  
✅ Maka suhu rata-rata **masih dalam rentang optimal**.

---

## 📎 Kesimpulan

- Ketiga suhu berhasil dikonversi ke format **floating point IEEE 754** 32-bit.
- Rata-rata suhu dihitung secara akurat dalam bentuk floating point.
- Hasil analisis menunjukkan suhu rata-rata **masih aman dan optimal** untuk server.

---

## 🔢 Ringkasan Nilai Heksadesimal (IEEE 754)
| Jam | Suhu (°C) |        Representasi IEEE 754       |     Hex     |
|-----|-----------|------------------------------------|-------------|
| 1   | 23.5      | 0 10000011 01111000000000000000000 | 0x41BC0000  |
| 2   | 26.75     | 0 10000011 10101100000000000000000 | 0x41D60000  |
| 3   | 22.25     | 0 10000011 01100100000000000000000 | 0x41B20000  |
| Avg | 24.166... | 0 10000011 10001010101010101010101 | ~0x41C55555 |


