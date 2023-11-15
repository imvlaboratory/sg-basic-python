# Data Structure

Data structure atau struktur data dalam Python adalah cara penyusunan dan penyimpanan data agar dapat diakses dan dikelola dengan efisien. Ini melibatkan cara elemen-elemen data disusun, disimpan, dan diakses dalam suatu program. Python menyediakan berbagai tipe data dan struktur data bawaan seperti lists, tuples, sets, dictionaries, strings, queues, stacks, linked lists, dan lainnya. Beberapa dintaranya telah dibahas pada section Data Types.

Data structure memungkinkan pengorganisasian data dengan cara tertentu agar dapat diakses atau dimanipulasi sesuai kebutuhan aplikasi atau algoritma. Pemilihan data structure yang tepat penting untuk mencapai kinerja dan efisiensi yang optimal dalam penyelesaian suatu masalah atau tugas pemrograman. Struktur data yang baik dapat memudahkan pengembangan, pemeliharaan, dan pemahaman kode program.

Pada section ini akan dijelaskan bagaimana cara pengoperasian dan menipulasi tipe data kompleks yang ada pada python.

## Indexing dan Slicing

### Indexing

- **Definisi**
  Indexing merujuk pada proses mengakses elemen di dalam struktur data seperti list, tuple, atau string dengan menggunakan indeks.
- **Indeks Dimulai dari 0**

  Dalam Python, indeks dimulai dari 0. Artinya, elemen pertama memiliki indeks 0, elemen kedua memiliki indeks 1, dan seterusnya.

#### Contoh Indexing pada List

```python
my_list = [10, 20, 30, 40, 50]

print(my_list[0])  # Output: 10
print(my_list[2])  # Output: 30
print(my_list[-1])  # Output: 50 (indeks negatif mengakses elemen dari belakang)
```

#### Contoh Indexing pada String

```python
my_string = "Hello, World!"

print(my_string[0])  # Output: 'H'
print(my_string[7])  # Output: 'W'
```

### Slicing

- **Definisi**
  Slicing adalah proses mengambil sebagian dari struktur data dengan menyertakan batas awal dan batas akhir.

#### Contoh Slicing pada List

```python
my_list = [10, 20, 30, 40, 50]

print(my_list[1:4])  # Output: [20, 30, 40] (indeks 1 hingga 3, indeks 4 tidak termasuk)
print(my_list[:3])   # Output: [10, 20, 30] (indeks awal tidak ditentukan, dimulai dari awal)
print(my_list[2:])   # Output: [30, 40, 50] (indeks akhir tidak ditentukan, berakhir di akhir)
```

#### Contoh Slicing pada String

```python
my_string = "Hello, World!"

print(my_string[7:12])  # Output: 'World' (indeks 7 hingga 11)
print(my_string[:5])    # Output: 'Hello' (indeks awal tidak ditentukan, dimulai dari awal)
print(my_string[7:])    # Output: 'World!' (indeks akhir tidak ditentukan, berakhir di akhir)
```

### Contoh Slicing dengan Langkah pada List

Slicing juga dapat menggunakan langkah (step) untuk mengambil elemen dengan interval tertentu.

```python
my_list = [10, 20, 30, 40, 50, 60, 70, 80, 90]

print(my_list[1:8:2])  # Output: [20, 40, 60, 80] (indeks 1 hingga 7, langkah 2)
```

### Penting

- Saat melakukan indexing atau slicing, pastikan indeks yang digunakan berada dalam batas valid untuk menghindari IndexError.

- Slicing menghasilkan salinan dari struktur data baru, sehingga perubahan pada hasil slicing tidak mempengaruhi struktur data asli.

Indexing dan slicing adalah teknik dasar yang sangat penting dalam pemrograman Python, memungkinkan Anda untuk mengakses dan memanipulasi data secara efisien dalam berbagai jenis struktur data.

## List Comprehensions

List comprehensions adalah konstruksi sintaksis yang kuat dalam Python yang memungkinkan kita membuat list dengan kode yang lebih singkat dan ekspresif. Mereka memberikan cara ringkas untuk membuat list dengan memanfaatkan loop dan ekspresi kondisional.

### Sinstaksis Umum

```python
new_list = [expression for item in iterable if condition]
```

#### Komponen Utama

- **expression**: Ekspresi yang mendefinisikan nilai untuk setiap elemen dalam list.
- **item**: Variabel yang mewakili setiap elemen dalam iterable (misalnya, list, tuple, atau string).
- **iterable**: Struktur data yang dapat diiterasi (list, tuple, string, dll.).
- **condition (opsional)**: Kondisi opsional yang memfilter elemen yang akan dimasukkan ke dalam list.

#### Contoh List Comprehensions

1. **Membuat Angka Kuadrat**

```python
squares = [x**2 for x in range(5)]
# Output: [0, 1, 4, 9, 16]
```

2. **Membuat List Hanya Bilangan Ganjil**

```python
odd_numbers = [x for x in range(10) if x % 2 != 0]
# Output: [1, 3, 5, 7, 9]
```

3. **Membuat List yang Menggandakan Setiap Karakter dalam String**

```python
word = "hello"
doubled_characters = [char*2 for char in word]
# Output: ['hh', 'ee', 'll', 'll', 'oo']
```

4. **Membuat List yang Menggabungkan Elemen Dua List**

```python
list1 = [1, 2, 3]
list2 = ['a', 'b', 'c']
combined_list = [(x, y) for x in list1 for y in list2]
# Output: [(1, 'a'), (1, 'b'), (1, 'c'), (2, 'a'), (2, 'b'), (2, 'c'), (3, 'a'), (3, 'b'), (3, 'c')]
```

#### Keuntungan List Comprehensions

- **Kode Lebih Singkat**: Membuat list dengan sintaksis yang lebih singkat dan mudah dibaca.
- **Kode Lebih Cepat**: Dapat lebih efisien daripada menggunakan loop tradisional untuk membuat list.
- **Ekspresif**: Menyederhanakan logika pembuatan list.

### Penting

- Gunakan list comprehensions dengan bijak agar kode tetap mudah dibaca.
- Jangan terlalu kompleks untuk menjaga kejelasan.

List comprehensions adalah alat yang sangat berguna untuk membuat list dengan cara yang ringkas dan ekspresif, mengurangi jumlah kode yang diperlukan untuk membuat list secara manual.
