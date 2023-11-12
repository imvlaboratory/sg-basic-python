# Tipe data

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
      'laboratorium': ('Daskom','IMV'),
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
