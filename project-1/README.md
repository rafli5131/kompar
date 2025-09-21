## Project: Ambil Data Cuaca Kecamatan di Jawa Tengah (Multithread)

Script ini digunakan untuk mengambil data cuaca terkini dari API weatherapi.com untuk setiap kecamatan di Jawa Tengah yang terdapat pada file Excel, lalu menyimpan hasilnya ke file Excel baru. Proses pengambilan data dilakukan secara multithread agar lebih cepat.

### Kebutuhan
- Python 3.x
- Paket `requests`
- Paket `openpyxl`

### Instalasi Dependensi
Jalankan perintah berikut di terminal (direktori project):

```bash
pip install requests openpyxl
```

### Cara Menjalankan
1. Pastikan file `kecamatan_jateng.xlsx` sudah ada di folder ini dan berisi daftar kecamatan pada kolom pertama (A), mulai dari baris ke-2 (baris pertama untuk header).
2. Jalankan script dengan perintah:

```bash
python cuaca_multithread.py
```

3. Hasil akan disimpan pada file `cuaca_hasil.xlsx` di folder yang sama.

### Penjelasan File
- `cuaca_multithread.py` : Script utama untuk mengambil data cuaca.
- `kecamatan_jateng.xlsx` : Daftar kecamatan (input).
- `cuaca_hasil.xlsx` : Hasil data cuaca (output).

### Catatan
- Script ini menggunakan API key gratis dari weatherapi.com. Jika limit tercapai, Anda bisa mengganti API key pada script.
- Jika ada kecamatan yang gagal diambil datanya, akan tertulis "ERROR" pada hasil.