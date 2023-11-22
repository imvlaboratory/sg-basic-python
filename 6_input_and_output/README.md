# Input/Output (I/O)

I/O pada Python merujuk pada proses masukan dan keluaran dalam program. Ini melibatkan interaksi antara program dan lingkungannya, baik itu dengan berkomunikasi dengan pengguna melalui terminal atau mengakses file untuk membaca atau menulis data.

## Standar Input dan Output

### Standar Input

- `input()` digunakan untuk membaca input dari pengguna.
- Mengembalikan string yang diinput oleh pengguna.

### Standar Output

- `print()` digunakan untuk menampilkan output ke layar.
- Dapat mencetak nilai variabel atau teks.

#### Contoh

```python
name = input("Masukkan nama Anda: ")
print("Hello, " + name + "!")
```

#### Contoh untuk tipe data lain, selain string

```python
# parse input ke tipe data string
umur = int(input("Masukan umur anda"))
print(f'umur anda adalah {umur}')
# parse input ke tipe data
tinggi = float(input("Masukan tinggi badan anda: "))
print(f'tinggi badan anda adalah {tinggi} cm')
```

## Membaca dan menulis file

### Membaca file

- Fungsi `open()` digunakan untuk membuka file. Dapat menerima dua argumen: nama file dan mode (`r` untuk membaca, `w` untuk menulis, `a` untuk menambahkan, dan sebagainya).
- Metode `read()` digunakan untuk membaca isi file

#### Contoh

```python
with open('file.txt', 'r') as file:
    content = file.read()
    print(content)
```

### Menulis file

- Jika file belum ada, fungsi `open()` dengan mode `w` akan membuat file baru. Jika sudah ada, akan menghapus kontennya dan menulis yang baru.
- Metode `write()` digunakan untuk menulis ke file.

#### Contoh

```python
with open('file.txt', 'w') as file:
    file.write("Ini adalah contoh tulisan ke file.")
```

### Iterasi baris dalam File

- Anda dapat menggunakan perulangan untuk membaca setiap baris dalam file.

#### Contoh

```python
with open('file.txt', 'r') as file:
    for line in file:
        print(line)
```

### Membaca, menulis, dan memanipulasi file data menggunakan Pandas

Pandas adalah salah satu pustaka Python yang sangat populer untuk analisis data, dan menyediakan fungsi untuk membaca dan menulis data dari dan ke berbagai format file, termasuk CSV (Comma-Separated Values). Berikut adalah cara membaca dan menulis file dari dan ke DataFrame Pandas ke file CSV:

### Membaca file ke DataFrame

```python
import pandas as pd

# Membaca file CSV ke DataFrame
df = pd.read_csv('nama_file.csv')

# Menampilkan beberapa baris pertama dari DataFrame
print(df.head())
```

Pada contoh di atas, `pd.read_csv('nama_file.csv')` digunakan untuk membaca data dari file CSV ke dalam sebuah DataFrame. Fungsi `head() `kemudian digunakan untuk menampilkan beberapa baris pertama dari DataFrame tersebut.

### Menulis DataFrame ke File

```python
import pandas as pd

# Membuat DataFrame contoh
data = {'Nama': ['John', 'Alice', 'Bob'],
        'Usia': [28, 24, 22],
        'Kota': ['Jakarta', 'New York', 'London']}

df = pd.DataFrame(data)

# Menulis DataFrame ke file CSV
df.to_csv('output_file.csv', index=False)
```

Pada contoh ini,` pd.DataFrame(data)` digunakan untuk membuat DataFrame dari data yang diberikan. Kemudian, `df.to_csv('output_file.csv', index=False) `digunakan untuk menulis DataFrame ke dalam file CSV baru dengan nama `output_file.csv`. Argumen `index=False` menunjukkan bahwa kita tidak ingin menyimpan indeks baris dalam file CSV.

Dengan menggunakan Pandas, Anda dapat dengan mudah membaca dan menulis data dari dan ke file CSV, serta berbagai format file lainnya. Ini sangat berguna ketika Anda bekerja dengan dataset dalam bentuk DataFrame dan ingin menyimpannya atau memuatnya dari file CSV untuk analisis lebih lanjut.
