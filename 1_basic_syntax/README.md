# Basic Syntax

Bahasa Python memiliki sintaks yang relatif sederhana dan mudah dipelajari. Berikut adalah beberapa sintaks dasar Python:

## Comment

Comment adalah catatan yang dapat dimasukkan ke dalam kode untuk menjelaskan apa yang dilakukan oleh kode tersebut. Comment dimulai dengan tanda pound (#).

```python
# Ini adalah contoh comment dalam satu baris
# dan ini adalah comment baris kedua

"""
Ini adalah multi-line comment atau biasa disebut juga sebagai docs string

Dengan cara ini kita dapat membuat sebuah dokumentasi kode yang kita buat,
cara ini biasa dipakai untuk mendokumentasikan sebuah class atau fungsi. Sejatinya
comment seperti ini merupakan sebuah multi-line string (akan dijelaskan disection tipe data string dibawah)
"""
```

## Indentasi

Python menggunakan indentasi untuk menentukan blok kode. Blok kode adalah sekumpulan pernyataan yang dikelompokkan bersama. Indentasi standar di Python adalah 2 atau 4 spasi..

```python
a = "variable dalam outer scope"
print(a) # kode akan tereksekusi tanpa error, karna variable a dalam jangkauan

    b = "variable dalam inner scope"
    print(a) # kode akan tereksekusi tanpa error, karna variable a masih bisa dijangkau walaupun berada di scope luar
    print(b) # kode akan tereksekusi tanpa error, karna variable b dalam jangkauan

print(b) # kode error, variable a tidak terbaca karena ada pada block scope berbeda, dan outer scope tidak bisa membaca variable yang terdefinisi di inner scope
```

## Variabel

Variabel adalah tempat penyimpanan nilai. Variabel pada python bersifat mutable, artinya nilainya bisa berubah-ubah. Variabel diberi nama dengan huruf, angka, atau tanda underscore (`_`). Nama variabel bersifat case-sensitive (yang artinya perbedaan huruf besar dan huruf kecil sangat berpengaruh).

Berikut adalah aturan penulisan variabel pada Python:

- Karakter pertama harus berupa huruf atau garis bawah/underscore (`_`).
- Karakter selanjutnya dapat berupa huruf, garis bawah/underscore (`_`) atau angka.
- Karakter pada nama variabel bersifat sensitif (case-sensitif), Yang artinya perbedaan huruf besar dan huruf kecil sangat berpengaruh.
- Nama variabel tidak boleh menggunakan kata kunci yang sudah ada dalam python seperti `if` , `while` , `for` , dsb.

Berikut adalah contoh penulisan variabel pada Python:

```python
# Variabel string
nama = "Satoru Dawwam"
alamat = "Telkom University Landmark Tower Lantai 11 no 08 (TULT 11.08)"

# Variabel numerik
umur = 74
tinggi_badan = 301.8

# Variabel boolean
sudah_menikah = True

# Variabel list
angka = [1, 2, 3, 4, 5]

# Variabel tuple
hari_kuliah = ("Senin", "Selasa", "Rabu", "Kamis", "Jumat")

# Variabel dictionary
data = {"nama": "John Doe", "alamat": "Jl. Jendral Sudirman No. 100"}
```

Variabel dapat digunakan untuk menyimpan data yang akan digunakan dalam program. Variabel dapat digunakan untuk membuat kode yang lebih efisien dan efektif.

Berikut adalah beberapa manfaat variabel pada Python:

- Mudah digunakan dan dibaca.
- Dapat digunakan untuk menyimpan data dalam jumlah besar.
- Dapat digunakan untuk membuat kode yang lebih efisien dan efektif.

## Statement

Statement adalah instruksi yang diberikan kepada komputer untuk melakukan sesuatu. Berbeda dengan bahasa pemrograman lain, python tidak mengharuskan statement diakhiri dengan tanda titik koma (;).

Ada beberapa jenis statement pada Python, yaitu:

- Assignment statement digunakan untuk mengasignkan nilai ke variabel.
- Arithmetic statement digunakan untuk melakukan operasi aritmatika.
- Comparison statement digunakan untuk membandingkan dua nilai.
- Logical statement digunakan untuk menggabungkan dua atau lebih pernyataan logika.
- Control flow statement digunakan untuk mengontrol aliran eksekusi kode.

Berikut adalah contoh penulisan statement pada Python:

```python
# Assignment statement
a = 10
b = 20

# Arithmetic statement
c = a + b

# Comparison statement
d = a == b

# Logical statement
e = a > b and c < d

# Control flow statement
if a > b:
    print("a lebih besar dari b")
else:
    print("b lebih besar dari a")
```

- ### Assignment statement

  Assignment statement digunakan untuk mengasignkan nilai ke variabel. Sintaks penulisan assignment statement adalah sebagai berikut:

  ```python
  variable = value
  ```

  contoh:

  ```python
  a = 10
  b = "Hello, world!"
  ```

- ### Arithmetic statement

  Arithmetic statement digunakan untuk melakukan operasi aritmatika. Operator aritmatika yang tersedia di Python adalah sebagai berikut:

  | Operator | Keterangan        |
  | -------- | ----------------- |
  | `x`      | penjumlahan       |
  | `-`      | Pengurangan       |
  | `*`      | Perkalian         |
  | `/`      | Pembagian         |
  | `//`     | Pembagian Kebawah |
  | `%`      | Modulus           |
  | `**`     | exponensial       |

  contoh:

  ```python
  a = 10 + 20
  b = 10 - 20
  c = 10 * 20
  d = 10 / 20
  e = 10 % 20
  f = 10 ** 20
  ```

- ### Comparison statement

  Comparison statement digunakan untuk membandingkan dua nilai. Operator perbandingan yang tersedia di Python adalah sebagai berikut:

  | Operator | Keterangan                        |
  | -------- | --------------------------------- |
  | `==`     | Sama dengan                       |
  | `!=`     | Tidak Sama dengan                 |
  | `>`      | Lebih besar dari                  |
  | `<`      | Lebih kecil dari                  |
  | `>=`     | Lebih besar atau sama dengan dari |
  | `<=`     | Lebih besar atau sama dengan dari |

  contoh:

  ```python
  a = 10
  b = 20

  c = a == b
  d = a != b
  e = a > b
  f = a < b
  g = a >= b
  h = a <= b
  ```

- ### Logical statement

  Logical statement digunakan untuk menggabungkan dua atau lebih pernyataan logika. Operator logika yang tersedia di Python adalah sebagai berikut:

  | Operator | Keterangan |
  | -------- | ---------- |
  | `and`    | Dan        |
  | `or`     | Atau       |
  | `not`    | Bukanm     |

  contoh:

  ```python
  a = True
  b = False

  c = a and b
  d = a or b
  e = not a
  ```
