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

  | Operator | Keterangan  |
  | -------- | ----------- |
  | `x`      | penjumlahan |
  | `-`      | Pengurangan |
  | `*`      | Perkalian   |
  | `/`      | Pembagian   |
  | `%`      | Modulus     |
  | `\*\*`   | exponensial |

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

- ### Control flow statement

  Control flow statement digunakan untuk mengontrol aliran eksekusi kode. Jenis control flow statement yang tersedia di Python adalah sebagai berikut:

  - **If** statement digunakan untuk mengeksekusi kode jika kondisi bernilai benar.

  ```python
  a = 10

  if a > 5:
    # block code ini akan tereksekusi karna a = 10 dan 10 lebih besar dari 5
    print("a lebih besar dari 5")

  print("aku akan terseksekusi, apapun yg terjadi pada kondisi if diatas :)")
  ```

  - **Else** statement digunakan untuk mengeksekusi kode jika kondisi bernilai salah.

    ```python
    a = 10

    if a > 5:
      # block code ini akan tereksekusi karna a = 10 dan 10 lebih besar dari 5
      print("a lebih besar dari 5")
    else:
      # block code ini tidak akan tereksekusi karna a = 10 dan 10 tidak lebih besar dari 5
      print("a tidak lebih besar dari 5")
    ```

  - **Elif** statement digunakan untuk mengeksekusi kode jika kondisi pertama bernilai salah dan kondisi kedua bernilai benar.

    ```python
    a = 8
    if a > 10:
      # block code ini tidak akan tereksekusi karna a = 8 dan 8 tidak lebih besar dari 10
      print("a lebih besar dari 10")
    elif a > 5:
      # block code ini akan tereksekusi karna a = 8 dan 8  lebih besar dari 5
      print("a lebih besar dari 5")
    else:
      """
      block code ini akan tereksekusi jika dan hanya jika hasil dari statement if/elif
      diatasnya bernilai salah, pada kasus ini, block code ini tidak tereksekusi
      karna variable a memenuhi kondisi di block code elif
      """
      print("a tidak lebih besar dari 5")
    ```

  - **For loop** digunakan untuk mengulangi eksekusi kode hingga suatu kondisi terpenuhi.

    ```python
    for i in range(10):
      print(f"aku perulangan ke-{i}")
    ```

  - **While loop** digunakan untuk mengulangi eksekusi kode selama suatu kondisi bernilai benar.
    ```python
    a = 10
    while a > 0:
      print(a)
      a -= 1
    ```

## Tipe data

Tipe data pada Python adalah klasifikasi dari data yang disimpan di dalam variabel.Tipe data menentukan jenis data yang dapat disimpan dalam variabel. Python memiliki berbagai tipe data, termasuk integer, float, string, boolean, dan list.

Python memiliki berbagai macam tipe data, yang dapat dikelompokkan menjadi dua kategori utama, yaitu:

- ### Tipe data primitif

  adalah tipe data dasar yang tidak dapat dipecah menjadi tipe data yang lebih kecil. Tipe data primitif yang tersedia di Python adalah sebagai berikut:

  - #### Integer
    adalah tipe data untuk menyimpan bilangan bulat. Integer dapat berupa bilangan positif, negatif, atau nol.
    ```python
    umur = 20
    diskon_nilai = -10
    nilai_uts = 0
    ```
  - #### Float
    adalah tipe data untuk menyimpan bilangan desimal. Float dapat berupa bilangan desimal positif, negatif, atau nol.
    ```python
    tinggi_badan = 173.2
    a = -10.5
    b = 0.0
    ```
  - #### String

    adalah tipe data untuk menyimpan teks. String dapat berupa karakter, kata, kalimat, atau bahkan paragraf.

    ```python
    a = "Hello, world!"
    b = 'Python'
    c = '10.5'
    multi_line_str = """
    Ini adalah multi line string,

    kamu bisa membuat sebuah paragraf dan sebagainya tanpa harus memperdulikan newline dan memformat sebuah string
    """
    ```

  - #### Boolean
    adalah tipe data untuk menyimpan nilai logika, yaitu True atau False.
    ```python
    a = True
    b = False
    c = not a # False
    d = not c # True
    ```

- ### Tipe data kompleks

  adalah tipe data yang dapat dipecah menjadi tipe data yang lebih kecil. Tipe data kompleks yang tersedia di Python adalah sebagai berikut:

  - #### List

    adalah tipe data untuk menyimpan kumpulan data. List dapat berupa kumpulan bilangan, kumpulan string, atau kumpulan data kompleks lainnya.

    ```python
    angka = [1, 3, 5, 7] # List of integers
    nama = ["Ridwan", "Maulana", "Tanjung"] # List of string
    data = [1, "Image Processing", True, (1, 0.5, 7)] # List of mixed data types
    ```

  - #### Tuple

    adalah tipe data untuk menyimpan kumpulan data yang tidak dapat diubah (immutable). Tuple dapat berupa kumpulan bilangan, kumpulan string, atau kumpulan data kompleks lainnya.

    ```Python
    fte_majors = ("Teknik Telekomunikasi", "Teknik Fisika", "Teknik Elektro", "Teknik Komputer", "Teknik Biomedis", "Teknik Sistem Energi") # Tuple of strings
    data = (1, "Jonathan Vito Setiawan", 2020, "IMV Assistant", True) # Tuple of mixed data types
    ```

  - #### Set

    adalah tipe data untuk menyimpan kumpulan data yang tidak memiliki urutan. Set dapat berupa kumpulan bilangan, kumpulan string, atau kumpulan data kompleks lainnya.

    ```python
    angka = {1, -2, 6, 0.2, 9, 1000000}  # Set of numeric
    imv = {'IMV', '2023', 'Kaya! Kaya! Kaya!'}  # Set of strings
    data = {1, "John Doe", True}  # Set of mixed data types
    ```

  - #### Dictionary

    adalah tipe data untuk menyimpan kumpulan data yang memiliki pasangan kunci-nilai. Dictionary dapat digunakan untuk menyimpan data dalam bentuk tabel.

    ```python
    biodata = {
      'nama' : 'Muhammad Dawwam',
      'alamat': 'Telkom University Landmark Tower Lantai 11 no 08 (TULT 11.08)',
      'jurusan': 'Teknik Telekomunikasi',
      'umur': 78,
      'is_married': True,
      'tinggi_badan': 309.62,
      'laboratorium': ('Daskom','IMV')
      'murid': {
        'nama': 'Ridwan Maulana Tanjung',
        'alamat': 'Perumahan Bogor Ogah Geser Blok B1, No 7',
        'jurusan': 'Teknik Fisika',
        'is_married': False,
        'matkul_fav': ['Kalkulus', 'Pengolahan Sinyal', 'Elektromagnetika', 'Fisika Modern'],
      }
    }
    ```

  Mari kita bahas perbedaan antara set, list, dictionary, dan tuple berdasarkan beberapa aspek termasuk mutabilitas, pengindeksan, duplikasi, penggunaan memory, fleksibilitas, dan kasus penggunaan.

  - #### Mutabilitas
    - **Set**: _Mutable_, elemen-elemen dalam set dapat diubah setelah pembuatan.
    - **List**: _Mutable_, elemen-elemen dalam list dapat diubah, ditambahkan, atau dihapus.
    - **Dictionary**: _Mutable_, kunci dan nilai dalam dictionary dapat diubah.
    - **Tuple**: _Immutable_, elemen-elemen dalam tuple tidak dapat diubah setelah pembuatan.
  - #### Pengindeksan
    - **Set**: Tidak dapat diindeks karena elemennya tidak diurutkan.
    - **List**: Dapat diindeks, elemen-elemen dalam list diakses dengan indeks.
    - **Dictionary**: Tidak dapat diindeks menggunakan angka, tetapi menggunakan kunci.
    - **Tuple**: Dapat diindeks, elemen-elemen dalam tuple diakses dengan indeks.
  - #### Duplikasi
    - **Set**: Tidak mengizinkan elemen duplikat, hanya elemen unik yang diterima.
    - **List**: Dapat memiliki elemen duplikat, elemen dengan nilai yang sama dapat muncul lebih dari sekali.
    - **Dictionary**: Tidak mengizinkan kunci duplikat, tetapi nilai-nilai dapat duplikat.
    - **Tuple**: Dapat memiliki elemen duplikat, elemen dengan nilai yang sama dapat muncul lebih dari sekali.
  - #### Penggunaan Memori

    - **Set**: Menggunakan lebih banyak memory karena harus mempertahankan elemen-elemen unik dan melakukan operasi hash untuk memastikan keunikan.
    - **List**: Menggunakan lebih banyak memory daripada tuple karena memungkinkan elemen duplikat dan perlu menyimpan urutan elemen.
    - **Dictionary**: Menggunakan lebih banyak memory karena perlu menyimpan pasangan kunci-nilai dan melakukan operasi hash untuk mengakses nilai berdasarkan kunci.
    - **Tuple**: Menggunakan memory lebih sedikit dibandingkan list karena elemennya immutable.

  - #### Fleksibilitas

    - **Set**: Tidak terurut, tidak dapat diindeks, dan fokus pada operasi set seperti gabungan, irisan, dan perbedaan.
    - **List**: Terurut, dapat diindeks, dan lebih fleksibel untuk modifikasi, penambahan, penghapusan elemen.
    - **Dictionary**: Tidak terurut (di Python sebelum versi 3.7), memungkinkan penyimpanan data yang terstruktur menggunakan pasangan kunci-nilai.
    - **Tuple**: Terurut, dapat diindeks, dan lebih aman karena immutable.

  - #### Kasus Penggunaan
    - **Set**: Cocok untuk menyimpan elemen unik, melakukan operasi matematika seperti gabungan, irisan, atau perbedaan set.
    - **List**: Cocok untuk menyimpan dan mengelola kumpulan data yang dapat diubah-ubah, seperti daftar item atau log data.
    - **Dictionary**: Berguna untuk merepresentasikan data yang membutuhkan pasangan kunci-nilai, seperti konfigurasi, entitas terstruktur, atau data yang membutuhkan akses berdasarkan kunci.
    - **Tuple**: Digunakan ketika data harus tetap konstan, seperti kumpulan data yang relevan seperti nama, usia, dll., yang tidak boleh diubah.
