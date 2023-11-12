# Control Structure

Struktur kontrol (control structure) dalam Python merujuk pada cara Anda mengendalikan aliran eksekusi program dengan menggunakan pernyataan dan blok kode tertentu. Struktur kontrol digunakan untuk mengatur urutan eksekusi pernyataan dalam sebuah program. Dalam Python, ada beberapa struktur kontrol utama, termasuk:

## Pernyataan Kondisional (Conditional Statements)

Pernyataan kondisional (conditional statements) adalah pernyataan yang digunakan untuk mengontrol aliran kode berdasarkan kondisi tertentu. Pernyataan kondisional pada Python terdiri dari dua bagian utama, yaitu:

- **Kondisi** adalah pernyataan yang digunakan untuk menentukan apakah blok kode akan dieksekusi atau tidak.
- **Blok kode** adalah kumpulan pernyataan yang akan dieksekusi jika kondisi bernilai benar.

Ada tiga jenis pernyataan kondisional pada Python, yaitu:

- **If statement**
  adalah pernyataan kondisional yang paling dasar. If statement akan mengeksekusi blok kode jika kondisi bernilai benar.

- **Elif statement**
  adalah pernyataan kondisional yang digunakan untuk menambahkan kondisi tambahan setelah if statement.

- **Else statement**
  adalah pernyataan kondisional yang digunakan untuk mengeksekusi blok kode jika kondisi dari if statement dan elif statement bernilai salah.

### _If_ statement

digunakan untuk mengeksekusi kode jika kondisi bernilai benar.

```python
a = 10

if a > 5:
  # block code ini akan tereksekusi karna a = 10 dan 10 lebih besar dari 5
  print("a lebih besar dari 5")

print("aku akan terseksekusi, apapun yg terjadi pada kondisi if diatas :)")
```

### _Else_ statement

statement digunakan untuk mengeksekusi kode jika kondisi bernilai salah.

```python
a = 10

if a > 5:
  # block code ini akan tereksekusi karna a = 10 dan 10 lebih besar dari 5
  print("a lebih besar dari 5")
else:
  # block code ini tidak akan tereksekusi karna a = 10 dan 10 tidak lebih besar dari 5
  print("a tidak lebih besar dari 5")
```

### _Elif_ statement

digunakan untuk mengeksekusi kode jika kondisi pertama bernilai salah dan kondisi kedua bernilai benar.

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

### Manfaat Pernyataan Kondisional

Pernyataan kondisional dapat digunakan untuk berbagai keperluan, antara lain:

- Untuk membuat kode yang lebih efisien
- Untuk membuat kode yang lebih fleksibel
- Untuk membuat kode yang lebih mudah dibaca

Berikut adalah beberapa manfaat pernyataan kondisional:

- Dapat membantu programmer untuk menghindari penulisan kode yang berulang-ulang
- Dapat membantu programmer untuk membuat kode yang dapat disesuaikan dengan berbagai kondisi
- Dapat membantu programmer untuk membuat kode yang lebih mudah dibaca dan dipahami

Pernyataan kondisional adalah salah satu fitur penting yang perlu dipahami oleh programmer Python. Pernyataan kondisional dapat digunakan untuk membuat kode Python lebih efisien, fleksibel, dan mudah dibaca.

## Pernyataan Perulangan (Loop Statements)

Pernyataan perulangan (loop statements) adalah pernyataan yang digunakan untuk mengeksekusi blok kode berulang kali selama kondisi tertentu terpenuhi. Pernyataan perulangan pada Python terdiri dari dua bagian utama, yaitu:

- **Kondisi**
  adalah pernyataan yang digunakan untuk menentukan apakah blok kode akan dieksekusi atau tidak.
- **Blok kode**
  adalah kumpulan pernyataan yang akan dieksekusi berulang kali.

Ada dua jenis pernyataan perulangan pada Python, yaitu:

- **While loop**
  adalah pernyataan perulangan yang akan mengeksekusi blok kode selama kondisi bernilai benar.
- **For loop**
  adalah pernyataan perulangan yang akan mengeksekusi blok kode untuk setiap elemen dalam kumpulan data.

### _For loop_

digunakan untuk mengulangi eksekusi kode hingga suatu kondisi terpenuhi.

```python
for i in range(10):
  print(f"aku perulangan ke-{i}")
```

### _While loop_

digunakan untuk mengulangi eksekusi kode selama suatu kondisi bernilai benar.

```python
a = 10
while a > 0:
  print(a)
  a -= 1
```

### Manfaat Pernyataan Perulangan

Pernyataan perulangan dapat digunakan untuk berbagai keperluan, antara lain:

- Untuk mengeksekusi kode berulang kali
- Untuk memproses kumpulan data
- Untuk membuat kode yang lebih efisien

Berikut adalah beberapa manfaat pernyataan perulangan:

- Dapat membantu programmer untuk menghindari penulisan kode yang berulang-ulang
- Dapat membantu programmer untuk memproses kumpulan data dengan lebih efisien
- Dapat membantu programmer untuk membuat kode yang lebih mudah dibaca dan dipahami

Pernyataan perulangan adalah salah satu fitur penting yang perlu dipahami oleh programmer Python. Pernyataan perulangan dapat digunakan untuk membuat kode Python lebih efisien, fleksibel, dan mudah dibaca.
