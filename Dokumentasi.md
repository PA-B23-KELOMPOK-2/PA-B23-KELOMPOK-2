### Deskipsi program 
Tujuan:
- Menyediakan sistem informasi terintegrasi dan mudah diakses tentang perkotaan dan pemukiman di Indonesia.
- Membantu para pemangku kepentingan dalam membuat kebijakan yang tepat dan efektif untuk pembangunan perkotaan dan pemukiman yang berkelanjutan.
  
Masukan:
- Data tentang perkotaan dan pemukiman dari berbagai :
   - Kementerian Pekerjaan Umum dan Perumahan Rakyat (PUPR) 
   - Kementerian Agraria dan Tata Ruang/Badan Pertanahan Nasional
   - Kementerian Sosial
   - Kementerian Keuangan (Kemenkeu)
     
Keluaran:
- Alat dan platform untuk mendukung pengambilan keputusan terkait pembangunan perkotaan dan pemukiman yang berkelanjutan.
  
Algoritma:
- Sistem SIP2B akan menggunakan berbagai algoritma dan teknik data science untuk mengolah dan menganalisis data tentang perkotaan dan pemukiman.
- Algoritma ini akan digunakan untuk menghasilkan laporan, peta, dan visualisasi data yang dapat membantu para pemangku kepentingan dalam memahami kondisi perkotaan dan pemukiman di Indonesia.
  
Batasan:
- Sistem SIP2B masih dalam tahap pengembangan, dan data yang tersedia mungkin belum lengkap atau akurat.
- Sistem ini mungkin tidak dapat menjawab semua pertanyaan tentang perkotaan dan pemukiman di Indonesia.
  
Manfaat:
- Sistem SIP2B dapat membantu para pemangku kepentingan dalam:
  - Memahami kondisi perkotaan dan pemukiman di Indonesia.
  - Mengidentifikasi masalah dan tantangan yang dihadapi perkotaan dan pemukiman di Indonesia.
  - Mengembangkan kebijakan dan program yang tepat dan efektif untuk pembangunan perkotaan dan pemukiman yang berkelanjutan.
  - Memantau dan mengevaluasi kemajuan pembangunan perkotaan dan pemukiman yang berkelanjutan.

Sistem Informasi Perkotaan dan Pemukiman Berkelanjutan (SIP2B) dengan menganut konsep kota komunitas berkelanjutan telah menjadi solusi yang inovatif untuk menghadapi permasalahan kota modern sekarang. SIP2B dirancang untuk mengatasi tantangan-tantangan tersebut dengan menyediakan sistem informasi yang terintegrasi dan mudah diakses tentang perkotaan dan pemukiman di Indonesia. SIP2B diharapkan dapat membantu para pemangku kepentingan dalam membuat kebijakan yang tepat dan efektif untuk pembangunan perkotaan dan pemukiman yang berkelanjutan.

## struktur project

- Database Connection Module: Berisi kode untuk menghubungkan ke database MySQL.
- Data Structures Module: Berisi definisi dari kelas Node dan LinkedList untuk representasi linked list serta fungsi sorting dan searching.
- Display Module: Berisi metode-metode untuk menampilkan data ke dalam tabel menggunakan PrettyTable.
- Main Program Module: Berisi logika utama program, termasuk interaksi dengan pengguna dan penggunaan modul-modul sebelumnya.
- models/: Modul yang berisi definisi model-model data yang digunakan dalam program.
  - admin.py: File yang berisi definisi model untuk data admin.
  - perkotaan.py: File yang berisi definisi model untuk data perkotaan.
  - pemukiman.py: File yang berisi definisi model untuk data pemukiman.
  - proyek.py: File yang berisi definisi model untuk data proyek.
- Direktori admin: Mengelola operasi-admin terkait pengelolaan data admin.
  - admin.py: Berisi fungsi-fungsi yang terkait dengan admin.
  - admin_utils.py: Berisi utilitas yang dapat digunakan dalam modul admin.
- Direktori perkotaan: Mengelola operasi terkait dengan data perkotaan.
  - perkotaan.py: Berisi fungsi-fungsi yang terkait dengan data perkotaan.
  - perkotaan_utils.py: Berisi utilitas yang dapat digunakan dalam modul perkotaan.
- Direktori pemukiman: Mengelola operasi terkait dengan data pemukiman.
  - pemukiman.py: Berisi fungsi-fungsi yang terkait dengan data pemukiman.
  - pemukiman_utils.py: Berisi utilitas yang dapat digunakan dalam modul pemukiman.
- Direktori proyek: Mengelola operasi terkait dengan data proyek.
  - proyek.py: Berisi fungsi-fungsi yang terkait dengan data proyek.
  - proyek_utils.py: Berisi utilitas yang dapat digunakan dalam modul proyek.
- Direktori utils: Berisi utilitas yang digunakan secara umum.
  - database.py: Berisi fungsi-fungsi untuk berinteraksi dengan database.
  - input_validation.py: Berisi fungsi-fungsi untuk memvalidasi input pengguna.
- Direktori authentication: Ini adalah direktori yang mengelola proses otentikasi pengguna.
  - login.py: Berisi kelas Login dan metode-metodenya untuk registrasi dan login pengguna.
- Direktori database: Ini adalah direktori yang mengelola koneksi dan operasi terkait database.
  - database_utils.py: Berisi fungsi-fungsi untuk berinteraksi dengan database, seperti menjalankan kueri dan mengambil data.

## fitur 

Beberapa library yang digunakan seperti : 

- import mysql.connector: Baris ini mengimpor modul mysql.connector, yang menyediakan fungsi untuk terhubung dan berinteraksi dengan database MySQL di Python.
- from mysql.connector import Error: Ini mengimpor kelas Error secara khusus dari modul mysql.connector. Kelas ini kemungkinan digunakan untuk menangani kesalahan yang mungkin terjadi selama operasi database.
- import prettytable: Baris ini mengimpor modul prettytable, yang menawarkan alat untuk membuat tabel menarik secara visual untuk menampilkan data. Biasanya -digunakan untuk menampilkan hasil query database dalam format yang jelas dan teratur.
- import getpass: Baris ini mengimpor modul getpass, yang menyediakan cara aman untuk meminta kata sandi pengguna tanpa menampilkannya di konsol. Ini sering digunakan saat terhubung ke database yang membutuhkan autentikasi.

Beberapa fitur yang terdapat dalam program :

1. login
   - login = User yang telah memiliki akun dapat melakukan login dengan memasukan userame dan password
   - Membuat Akun Baru = User yang belum memiliki akun dapat membuat akun dengan membuat username dan password
   - Keluar = Ketika user memilih menu keluar maka program akan terhenti

2. user
   - Database Perkotaan : User dapat memlihat database perkotaan dan memilih beberapa menu seperti :
     - Tampilkan Data (urutkan berdasarkan ID - A-Z) : User dapat melihat tampilan data Perkotaan berdasarkan id yang diurutkan secara terurut atau ascending 
     - Tampilkan Data (urutkan berdasarkan ID - Z-A) : User dapat melihat tampilan data Perkotaan berdasarkan id yang diurutkan secara terbalik atau ascending
     - Cari Data (berdasarkan ID) : User dapat mencari data Perkotaan dengan memasukan id Perkotaan
     - Kembali ke Menu Utama : User dapat kembali ke menu utama
      
   - Database Pemukiman : : User dapat memlihat database perkotaan dan memilih beberapa menu seperti :
     - Tampilkan Data (urutkan berdasarkan ID - A-Z) : User dapat melihat tampilan data Pemukiman berdasarkan id yang diurutkan secara terurut atau ascending 
     - Tampilkan Data (urutkan berdasarkan ID - Z-A) : User dapat melihat tampilan data Pemukiman berdasarkan id yang diurutkan secara terbalik atau ascending
     - Cari Data (berdasarkan ID) : User dapat mencari data Pemukiman dengan memasukan id Pemukiman
     - Kembali ke Menu Utama : User dapat kembali ke menu utama
   
   - Database Proyek: User dapat memlihat database proyek dan memilih beberapa menu seperti :
     - Tampilkan Data (urutkan berdasarkan ID - A-Z) : User dapat melihat tampilan data Proyek berdasarkan id yang diurutkan secara terurut atau ascending 
     - Tampilkan Data (urutkan berdasarkan ID - Z-A) : User dapat melihat tampilan data Proyek berdasarkan id yang diurutkan secara terbalik atau ascending
     - Cari Data (berdasarkan ID) : User dapat mencari data Proyek dengan memasukan id Proyek 
     - Kembali ke Menu Utama : User dapat kembali ke menu utama

3. Super Admin
   - Database Admin : Super admin dapat mengelola database Admin, memmilih beberapa menu dan melakukan crud untuk
     - Tambah Data Admin : Super admin dapat menambahkan admin baru dengan memasukan nama admin, email admin, password admin dan role admin 
     - Hapus Data Admin : Super Admin dapat menghapus admin dengan memasukan id dari admin yang ingin dihapus
     - Perbaharui Data Admin : Super Admin dapat memperbaharui data admin dengan memilih admin ber dasarkan id kemudian memasukan nama admin baru, email admin    
       baru, password admin baru dan role admin baru 
     - Tampilkan Data Admin : Super admin dapat melihat isi dari tampilan database Admin
     - Keluar : Super Admin dapat kembali ke menu sebelumnya

   - Database Perkotaan : Super admin dapat mengelola database perkotaan, memilih beberapa menu dan melakukan crud untuk
     - Tambah Data Perkotaan : Super admin dapat menambahkan perkotaan baru dengan memasukan nama kota, provinsi, jumlah penduduk, luas wilayah, indeks 
       keberlanjutan dan id admin
     - Hapus Data Perkotaan : Super Admin dapat menghapus perkotaan dengan memasukan id dari perkotaan yang ingin dihapus 
     - Perbaharui Data Perkotaan : Super Admin dapat memperbaharui data perkotaan dengan memilih perkotaan berdasarkan id kemudian memasukan id perkotaan baru, 
       nama kota baru, provinsi baru, jumlah penduduk baru, luas wilayah baru, indeks keberlanjutan baru dan id admin baru
     - Tampilkan Data Perkotaan : Super admin dapat memlihat database perkotaan dan memilih beberapa menu seperti :
       - Tampilkan Data (urutkan berdasarkan ID - A-Z) : Super admin dapat melihat tampilan data Perkotaan berdasarkan id yang diurutkan secara terurut atau 
         ascending 
       - Tampilkan Data (urutkan berdasarkan ID - Z-A) :  Super admin dapat melihat tampilan data Perkotaan berdasarkan id yang diurutkan secara terbalik atau 
         ascending
       - Cari Data (berdasarkan ID) : Super admin dapat mencari data Perkotaan dengan memasukan id Pemukiman
       - Kembali ke Menu Utama : Super admin dapat kembali ke menu utama
     - Keluar : Super admin dapar kembali ke menu sebelumnya

   - Database Pemukiman : Super admin dapat mengelola database pemukiman, memilih beberapa menu dan melakukan crud untuk
     - Tambah Data Pemukiman : Super admin dapat menambahkan Pemukiman baru dengan memasukan nama pemukiman, id perkotaan, Jenis pemukiman, akses air bersih, 
       akses sanitasi layak, id admin 
       keberlanjutan dan id admin
     - Hapus Data Pemukiman : Super Admin dapat menghapus Pemukiman dengan memasukan id dari Pemukiman yang ingin dihapus 
     - Perbaharui Data Pemukiman : Super Admin dapat memperbaharui data Pemukiman dengan memilih Pemukiman berdasarkan id kemudian memasukan id pemukiman baru, 
       nama pemukiman baru, id perkotaan baru, Jenis pemukiman baru, akses air bersih baru, akses sanitasi layak baru, id admin baru
       akses sanitasi layak, id admin 
       perkotaan baru, Jenis pemukiman baru, akses air bersih baru, akses sanitasi layak baru, id admin baru
     - Tampilkan Data Pemukiman : Super admin dapat memlihat database Pemukiman dan memilih beberapa menu seperti :
       - Tampilkan Data (urutkan berdasarkan ID - A-Z) : Super admin dapat melihat tampilan data Pemukiman berdasarkan id yang diurutkan secara terurut atau 
         ascending 
       - Tampilkan Data (urutkan berdasarkan ID - Z-A) :  Super admin dapat melihat tampilan data Pemukiman berdasarkan id yang diurutkan secara terbalik atau 
         ascending
       - Cari Data (berdasarkan ID) : Super admin dapat mencari data Pemukiman dengan memasukan id Pemukiman
       - Kembali ke Menu Utama : Super admin dapat kembali ke menu utama
     - Keluar : Super admin dapat kembali ke menu sebelumnya
     
   - Database Proyek : Super admin dapat mengelola database Proyek, memilih beberapa menu dan melakukan crud untuk
     - Tambah Data Proyek : Super admin dapat menambahkan Pemukiman baru dengan memasukan nama proyek, id pemukiman, deskripsi proyek, jenis proyek, 
       dana proyek, status proyek, id admin 
     - Hapus Data Proyek : Super Admin dapat menghapus Pemukiman dengan memasukan id dari Pemukiman yang ingin dihapus 
     - Perbaharui Data Proyek : Super Admin dapat memperbaharui data Pemukiman dengan memilih Pemukiman berdasarkan id kemudian memasukan id proyek baru, nama 
       proyek baru, id pemukiman baru, deskripsi proyek baru, jenis proyek baru, dana proyek baru, status proyek baru, id admin baru
     - Tampilkan Data Proyek : Super admin dapat memlihat database Pemukiman dan memilih beberapa menu seperti :
       - Tampilkan Data (urutkan berdasarkan ID - A-Z) : Super admin dapat melihat tampilan data Proyek berdasarkan id yang diurutkan secara terurut atau 
         ascending 
       - Tampilkan Data (urutkan berdasarkan ID - Z-A) :  Super admin dapat melihat tampilan data Proyek berdasarkan id yang diurutkan secara terbalik atau 
         ascending
       - Cari Data (berdasarkan ID) : Super admin dapat mencari data Proyek dengan memasukan id Proyek
       - Kembali ke Menu Utama : Super admin dapat kembali ke menu utama
     - Keluar : Super admin dapat kembali ke menu sebelumnya
    
4. Admin Perkotaan : Admin Perkotaan hanya dapat mengelola database perkotaan, memilih beberapa menu dan melakukan crud untuk
    - Tambah Data Perkotaan : Admin Perkotaan dapat menambahkan perkotaan baru dengan memasukan nama kota, provinsi, jumlah penduduk, luas wilayah, indeks 
      keberlanjutan dan id admin
    - Hapus Data Perkotaan : Admin Perkotaan dapat menghapus perkotaan dengan memasukan id dari perkotaan yang ingin dihapus 
    - Perbaharui Data Perkotaan : Admin Perkotaan dapat memperbaharui data perkotaan dengan memilih perkotaan berdasarkan id kemudian memasukan id perkotaan 
      baru, nama kota baru, provinsi baru, jumlah penduduk baru, luas wilayah baru, indeks keberlanjutan baru dan id admin baru
    - Tampilkan Data Perkotaan : Admin Perkotaan dapat memlihat database perkotaan dan memilih beberapa menu seperti :
      - Tampilkan Data (urutkan berdasarkan ID - A-Z) : Admin Perkotaan dapat melihat tampilan data Perkotaan berdasarkan id yang diurutkan secara terurut atau 
         ascending 
      - Tampilkan Data (urutkan berdasarkan ID - Z-A) :  Admin Perkotaan dapat melihat tampilan data Perkotaan berdasarkan id yang diurutkan secara terbalik atau 
         ascending
      - Cari Data (berdasarkan ID) : Admin Perkotaan dapat mencari data Perkotaan dengan memasukan id Pemukiman
      - Kembali ke Menu Utama : Admin Perkotaan dapat kembali ke menu utama
    - Keluar : Admin Perkotaan dapar kembali ke menu sebelumnya

5. Admin Pemukiman : Admin Pemukiman hanya dapat mengelola database Proyek, memilih beberapa menu dan melakukan crud untuk
    - Tambah Data Proyek : Admin Pemukiman dapat menambahkan Pemukiman baru dengan memasukan nama proyek, id pemukiman, deskripsi proyek, jenis proyek, 
      dana proyek, status proyek, id admin 
    - Hapus Data Proyek : Admin Pemukiman dapat menghapus Pemukiman dengan memasukan id dari Pemukiman yang ingin dihapus 
    - Perbaharui Data Proyek : Admin Pemukiman dapat memperbaharui data Pemukiman dengan memilih Pemukiman berdasarkan id kemudian memasukan id proyek baru, nama 
      proyek baru, id pemukiman baru, deskripsi proyek baru, jenis proyek baru, dana proyek baru, status proyek baru, id admin baru
    - Tampilkan Data Proyek : Admin Pemukiman dapat memlihat database Pemukiman dan memilih beberapa menu seperti :
      - Tampilkan Data (urutkan berdasarkan ID - A-Z) : Admin Pemukiman dapat melihat tampilan data Proyek berdasarkan id yang diurutkan secara terurut atau 
        ascending 
      - Tampilkan Data (urutkan berdasarkan ID - Z-A) : Admin Pemukiman dapat melihat tampilan data Proyek berdasarkan id yang diurutkan secara terbalik atau 
        ascending
      - Cari Data (berdasarkan ID) : Admin Pemukiman dapat mencari data Proyek dengan memasukan id Proyek
      - Kembali ke Menu Utama : Admin Pemukiman dapat kembali ke menu utama
    - Keluar : Admin Pemukiman dapat kembali ke menu sebelumnya

7. Admin Proyek : Admin Proyek dapat mengelola database Proyek, memilih beberapa menu dan melakukan crud untuk
    - Tambah Data Proyek :Admin Proyek dapat menambahkan Pemukiman baru dengan memasukan nama proyek, id pemukiman, deskripsi proyek, jenis proyek, 
      dana proyek, status proyek, id admin 
    - Hapus Data Proyek : Admin Proyek dapat menghapus Pemukiman dengan memasukan id dari Pemukiman yang ingin dihapus 
    - Perbaharui Data Proyek : Admin Proyek dapat memperbaharui data Pemukiman dengan memilih Pemukiman berdasarkan id kemudian memasukan id proyek baru, nama 
      proyek baru, id pemukiman baru, deskripsi proyek baru, jenis proyek baru, dana proyek baru, status proyek baru, id admin baru
    - Tampilkan Data Proyek : Admin Proyek dapat memlihat database Pemukiman dan memilih beberapa menu seperti :
      - Tampilkan Data (urutkan berdasarkan ID - A-Z) : Admin Proyek dapat melihat tampilan data Proyek berdasarkan id yang diurutkan secara terurut atau 
        ascending 
      - Tampilkan Data (urutkan berdasarkan ID - Z-A) :  Admin Proyek dapat melihat tampilan data Proyek berdasarkan id yang diurutkan secara terbalik atau 
        ascending
      - Cari Data (berdasarkan ID) : Admin Proyek dapat mencari data Proyek dengan memasukan id Proyek
      - Kembali ke Menu Utama : Admin Proyek dapat kembali ke menu utama
    - Keluar : Admin Proyek dapat kembali ke menu sebelumnya
  
## fungsional
