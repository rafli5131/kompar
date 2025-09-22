## Project: Ambil Data Cuaca Kecamatan di DIY (Multithread)

Buatlah sebuah program menggunakan multithraeding class untuk mendapatkan kondisi cuaca dari semua kecamatan di sebuah provinsi di indonesia. Setiap kelompok harus memilih provinsi yang berbeda-beda.

Kondisi cuaca yang perlu didapatkan adalah

    -Last Update (time)
    -Suhu dalam derajat celcius
    -Kelembapan
    -Kondisi cuaca (cerah, berawan, hujan, dll)
    -Kecepatan angin
    -Arah Angin
    -Sinar UV

Masukan dari program berupa daftar kecamatan dalam file excel. output dari program adalah data nomor 1 sampa dengan nomer 7 yang diletakkan dalam kolom setelah nama kecamatan di file excel yang sama.

### Kebutuhan
- Python 3
- Paket `requests`
- Paket `openpyxl`

### Instalasi Dependensi

```bash
pip install requests openpyxl
```

### Cara Menjalankan
1. Pastikan file `DIY.xlsx` sudah ada di folder ini dan berisi daftar kecamatan pada kolom pertama (A), mulai dari baris ke-2 (baris pertama untuk header).
2. Jalankan script dengan perintah:

```bash
python cuaca_multithread.py
```

3. Hasil akan disimpan pada file yang sama.
