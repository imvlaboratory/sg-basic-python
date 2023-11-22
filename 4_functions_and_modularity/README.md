# Functions and Modularity

Dalam Python, fungsi adalah blok kode yang dapat dipanggil untuk menjalankan tugas tertentu, membantu mengorganisir logika program menjadi unit yang dapat digunakan kembali. Fungsi menerima input, melakukan operasi, dan mengembalikan output. Sementara itu, modularitas merujuk pada praktik membagi program menjadi modul-modul terpisah. Modul adalah file Python yang berisi definisi variabel, fungsi, dan kelas. Dengan fungsi, kita dapat mengelompokkan kode dengan logika serupa, sementara modularitas memungkinkan pemisahan program ke dalam bagian yang lebih kecil, meningkatkan kejelasan, pemeliharaan, dan penggunaan kembali kode. Kombinasi fungsi dan modularitas memperkuat struktur dan pemahaman program, memfasilitasi pengembangan dan pemeliharaan yang lebih efisien.

## Higher Order Functions

Dalam Python, fungsi adalah blok kode yang dapat dipanggil secara berulang untuk melakukan tugas tertentu. Mereka membantu mengorganisir kode ke dalam unit-unit kecil yang dapat digunakan kembali. Fungsi biasanya menerima input (parameter), melakukan operasi tertentu, dan mengembalikan output.

Contoh fungsi sederhana:

```python
def greet():
    """Fungsi sapaan sederhana."""
    print(f"Hello, World!")

# Memanggil fungsi
greet()
```

### Parameter dan Return Values

Fungsi dapat menerima parameter sebagai input untuk melakukan operasi tertentu. Return statement digunakan untuk mengembalikan nilai dari fungsi. Sebuah fungsi dapat memiliki atau tidak memiliki parameter, dan dapat atau tidak mengembalikan nilai.

Contoh fungsi dengan parameter dan return values:

```python
def add(x, y):
    """Fungsi penjumlahan."""
    result = x + y
    return result

# Memanggil fungsi dan menyimpan hasilnya
sum_result = add(5, 3)
print("Hasil penjumlahan:", sum_result)
```

### Function Scope

Function scope mengacu pada cakupan (lingkup) variabel yang didefinisikan dalam fungsi. Variabel yang didefinisikan dalam fungsi hanya dapat diakses di dalam fungsi tersebut, kecuali jika dideklarasikan sebagai variabel global.

```python
def multiply(x, y):
    """Fungsi perkalian."""
    result = x * y
    return result

# Function scope di luar fungsi tidak dapat mengakses variabel 'result'
print(result) # ERROR! result hanya berlaku dalam fungsi 'multiply'
```

### Lambda Functions

Fungsi lambda, yang juga dikenal sebagai fungsi anonim, adalah cara untuk membuat fungsi kecil tanpa perlu memberikannya nama. Fungsi ini didefinisikan menggunakan kata kunci lambda diikuti oleh parameter-parameter dan ekspresi yang harus dievaluasi. Lambda biasanya digunakan untuk membuat fungsi sederhana untuk keperluan yang sementara atau dalam situasi di mana fungsi kecil diperlukan

#### Berikut adalah sintaks dari fungsi lambda:

```python
lambda arguments: expression
```

- **arguments**: Parameter atau argumen yang diperlukan oleh fungsi.
- **expression**: Ekspresi yang akan dievaluasi dan mengembalikan hasil.

#### Contoh penggunaan fungsi lambda:

```python
# Contoh 1: Fungsi lambda dengan satu parameter
square = lambda x: x**2
print(square(5))  # Output: 25

# Contoh 2: Fungsi lambda dengan dua parameter
multiply = lambda x, y: x * y
print(multiply(3, 4))  # Output: 12

# Contoh 3: Fungsi lambda dalam ekspresi yang lebih kompleks
addition = lambda a, b, c: a + b + c
print(addition(1, 2, 3))  # Output: 6
```

Fungsi lambda sering digunakan bersama dengan fungsi-fungsi tingkat tinggi seperti `map()`, `filter()`, dan `sorted()`. Berikut adalah contoh penggunaan lambda dengan fungsi-fungsi tersebut:

```python
# Contoh menggunakan map() dengan lambda
numbers = [1, 2, 3, 4, 5]
squared_numbers = list(map(lambda x: x**2, numbers))
print(squared_numbers)  # Output: [1, 4, 9, 16, 25]

# Contoh menggunakan filter() dengan lambda
even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
print(even_numbers)  # Output: [2, 4]

# Contoh menggunakan sorted() dengan lambda untuk mengurutkan berdasarkan panjang kata
words = ['apple', 'banana', 'kiwi', 'orange']
sorted_words = sorted(words, key=lambda x: len(x))
print(sorted_words)  # Output: ['kiwi', 'apple', 'banana', 'orange']
```

Meskipun fungsi lambda memberikan kemampuan untuk membuat fungsi secara ringkas, tetapi dalam beberapa kasus, fungsi yang didefinisikan dengan def dapat lebih mudah dibaca dan lebih deskriptif. Fungsi lambda umumnya digunakan untuk kasus-kasus sederhana di mana membuat fungsi terpisah mungkin terlalu berlebihan.

## Modularity

Modularity atau Modularitas adalah konsep dalam pemrograman yang merujuk pada pemisahan program ke dalam bagian-bagian yang lebih kecil yang disebut modul. Modul adalah file Python yang berisi definisi variabel, fungsi, dan kelas yang dapat digunakan oleh program lain. Prinsip modularitas memberikan keuntungan dalam pemeliharaan, pengembangan, dan kejelasan kode.

### Keuntungan Modularitas

- **Pemisahan Tugas**

  Program yang besar dan kompleks dapat dibagi menjadi modul-modul kecil, memudahkan pengelolaan dan pemeliharaan.

- **Penggunaan Kembali Kode**

  Modul dapat digunakan kembali dalam berbagai proyek. Sebuah fungsi atau kelas yang didefinisikan dalam satu modul dapat diimpor dan digunakan di modul lain atau proyek lain.

- **Kejelasan Kode**

  Pembagian program ke dalam modul-modul membuat kode menjadi lebih terstruktur dan mudah dipahami. Setiap modul dapat fokus pada satu tugas atau fitur tertentu.

- **Isolasi Logika**

  Modul memberikan isolasi logika, di mana perubahan dalam satu modul tidak memengaruhi bagian lain dari program, asalkan antarmuka modul tetap konsisten.

### Cara Menggunakan Modularitas dalam Python

1. **Membuat Module**

   - Definisikan variabel, fungsi, dan kelas di dalam suatu file Python.
   - Simpan file tersebut dengan ekstensi `.py`, misalnya `my_module.py`.

   ```python
   # Contoh: my_module.py

   def greet(name):
       """Fungsi sapaan."""
       print(f"Hello, {name}!")

    def exponential(x,y)
        """fungsi perpangkatan"""
        hasil = x**y
        return hasil

   ```

2. **Mengimpor Module**

   - Gunakan pernyataan import untuk mengimpor module ke dalam program utama.

   ```python
   # Contoh penggunaan module di program utama

   import my_module
   ```

3. **Pemanggilan Fungsi atau Variabel dari Module**

   - Setelah mengimpor modulD, panggil fungsi atau variabelnya menggunakan sintaks `nama_module.nama_fungsi`.

   ```python
   # Contoh penggunaan fungsi dari modul

   import my_module

   hasil = my_module.exponential(2,4)
   print(hasil)
   ```

### Catatan Penting:

- Pastikan file modul berada di direktori yang sama dengan program utama atau dalam path pencarian Python.
- Jangan lupa untuk menyertakan dokumen/docstring yang menjelaskan fungsi atau kelas yang didefinisikan di dalam module.

Dengan menggunakan modularitas, programmer dapat mengelola kompleksitas, meningkatkan pemahaman terhadap kode, dan memfasilitasi pengembangan tim. Modularitas merupakan salah satu prinsip penting dalam pemrograman yang mendukung pemeliharaan dan pengembangan yang efisien.
