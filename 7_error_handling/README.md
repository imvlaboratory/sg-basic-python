# Error Handling

Error handling atau penanganan kesalahan adalah suatu teknik dalam pemrograman yang digunakan untuk mengatasi potensi kesalahan yang mungkin terjadi selama eksekusi program. Dalam Python, penanganan kesalahan dilakukan menggunakan blok `try`, `except`, `else`, dan `finally`.

## Try dan Except

- Try Block

  Blok `try` digunakan untuk menempatkan kode yang mungkin menyebabkan error.

- Except Block

  Blok `except` digunakan untuk menangkap dan menangani error yang muncul di dalam blok `try`.

```python
try:
    # Kode yang mungkin menyebabkan error
    result = 10 / 0
except ZeroDivisionError:
    # Menangani error jika terjadi ZeroDivisionError
    print("Tidak bisa membagi dengan nol.")
```

## Else

- Else

  Blok `else` dapat digunakan setelah blok except untuk mengeksekusi kode jika tidak ada error yang terjadi di dalam blok `try`.

```python
try:
    result = 10 / 2
except ZeroDivisionError:
    print("Tidak bisa membagi dengan nol.")
else:
    print("Hasil:", result)
```

## Finally

- Finally

  Blok `finally` dapat digunakan untuk menempatkan kode yang harus dijalankan, baik terjadi error atau tidak. Blok ini akan dijalankan selalu, bahkan jika ada atau tidak ada error.

  ```python
  try:
    result = 10 / 2
  except ZeroDivisionError:
    print("Tidak bisa membagi dengan nol.")
  else:
    print("Hasil:", result)
  finally:
    print("Eksekusi blok finally.")
  ```

## Menangkap Beberapa Jenis Error

- Anda dapat menangani beberapa jenis error dengan menambahkan beberapa blok except.

```python
try:
    result = 10 / 'a'
except ZeroDivisionError:
    print("Tidak bisa membagi dengan nol.")
except TypeError:
    print("Tipe data tidak sesuai.")
```

## Penggunaan `as` untuk Informasi Error

- Anda dapat menggunakan `as` untuk memberikan nama pada variabel yang menyimpan informasi error.

```python
try:
    result = 10 / 'a'
except (ZeroDivisionError, TypeError) as err:
    print(f"Terjadi kesalahan: {err}")
```

## Raise

- Blok `raise` digunakan untuk memicu error secara manual. Anda dapat memasukkan tipe error atau membuat error khusus

```python
try:
    raise ValueError("Ini adalah error custom.")
except ValueError as err:
    print(f"Terjadi kesalahan: {err}")
```

Dengan konsep-konsep di atas, Anda dapat membuat program Python yang lebih tahan kesalahan dan memberikan pesan yang jelas saat terjadi kesalahan. Ini membantu dalam pemeliharaan dan debugging kode
