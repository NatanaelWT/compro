# Deskripsi Aplikasi

Aplikasi "Smart School" adalah sebuah platform berbasis Laravel yang dirancang untuk membantu institusi pendidikan dalam mengelola berbagai aspek operasional sekolah, termasuk manajemen siswa, guru, dan administrasi sekolah. Aplikasi ini akan mempermudah pengelolaan data, pengarsipan, dan interaksi antara stakeholder dalam lingkungan pendidikan.

## Fitur Utama

Aplikasi "Smart School" akan memiliki beberapa fitur utama, termasuk:

1. Manajemen Siswa: Mendaftarkan, mengupdate, dan mengarsipkan data siswa.
2. Manajemen Guru: Mengelola data guru, jadwal mengajar, dan informasi pribadi guru.
3. Manajemen Kelas: Membuat dan mengelola kelas, serta menghubungkannya dengan guru dan siswa.
4. Penilaian dan Raport: Mencatat penilaian siswa dan menghasilkan raport secara otomatis.
5. Manajemen Administrasi: Mengelola inventaris, dan administrasi sekolah lainnya.
6. Komunikasi: Memfasilitasi komunikasi antara siswa, guru, dan orang tua melalui pesan dan pemberitahuan.

## Integrasi AI Profiling (Python + Laravel)

1. Jalankan layanan FastAPI pada folder `ai_service` (lihat panduan lengkap di `ai_service/README.md`). Secara default berjalan di `http://127.0.0.1:8001`.
2. Pastikan variabel lingkungan `AI_PROFILING_SERVICE_URL` dan `AI_PROFILING_TIMEOUT` sudah diisi pada `.env`. Nilai default sudah disediakan pada `.env.example`.
3. Endpoint baru `GET /api/ai/profiling/{siswa}` (proteksi `auth:sanctum`) akan membaca nilai dan absensi siswa, memanggil layanan Python, kemudian mengembalikan rekomendasi AI berupa JSON.
4. Contoh pemanggilan:
    ```bash
    curl -H "Authorization: Bearer <SANCTUM_TOKEN>" \
         http://localhost/api/ai/profiling/123
    ```
    Ganti `123` dengan `id` siswa yang valid.
5. Dashboard siswa kini otomatis memanggil endpoint ini dan menampilkan ringkasan AI begitu halaman dibuka, jadi pastikan layanan FastAPI aktif saat user siswa login.

<br><br>

# LIST DEFAULT ACCOUNT

### **Admin/root access**
- **Username:** root
- **Password:** admin

### **Guru/teacher access**
- **Username:** guru
- **Password:** guru

### **Murid/student access**
- **Username:** siswa
- **Password:** siswa

## Kontribusi

Kami menyambut kontribusi dari siapa saja yang ingin berpartisipasi dalam pengembangan aplikasi "Smart School". Jika Anda ingin berkontribusi, silakan buat pull request dan kami akan meninjau kontribusi Anda.

Terima kasih telah berkontribusi pada proyek "Smart School"!
