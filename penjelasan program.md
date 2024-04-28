## PENJELASAN PROGRAM 
![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/1.png?raw=true)

- import mysql.connector: Baris ini mengimpor modul mysql.connector, yang menyediakan fungsi untuk terhubung dan berinteraksi dengan database MySQL di Python.
- from mysql.connector import Error: Ini mengimpor kelas Error secara khusus dari modul mysql.connector. Kelas ini kemungkinan digunakan untuk menangani kesalahan yang mungkin terjadi selama operasi database.
- import prettytable: Baris ini mengimpor modul prettytable, yang menawarkan alat untuk membuat tabel menarik secara visual untuk menampilkan data. Biasanya digunakan untuk menampilkan hasil query database dalam format yang jelas dan teratur.
- import getpass: Baris ini mengimpor modul getpass, yang menyediakan cara aman untuk meminta kata sandi pengguna tanpa menampilkannya di konsol. Ini sering digunakan saat terhubung ke database yang membutuhkan autentikasi.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/2.png?raw=true)

- mydb = mysql.connector.connect(...): Baris ini mencoba untuk terhubung ke database MySQL menggunakan fungsi mysql.connector.connect(). Fungsi ini menerima argumen sebagai berikut:
  - host: Nama host atau alamat IP dari server MySQL (dalam kasus ini, "sql6.freesqldatabase.com").
  - user: Username untuk mengakses database ("sql6701169").
  - password: Password untuk user tersebut ("Lh6evPczGK").
  - database: Nama database yang akan dihubungi ("sql6701169").
- Jika koneksi berhasil, fungsi connect() akan mengembalikan objek koneksi, yang disimpan dalam variabel mydb.
- mycursor = mydb.cursor(): Baris ini membuat objek kursor menggunakan metode cursor() dari objek koneksi mydb. Kursor bertindak sebagai penunjuk yang dapat digunakan untuk menjalankan pernyataan SQL dan mengambil hasil dari database.
- except Error as e:: Blok ini mendefinisikan penanganan pengecualian yang menangkap segala kesalahan (dari tipe Error) yang mungkin terjadi selama proses pembuatan koneksi. Bagian as e menetapkan kesalahan yang ditemui ke variabel e untuk diproses lebih lanjut.
- print("Error saat menghubungkan ke database:", e): Jika terjadi kesalahan, baris ini mencetak pesan informatif ke konsol: "Error saat menghubungkan ke database:" diikuti oleh detail kesalahan yang disimpan dalam e. Ini membantu dalam memecahkan masalah koneksi.
- exit(): Fungsi exit() menghentikan eksekusi program setelah mencetak pesan kesalahan. Ini adalah pendekatan umum untuk mencegah program melanjutkan dengan data atau tindakan yang mungkin salah.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/3.png?raw=true)

- Node: Ini adalah nama yang diberikan untuk kelas. Nama ini mencerminkan tujuan kelas, yaitu untuk mewakili node dalam struktur data tertaut.
- def __init__(self, data):: Ini adalah metode konstruktor kelas, yang dipanggil saat membuat instance baru dari kelas Node.
  - self: Parameter ini merujuk pada objek Node yang baru dibuat.
  - data: Parameter ini menampung nilai yang akan disimpan dalam node.
- self.data: Ini adalah atribut privat (private attribute) dari kelas Node. Atribut ini menyimpan nilai yang terkait dengan node.
  - data: Tipe data atribut ini tidak ditentukan dalam kode yang diberikan.
- self.next: Ini adalah atribut privat lainnya dari kelas Node. Atribut ini menunjuk ke node berikutnya dalam struktur data tertaut.
  - None: Nilai awal self.next adalah None, menunjukkan bahwa node baru tidak terhubung ke node lain pada saat pembuatan.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/4.png?raw=true)

- LinkedList: Ini adalah nama yang diberikan untuk kelas. Nama ini mencerminkan tujuan kelas, yaitu untuk mewakili struktur data tertaut.
- def __init__(self):: Ini adalah metode konstruktor kelas, yang dipanggil saat membuat instance baru dari kelas LinkedList.
  - self: Parameter ini merujuk pada objek LinkedList yang baru dibuat.
- self.head: Ini adalah atribut privat (private attribute) dari kelas LinkedList. Atribut ini menyimpan referensi ke node pertama (head) dalam struktur data tertaut.
  - None: Nilai awal self.head adalah None, menunjukkan bahwa linked list masih kosong pada saat pembuatan.
 
![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/5.png?raw=true)

- append: Nama ini menunjukkan fungsi dari metode, yaitu untuk menambahkan (append) data baru ke linked list.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode append.
- data: Parameter ini berisi nilai data yang akan disimpan dalam node baru yang akan ditambahkan.
- new_node = Node(data): Baris ini membuat sebuah node baru menggunakan kelas Node. Nilai data yang diberikan sebagai parameter diteruskan ke konstruktor kelas Node untuk disimpan dalam atribut data dari node baru tersebut.
- if not self.head:: Baris ini mengecek apakah linked list masih kosong (atribut head bernilai None).
  - self.head = new_node: Jika linked list kosong, node baru yang dibuat langsung ditetapkan sebagai node pertama (head) menggunakan self.head = new_node.
  - return: Setelah menetapkan head, fungsi append langsung dihentikan menggunakan return.
- last_node = self.head: Baris ini menyimpan referensi ke node pertama (head) ke dalam variabel last_node.
- while last_node.next:: Ini adalah perulangan while yang akan terus berjalan selama last_node.next tidak bernilai None. Atribut next dari sebuah node menunjuk ke node berikutnya dalam linked list.
  - last_node = last_node.next: Di dalam perulangan, last_node diperbarui untuk menunjuk ke node berikutnya, sehingga iterasi perulangan akan menelusuri linked list hingga mencapai node terakhir.
- last_node.next = new_node: Setelah perulangan selesai, last_node akan menunjuk ke node terakhir dalam linked list. Baris ini menetapkan atribut next dari node terakhir tersebut untuk menunjuk ke node baru (new_node). Ini essentially menghubungkan node baru ke akhir linked list.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/6.png?raw=true)

- display_admin: Nama ini menunjukkan fungsi dari metode, yaitu untuk menampilkan (display) data admin.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode display_admin.
- current = self.head: Baris ini menyimpan referensi ke node pertama (head) dari linked list ke dalam variabel current. Variabel ini akan digunakan untuk iterasi (menelusuri) linked list.
- x = PrettyTable(): Baris ini membuat objek dari library PrettyTable (kemungkinan library pihak ketiga yang belum didefinisikan sebelumnya). Objek ini mungkin digunakan untuk memformat tampilan data admin.
- x.field_names = ["ID Admin", "Nama Admin", "Email Admin", "Password Admin", "Role"]: Baris ini menetapkan nama kolom untuk tabel yang akan dibuat. Nama kolom ini sesuai dengan properti (atribut) yang mungkin dimiliki oleh objek admin yang tersimpan dalam node linked list.
- while current:: Ini adalah perulangan while yang akan terus berjalan selama current tidak bernilai None. Ingat current menunjuk ke node saat ini dalam linked list.
  - x.add_row(current.data): Di dalam perulangan, baris ini menambahkan baris baru ke tabel yang dibuat sebelumnya. current.data mengacu pada data yang tersimpan dalam node saat ini (kemungkinan berupa objek admin). Diasumsikan bahwa objek admin tersebut memiliki properti (atribut) yang sesuai dengan nama kolom yang telah ditetapkan sebelumnya.
  - current = current.next: Baris ini memperbarui current untuk menunjuk ke node berikutnya dalam linked list, sehingga iterasi selanjutnya akan memproses data admin dari node berikutnya.
- print(x): Setelah iterasi selesai, baris ini mencetak tabel yang telah diisi dengan data admin dari linked list menggunakan fungsi print.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/7.png?raw=true)

- display_perkotaan: Nama ini menunjukkan fungsi dari metode, yaitu untuk menampilkan (display) data perkotaan.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode display_perkotaan.
- current = self.head: Baris ini menyimpan referensi ke node pertama (head) dari linked list ke dalam variabel current. Variabel ini akan digunakan untuk iterasi (menelusuri) linked list.
- x = PrettyTable(): Baris ini membuat objek dari library PrettyTable (kemungkinan library pihak ketiga yang belum didefinisikan sebelumnya). Objek ini mungkin digunakan untuk memformat tampilan data perkotaan.
- x.field_names = ["ID", "Nama Kota", "Provinsi", "Jumlah Penduduk", "Luas Wilayah", "indeks keberlanjutan_kota", "ID ADMIN"]: Baris ini menetapkan nama kolom untuk tabel yang akan dibuat. Nama kolom ini sesuai dengan properti (atribut) yang mungkin dimiliki oleh objek perkotaan yang tersimpan dalam node linked list.
- while current:: Ini adalah perulangan while yang akan terus berjalan selama current tidak bernilai None. Ingat current menunjuk ke node saat ini dalam linked list.
  - x.add_row(current.data): Di dalam perulangan, baris ini menambahkan baris baru ke tabel yang dibuat sebelumnya. current.data mengacu pada data yang tersimpan dalam node saat ini (kemungkinan berupa objek perkotaan). Diasumsikan bahwa objek perkotaan tersebut memiliki properti (atribut) yang sesuai dengan nama kolom yang telah ditetapkan sebelumnya.
  - current = current.next: Baris ini memperbarui current untuk menunjuk ke node berikutnya dalam linked list, sehingga iterasi selanjutnya akan memproses data perkotaan dari node berikutnya.
- print(x): Setelah iterasi selesai, baris ini mencetak tabel yang telah diisi dengan data perkotaan dari linked list menggunakan fungsi print.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/8.png?raw=true)

- display_pemukiman: Nama ini menunjukkan fungsi dari metode, yaitu untuk menampilkan (display) data pemukiman.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode display_pemukiman.
- current = self.head: Baris ini menyimpan referensi ke node pertama (head) dari linked list ke dalam variabel current. Variabel ini akan digunakan untuk iterasi (menelusuri) linked list.
- x = PrettyTable(): Baris ini membuat objek dari library PrettyTable (kemungkinan library pihak ketiga yang belum didefinisikan sebelumnya). Objek ini mungkin digunakan untuk memformat tampilan data pemukiman.
- x.field_names = ["ID Pemukiman", "Nama Pemukiman", "ID Perkotaan", "Jenis Pemukiman", "Akses Air Bersih", "Akses Sanitasi Layak", "ID ADMIN"]: Baris ini menetapkan nama kolom untuk tabel yang akan dibuat. Nama kolom ini sesuai dengan properti (atribut) yang mungkin dimiliki oleh objek pemukiman yang tersimpan dalam node linked list.
- while current:: Ini adalah perulangan while yang akan terus berjalan selama current tidak bernilai None. Ingat current menunjuk ke node saat ini dalam linked list.
  - x.add_row(current.data): Di dalam perulangan, baris ini menambahkan baris baru ke tabel yang dibuat sebelumnya. current.data mengacu pada data yang tersimpan dalam node saat ini (kemungkinan berupa objek pemukiman). Diasumsikan bahwa objek pemukiman tersebut memiliki properti (atribut) yang sesuai dengan nama kolom yang telah ditetapkan sebelumnya.
  - current = current.next: Baris ini memperbarui current untuk menunjuk ke node berikutnya dalam linked list, sehingga iterasi selanjutnya akan memproses data pemukiman dari node berikutnya.
- print(x): Setelah iterasi selesai, baris ini mencetak tabel yang telah diisi dengan data pemukiman dari linked list menggunakan fungsi print.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/9.png?raw=true)

- display_proyek: Nama ini menunjukkan fungsi dari metode, yaitu untuk menampilkan (display) data proyek.
- self: Parameter ini merujuk pada objek LinkedList yang digunakan untuk memanggil metode display_proyek.
- current = self.head: Baris ini menyimpan referensi ke node pertama (head) dari linked list ke dalam variabel current. Variabel ini akan digunakan untuk iterasi (menelusuri) linked list.
- x = PrettyTable(): Baris ini membuat objek dari library PrettyTable (kemungkinan library pihak ketiga yang belum didefinisikan sebelumnya). Objek ini mungkin digunakan untuk memformat tampilan data proyek.
- x.field_names = ["ID Proyek", "Nama Proyek", "ID Pemukiman", "Deskripsi Proyek", "Jenis Proyek", "Dana Proyek", "Status Proyek", "ID ADMIN"]: Baris ini menetapkan nama kolom untuk tabel yang akan dibuat. Nama kolom ini sesuai dengan properti (atribut) yang mungkin dimiliki oleh objek proyek yang tersimpan dalam node linked list.
- while current:: Ini adalah perulangan while yang akan terus berjalan selama current tidak bernilai None. Ingat current menunjuk ke node saat ini dalam linked list.
  - x.add_row(current.data): Di dalam perulangan, baris ini menambahkan baris baru ke tabel yang dibuat sebelumnya. current.data mengacu pada data yang tersimpan dalam node saat ini (kemungkinan berupa objek proyek). Diasumsikan bahwa objek proyek tersebut memiliki properti (atribut) yang sesuai dengan nama kolom yang telah ditetapkan sebelumnya.
  - current = current.next: Baris ini memperbarui current untuk menunjuk ke node berikutnya dalam linked list, sehingga iterasi selanjutnya akan memproses data proyek dari node berikutnya.
- print(x): Setelah iterasi selesai, baris ini mencetak tabel yang telah diisi dengan data proyek dari linked list menggunakan fungsi print.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/10.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama quick_sort untuk mengurutkan elemen dalam list arr. Ini kemungkinan menggunakan algoritma pengurutan quicksort.
- arr: List yang berisi elemen-elemen yang akan diurutkan.
- ascending (opsional): Nilai boolean yang menentukan urutan pengurutan. True untuk urutan menaik (ascending), False untuk urutan menurun (descending). Default-nya adalah True (menaik).
- if len(arr) <= 1:: Baris ini mengecek apakah panjang list arr kurang dari atau sama dengan 1. Jika iya, maka list tersebut sudah terurut atau berisi tunggal elemen, dan langsung dikembalikan menggunakan return arr.
- pivot = arr[len(arr) // 2][0]: Baris ini memilih elemen pivot. Di sini, pivot diambil sebagai elemen tengah dari list arr (indeks len(arr) // 2). Kemudian, elemen pada indeks tersebut diakses menggunakan [0] untuk mendapatkan nilai pertamanya
- left = [x for x in arr if x[0] < pivot]: Baris ini membuat list baru bernama left yang berisi elemen-elemen dari arr yang lebih kecil dari nilai pivot. Ini menggunakan list comprehension untuk memfilter elemen-elemen yang memenuhi kondisi.
- middle = [x for x in arr if x[0] == pivot]: Baris ini membuat list baru bernama middle yang berisi elemen-elemen dari arr yang sama persis dengan nilai pivot.
- right = [x for x in arr if x[0] > pivot]: Baris ini membuat list baru bernama right yang berisi elemen-elemen dari arr yang lebih besar dari nilai pivot.
- if ascending:: Blok kode ini menangani pengurutan secara menaik.
  - return quick_sort(left, ascending) + middle + quick_sort(right, ascending): Baris ini memanggil fungsi quick_sort secara rekursif untuk mengurutkan list left dan right terlebih dahulu. Setelah itu, elemen-elemen dari left (yang sudah terurut), middle (pivot), dan right (yang sudah terurut) digabungkan menggunakan operator + untuk membentuk list yang terurut secara keseluruhan.
- else:: Blok kode ini menangani pengurutan secara menurun (descending).
  - return quick_sort(right, ascending) + middle + quick_sort(left, ascending): Perhatikan bahwa urutan pemanggilan fungsi quick_sort dibalik untuk mendapatkan urutan menurun. Elemen-elemen dari right (yang lebih besar) diurutkan terlebih dahulu, kemudian diikuti dengan middle dan left (yang lebih kecil).
- except Exception as e:: Blok kode ini menangani kemungkinan adanya kesalahan (exception) selama proses pengurutan.
  - print("Error saat melakukan sorting:", e): Jika terjadi kesalahan, pesan error akan dicetak ke konsol.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/11.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama jump_search untuk mencari elemen x dalam list arr.  Fungsi ini kemungkinan menggunakan teknik pencarian lompatan (jump search).
- arr: List yang berisi elemen-elemen yang akan dicari.
- x: Nilai yang ingin dicari dalam list arr.
- n = len(arr): Baris ini mendapatkan panjang dari list arr dan disimpan di variabel n.
- step = int(n ** 0.5): Baris ini menghitung nilai lompatan awal (step) berdasarkan akar pangkat dua dari panjang list n. Nilai ini dibulatkan menjadi integer menggunakan int().
- while arr[min(step, n)-1][0] < x:: Perulangan while ini berlanjut selama elemen pada indeks min(step, n)-1 (dikurangi 1 karena indeks dimulai dari 0) memiliki nilai yang lebih kecil dari nilai yang dicari x.
  - min(step, n) digunakan untuk memastikan indeks tidak melebihi batas akhir list arr.
- prev = step: Di dalam perulangan, nilai prev diperbarui dengan nilai step untuk menandai indeks lompatan selanjutnya.
- step += int(n ** 0.5): Nilai lompatan step diperbesar dengan nilai lompatan awal yang dihitung sebelumnya.
- if prev >= n:: Kondisi ini mengecek apakah prev sudah melewati batas akhir list arr. Jika ya, maka pencarian dihentikan dan fungsi mengembalikan -1 menandakan elemen tidak ditemukan.
- while arr[prev][0] < x:: Perulangan while kedua ini melakukan pencarian linear lokal di sekitar indeks yang diperoleh dari lompatan terakhir (prev). Perulangan berlanjut selama elemen pada indeks prev memiliki nilai yang lebih kecil dari nilai yang dicari x.
- prev += 1: Di dalam perulangan, indeks prev diincrement untuk memeriksa elemen selanjutnya.
- if prev == min(step, n): Kondisi ini mengecek apakah prev sudah mencapai batas akhir lompatan yang ditentukan sebelumnya (min(step, n)). Jika ya, maka pencarian lokal dihentikan dan fungsi mengembalikan -1 menandakan elemen tidak ditemukan.
- if arr[prev][0] == x:: Kondisi ini mengecek apakah elemen pada indeks prev sama persis dengan nilai yang dicari x. Jika ya, maka indeks tersebut (prev) dikembalikan sebagai hasil pencarian.
- return -1: Jika kesesuaian tidak ditemukan pada kondisi sebelumnya, maka fungsi mengembalikan -1 menandakan elemen tidak ditemukan dalam list arr.
- except Exception as e:: Blok kode ini menangani kemungkinan adanya kesalahan (exception) selama proses pencarian.
  - print("Error saat melakukan pencarian:", e): Jika terjadi kesalahan, pesan error akan dicetak ke konsol.
  - return -1: Fungsi tetap mengembalikan -1 untuk menandakan adanya kesalahan.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/12.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama read_admin kemungkinan untuk membaca data admin dari database dan menampilkannya.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan myresult).
- Class LinkedList telah didefinisikan sebelumnya dan memiliki fungsi append untuk menambahkan data dan display_admin untuk menampilkan data admin dalam format tabel.
- try:: Blok ini digunakan untuk mencoba menjalankan code di dalamnya. Jika terjadi kesalahan, blok except akan menangani.
- mycursor.execute("SELECT * FROM admin"): Baris ini mengirimkan query ke database untuk mengambil semua data dari tabel admin. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- myresult = mycursor.fetchall(): Baris ini mengambil semua hasil query yang dikembalikan oleh database dan disimpan di variabel myresult. Diasumsikan myresult berupa list yang berisi record-record data admin.
- ll = LinkedList(): Baris ini membuat objek baru dari class LinkedList dan disimpan di variabel ll. Objek ini kemungkinan digunakan untuk menyimpan data admin yang akan ditampilkan.
- for data in myresult:: Perulangan for ini iterasi melalui setiap record data admin yang ada di myresult.
  - ll.append(data): Di dalam perulangan, setiap record data admin (data) ditambahkan ke linked list ll menggunakan fungsi append.
- ll.display_admin(): Baris ini memanggil fungsi display_admin dari objek ll. Fungsi ini kemungkinan bertugas untuk menampilkan data admin yang tersimpan di linked list dalam format tabel yang rapi.
- except Error as e:: Blok ini akan dieksekusi jika terjadi kesalahan (exception) selama proses pembacaan data atau interaksi dengan database.
  - print("Error saat membaca data admin:", e): Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/13.png?raw=true)

- kode yang diberikan mendefinisikan sebuah fungsi bernama tambah_data_admin yang kemungkinan digunakan untuk menambahkan data admin baru ke database.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- try:: Blok ini digunakan untuk mencoba menjalankan code di dalamnya. Jika terjadi kesalahan, blok except akan menangani.
- nama_admin = input("Masukkan Nama Admin: "): Baris ini meminta pengguna untuk memasukkan nama admin dan disimpan di variabel nama_admin.
- email_admin = input("Masukkan Email Admin: "): Baris ini meminta pengguna untuk memasukkan email admin dan disimpan di variabel email_admin.
- password_admin = input("Masukkan Password Admin: "): Baris ini meminta pengguna untuk memasukkan password admin dan disimpan di variabel password_admin.
- role = input("Masukkan Role Admin: "): Baris ini meminta pengguna untuk memasukkan role admin dan disimpan di variabel role.
- query = f""": Baris ini memulai pembuatan string query SQL menggunakan f-string.
- INSERT INTO admin (nama_admin, email_admin, password_admin, role) VALUES ('{nama_admin}', '{email_admin}', '{password_admin}', '{role}'): Bagian ini berisi query SQL untuk menambahkan data admin baru ke tabel admin. Nilai-nilai yang dimasukkan (nama_admin, email_admin, password_admin, role) diambil dari variabel yang sudah diinput sebelumnya.
- """: Baris ini menutup pembuatan string query SQL.
- mycursor.execute(query): Baris ini menjalankan query SQL yang telah dibuat sebelumnya pada database. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- mydb.commit(): Baris ini melakukan komit perubahan ke database. Artinya, data admin baru yang ditambahkan akan disimpan secara permanen.
- print("Data Admin berhasil ditambahkan"): Baris ini mencetak pesan ke konsol untuk memberitahu pengguna bahwa data admin telah berhasil ditambahkan.
- except Error as e:: Blok ini akan dieksekusi jika terjadi kesalahan (exception) selama proses penambahan data admin.
- print("Error saat menambahkan data admin:", e): Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/14.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama hapus_data_admin kemungkinan untuk menghapus data admin dari database berdasarkan ID.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- try:: Blok ini digunakan untuk mencoba menjalankan code di dalamnya. Jika terjadi kesalahan, blok except akan menangani.
- id_admin = int(input("Masukkan ID Admin yang ingin dihapus: ")): Baris ini meminta pengguna untuk memasukkan ID admin yang ingin dihapus. input akan mengembalikan string, sehingga dilakukan konversi ke integer menggunakan int() untuk memastikan ID berupa angka.
- query = f"DELETE FROM admin WHERE id_admin = {id_admin}": Baris ini membuat query SQL untuk menghapus data admin dari tabel admin. Query tersebut akan mencari record yang memiliki id_admin sesuai dengan nilai yang dimasukkan pengguna (id_admin).
- mycursor.execute(query): Baris ini menjalankan query SQL yang telah dibuat sebelumnya pada database. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- mydb.commit(): Baris ini melakukan komit perubahan ke database. Artinya, penghapusan data admin akan disimpan secara permanen.
- print("Data Admin berhasil dihapus"): Baris ini mencetak pesan ke konsol untuk memberitahu pengguna bahwa data admin telah berhasil dihapus.
- except ValueError:: Blok ini akan dieksekusi jika terjadi kesalahan ValueError selama konversi input ID admin menjadi integer. ValueError biasanya muncul ketika pengguna memasukkan input yang bukan angka.
  - print("Masukkan ID Admin yang valid."): Baris ini menampilkan pesan kepada pengguna untuk memasukkan ID admin yang valid (berupa angka).
- except Error as e:: Blok ini akan dieksekusi jika terjadi kesalahan (exception) lain selama proses penghapusan data admin.
  - print("Error saat menghapus data admin:", e): Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/15.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama perbarui_data_admin untuk memperbarui data admin di database.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- try:: Blok ini digunakan untuk mencoba menjalankan code di dalamnya. Jika terjadi kesalahan, blok except akan menangani.
- id_admin = int(input("Masukkan ID Admin yang ingin diperbarui: ")): Baris ini meminta pengguna untuk memasukkan ID admin yang ingin diperbarui. Input dikonversi ke integer menggunakan int() untuk memastikan ID berupa angka.
- nama_admin = input("Masukkan Nama Admin Baru: "): Baris ini meminta pengguna untuk memasukkan nama admin baru.
- email_admin = input("Masukkan Email Admin Baru: "): Baris ini meminta pengguna untuk memasukkan email admin baru.
- password_admin = input("Masukkan Password Admin Baru: "): Baris ini meminta pengguna untuk memasukkan password admin baru.
- role = input("Masukkan Role Admin Baru: "): Baris ini meminta pengguna untuk memasukkan role admin baru.
- query = f""": Baris ini memulai pembuatan string query SQL menggunakan f-string.
- UPDATE admin: Bagian ini menunjukkan bahwa query akan melakukan update pada tabel admin.
- SET nama_admin = '{nama_admin}', email_admin = '{email_admin}', password_admin = '{password_admin}', role = '{role}': Bagian ini berisi daftar kolom yang akan diperbarui beserta nilai barunya. Nilai-nilai baru diambil dari variabel yang sudah diinput sebelumnya.
- WHERE id_admin = {id_admin}: Bagian ini menentukan kondisi WHERE untuk memperbarui hanya record yang memiliki id_admin sesuai dengan ID yang dimasukkan pengguna.
- """: Baris ini menutup pembuatan string query SQL.
- mycursor.execute(query): Baris ini menjalankan query SQL yang telah dibuat sebelumnya pada database. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- if mycursor.rowcount == 0:: Blok ini mengecek apakah ada record yang diperbarui dengan menggunakan mycursor.rowcount. rowcount akan mengembalikan jumlah record yang terpengaruh oleh query.
  - print("ID Admin tidak ditemukan."): Jika rowcount 0, berarti tidak ada record yang ditemukan dengan ID yang diberikan, dan pesan ini akan dicetak ke konsol.
- else:: Blok ini dijalankan jika ada record yang diperbarui (karena rowcount > 0).
  - mydb.commit(): Baris ini melakukan komit perubahan ke database. Artinya, pembaruan data admin akan disimpan secara permanen.
  - print("Data Admin berhasil diperbarui"): Baris ini mencetak pesan ke konsol untuk memberitahu pengguna bahwa data admin telah berhasil diperbarui.
- except ValueError:: Blok ini akan dieksekusi jika terjadi kesalahan ValueError selama konversi input ID admin atau input data lainnya ke format yang sesuai.
  - print("Masukkan ID Admin dalam bentuk bilangan bulat."): Baris ini menampilkan pesan kepada pengguna untuk memasukkan ID admin dalam bentuk bilangan bulat (jika terjadi error konversi ID admin).
- except Exception as e:: Blok ini akan dieksekusi jika terjadi kesalahan (exception) lain selama proses pembaruan data admin.
  - print("Terjadi kesalahan:", e): Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/16.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama read_perkotaan kemungkinan untuk membaca dan menampilkan data perkotaan dari database.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- Class LinkedList dan fungsi quick_sort dan jump_search telah didefinisikan sebelumnya.
- mycursor.execute("SELECT * FROM perkotaan"): Baris ini menjalankan query SQL untuk mengambil semua data dari tabel perkotaan.
- myresult = mycursor.fetchall(): Baris ini mengambil semua hasil query yang dikembalikan oleh database dan disimpan di variabel myresult. Diasumsikan myresult berupa list yang berisi record-record data perkotaan.
- data_list = []: Baris ini membuat list kosong bernama data_list untuk menyimpan data perkotaan.
- for data in myresult:: Perulangan for ini iterasi melalui setiap record data perkotaan di myresult.
  - data_list.append(data): Di dalam perulangan, setiap record data perkotaan (data) ditambahkan ke list data_list.
- while True:: Perulangan while True ini membuat menu interaktif terus berjalan sampai pengguna memilih untuk kembali ke menu utama.
  - print("============================================================"): Baris ini mencetak garis pemisah untuk membatasi bagian menu.
  - print("|                 TAMPILKAN DATA PERKOTAAN                 |"): Baris ini mencetak judul menu.
  - print("============================================================"): Baris ini mencetak garis pemisah lagi.
  - print("|   1. Tampilkan Data (urutkan berdasarkan ID - A-Z)       |"): Baris ini menampilkan pilihan menu 1.
  - print("|   2. Tampilkan Data (urutkan berdasarkan ID - Z-A)       |"): Baris ini menampilkan pilihan menu 2.
  - print("|   3. Cari Data (berdasarkan ID)                          |"): Baris ini menampilkan pilihan menu 3.
  - print("|   4. Kembali ke Menu Utama                               |"): Baris ini menampilkan pilihan menu 4.
  - print("============================================================"): Baris ini mencetak garis pemisah lagi.
  - pilihan = input("Masukkan pilihan Anda: "): Baris ini meminta pengguna untuk memasukkan pilihan mereka.
- if pilihan == "1":: Blok ini dijalankan jika pengguna memilih menu 1.
  - sorted_data = quick_sort(data_list, ascending=True): Baris ini mengurutkan data di data_list secara ascending (dari kecil ke besar) menggunakan fungsi quick_sort.
  - ll = LinkedList(): Baris ini membuat objek baru dari class LinkedList dan disimpan di variabel ll.
  - for data in sorted_data:: Perulangan for ini iterasi melalui data yang sudah diurutkan (sorted_data).
  - ll.append(data): Di dalam perulangan, setiap data di sorted_data ditambahkan ke linked list ll.
  - ll.display_perkotaan(): Baris ini memanggil fungsi display_perkotaan dari objek ll untuk menampilkan data perkotaan yang sudah diurutkan.
-  elif pilihan == "2":: Blok ini dijalankan jika pengguna memilih menu 2.
  - sorted_data = quick_sort(data_list, ascending=False): Baris ini mengurutkan data di data_list secara descending (dari besar ke kecil) menggunakan fungsi quick_sort.
  - ll = LinkedList(): Baris ini membuat objek baru dari class LinkedList dan disimpan di variabel ll.
  - for data in sorted_data:: Perulangan for ini iterasi melalui data yang sudah diurutkan (sorted_data).
- elif pilihan == "3":: Blok ini dijalankan jika pengguna memilih menu 3 (pencarian data).
  - id_to_search = int(input("Masukkan ID yang ingin dicari: "))**: Baris ini meminta pengguna untuk memasukkan ID yang ingin dicari. Input dikonversi ke integer menggunakan int() untuk memastikan ID berupa angka.
  - result_index = jump_search(data_list, id_to_search)**: Baris ini menggunakan fungsi jump_search untuk mencari data dengan ID yang dimasukkan dalam list data_list. jump_search mengembalikan indeks data yang ditemukan (atau -1 jika tidak ditemukan).
  - if result_index != -1:**: Blok ini dijalankan jika data ditemukan (karena result_index bukan -1).
   - print("Data ditemukan:")**: Baris ini mencetak pesan bahwa data ditemukan.
   - x = PrettyTable()**: Baris ini membuat objek PrettyTable untuk menampilkan data dengan format tabel yang rapi.
   - x.field_names = ["ID", "Nama Kota", "Provinsi", "Jumlah Penduduk", "Luas Wilayah", "Indeks Keberlanjutan", "ID ADMIN"]**: Baris ini menentukan nama-nama kolom yang akan ditampilkan di tabel.
   - x.add_row(data_list[result_index])**: Baris ini menambahkan data yang ditemukan (pada indeks result_index) ke tabel PrettyTable.
   - print(x)**: Baris ini mencetak tabel PrettyTable yang berisi data yang ditemukan.
  - else:**: Blok ini dijalankan jika data tidak ditemukan (karena result_index = -1).
   - print("Data tidak ditemukan.")**: Baris ini mencetak pesan bahwa data tidak ditemukan.
- elif pilihan == "4":: Blok ini dijalankan jika pengguna memilih menu 4 (kembali ke menu utama).
  - break**: Kata kunci break digunakan untuk keluar dari perulangan while True dan kembali ke menu utama.
- else:: Blok ini dijalankan jika pengguna memasukkan pilihan yang tidak valid.
  - print("Pilihan tidak valid. Silakan pilih kembali.")**: Baris ini mencetak pesan bahwa pilihan yang dimasukkan tidak valid dan meminta pengguna untuk memilih kembali.
- except ValueError:: Blok ini dijalankan jika terjadi error ValueError selama konversi input (misalnya pengguna memasukkan ID yang bukan angka).
  - print("Input tidak valid.")**: Baris ini mencetak pesan bahwa input yang dimasukkan tidak valid.
- except Error as e:: Blok ini dijalankan jika terjadi error (exception) lain selama proses program.
  - print("Error saat membaca data perkotaan:", e)**: Baris ini mencetak pesan error yang terjadi ke konsol. Variabel e berisi informasi mengenai error tersebut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/17.png?raw=true)

- Kode yang diberikan mendefinisikan sebuah fungsi bernama tambah_data_perkotaan yang kemungkinan digunakan untuk menambahkan data perkotaan baru ke database.
- Kode ini menggunakan library eksternal untuk interaksi dengan database, kemungkinan library tersebut bernama MySQL (berdasarkan penggunaan mycursor dan mydb).
- nama_kota = input("Masukkan Nama Kota: "): Baris ini meminta pengguna untuk memasukkan nama kota.
- provinsi = input("Masukkan Provinsi: "): Baris ini meminta pengguna untuk memasukkan provinsi.
- jumlah_penduduk = int(input("Masukkan Jumlah Penduduk: ")): Baris ini meminta pengguna untuk memasukkan jumlah penduduk. Input dikonversi ke integer menggunakan int() untuk memastikan format data valid.
- luas_wilayah = None: Baris ini menginisialisasi variabel luas_wilayah dengan nilai None.
- Loop while luas_wilayah is None:: Perulangan ini akan terus berjalan sampai nilai luas_wilayah valid dimasukkan.
  - try:: Blok ini digunakan untuk mencoba konversi input luas wilayah.
   - luas_wilayah = float(input("Masukkan Luas Wilayah: ")): Baris ini meminta pengguna untuk memasukkan luas wilayah. Input dikonversi ke float menggunakan float() untuk memastikan format data valid.
  - except ValueError:: Blok ini dijalankan jika terjadi error ValueError saat konversi input.
   - print("Luas wilayah harus berupa angka."): Baris ini mencetak pesan error kepada pengguna.
- indeks_keberlanjutan_kota = int(input("Masukkan Indeks Keberlanjutan Kota: ")): Baris ini meminta pengguna untuk memasukkan indeks keberlanjutan kota. Input dikonversi ke integer menggunakan int() untuk memastikan format data valid.
- id_admin = int(input("Masukkan ID Admin: ")): Baris ini meminta pengguna untuk memasukkan ID admin. Input dikonversi ke integer menggunakan int() untuk memastikan format data valid.
- if jumlah_penduduk < 0 or luas_wilayah < 0:: Blok ini mengecek apakah jumlah penduduk atau luas wilayah kurang dari 0.
  - raise ValueError("Jumlah penduduk dan luas wilayah tidak boleh negatif"): Baris ini memicu error ValueError jika salah satu kondisi terpenuhi. Pesan error yang akan ditampilkan juga dicantumkan.
- query_check_admin = "SELECT id_admin FROM admin WHERE id_admin = {}".format(id_admin): Baris ini membuat query SQL untuk memeriksa apakah ID admin yang dimasukkan ada di tabel admin.
- mycursor.execute(query_check_admin): Baris ini menjalankan query SQL yang dibuat sebelumnya.
- result_admin = mycursor.fetchone(): Baris ini mengambil hasil pertama dari query (jika ada).
- if not result_admin:: Blok ini dijalankan jika result_admin tidak ada (artinya ID admin tidak ditemukan).
  - print("ID Admin tidak ditemukan dalam database."): Baris ini mencetak pesan error kepada pengguna.
  - return: Kata kunci return digunakan untuk keluar dari fungsi tanpa menambahkan data.
- query = f""": Baris ini memulai pembuatan string query SQL menggunakan f-string.
- INSERT INTO perkotaan (nama_kota, provinsi, jumlah_penduduk, luas_wilayah, indeks_keberlanjutan_kota, id_admin) VALUES ('{nama_kota}', '{provinsi}', {jumlah_penduduk}, {luas_wilayah}, {indeks_keberlanjutan_kota}, {id_admin}): Bagian ini berisi query SQL untuk menambahkan data perkotaan baru ke tabel perkotaan. Nilai-nilai data diambil dari variabel yang sudah diinput sebelumnya.
- """: Baris ini menutup pembuatan string query SQL.
- mycursor.execute(query): Baris ini menjalankan query SQL yang telah dibuat sebelumnya. mycursor diasumsikan sebagai objek yang sudah terhubung ke database.
- mydb.commit(): Baris ini melakukan komit perubahan ke database. Artinya, data perkotaan baru yang ditambahkan akan disimpan secara permanen.
- Blok except ini menangani pengecualian ValueError. Pengecualian ini biasanya muncul ketika operasi matematika atau konversi data gagal karena input yang tidak valid.
  - kode akan mencetak pesan "Data berhasil ditambahkan" ketika pengecualian ValueError tertangkap.
- Blok except ini menangani pengecualian generik Error. Pengecualian ini lebih luas dan dapat menangkap berbagai jenis kesalahan, termasuk ValueError
  - "Input tidak valid." - Pesan ini menunjukkan bahwa ada masalah dengan input data.
  - "Error saat menambahkan data perkotaan:", e - Pesan ini menampilkan informasi detail tentang pengecualian yang tertangkap, termasuk objek pengecualian e. Objek ini berisi informasi tentang jenis kesalahan dan penyebabnya.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/18.png?raw=true)

- Fungsi ini memiliki tujuan untuk menghapus data dari tabel perkotaan di database MySQL.
- Fungsi meminta pengguna untuk memasukkan ID perkotaan yang ingin dihapus melalui input("Masukkan ID Perkotaan yang ingin dihapus: ").
- Input ini kemudian diubah menjadi tipe data integer menggunakan int().
- Sebuah string query SQL f"DELETE FROM perkotaan WHERE id_perkotaan = {id_perkotaan}" dibuat.
- Query ini menggunakan placeholder {id_perkotaan} untuk memasukkan nilai ID perkotaan yang diperoleh dari input pengguna.
- Query SQL dieksekusi menggunakan mycursor.execute(query).
- Perubahan pada database kemudian dikomit menggunakan mydb.commit().
- Jika proses penghapusan data berhasil, fungsi akan mencetak pesan "Data berhasil dihapus".
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
- Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi jika input ID perkotaan bukan bilangan bulat yang valid.
  - Dalam blok ini, fungsi akan mencetak pesan "Input tidak valid."
- Blok except Error menangani pengecualian generik Error yang mungkin terjadi selama proses penghapusan data.
  - Dalam blok ini, fungsi akan mencetak pesan "Error saat menghapus data perkotaan:" diikuti dengan objek pengecualian e.
 
![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/19.png?raw=true)

- Fungsi perbarui_data_perkotaan() ini dirancang untuk memperbarui data perkotaan di tabel perkotaan database MySQL
- Fungsi meminta pengguna untuk memasukkan beberapa informasi baru untuk memperbarui data perkotaan, termasuk:
  - id_perkotaan: ID perkotaan yang ingin diperbarui (harus bilangan bulat)
  - nama_kota: Nama kota baru
  - provinsi: Provinsi baru
  - jumlah_penduduk: Jumlah penduduk baru (harus bilangan bulat)
  - luas_wilayah: Luas wilayah baru (harus bilangan pecahan)
  - indeks_keberlanjutan_kota: Indeks keberlanjutan kota baru (harus bilangan bulat)
  - id_admin: ID admin yang terkait dengan perkotaan (harus bilangan bulat)
- Fungsi menggunakan loop while untuk memvalidasi input luas_wilayah.
  - Loop ini terus berjalan sampai pengguna memasukkan nilai numerik yang valid (bilangan pecahan).
  - Jika input tidak valid, pesan "Luas wilayah harus berupa angka." akan dicetak.
- Fungsi juga melakukan validasi untuk memastikan jumlah_penduduk dan luas_wilayah tidak negatif.
  - Jika salah satu nilainya negatif, pengecualian ValueError akan dibangkitkan.
- Fungsi menjalankan query SQL SELECT id_admin FROM admin WHERE id_admin = {id_admin} untuk memeriksa apakah ID Admin yang dimasukkan ada di tabel admin.
  - Jika ID Admin tidak ditemukan, pesan "ID Admin tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan.
- Fungsi membangun string query SQL UPDATE untuk memperbarui data perkotaan di tabel perkotaan.
  - Query ini menggunakan placeholder untuk memasukkan nilai-nilai baru yang diperoleh dari input pengguna.
- Query dijalankan menggunakan mycursor.execute(query).
- Fungsi memeriksa nilai mycursor.rowcount untuk mengetahui apakah data berhasil diperbarui.
  - Jika rowcount sama dengan 0, berarti tidak ada data yang diperbarui, dan pesan "ID Perkotaan atau ID Admin tidak ditemukan." akan dicetak.
  - Jika rowcount lebih besar dari 0, berarti data berhasil diperbarui, dan pesan "Data berhasil diperbarui" akan dicetak.
- Terakhir, perubahan pada database dikomit menggunakan mydb.commit().
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi selama validasi input.
  - Pesan informatif akan dicetak untuk membantu pengguna memahami jenis kesalahan yang terjadi.
- Blok except Exception menangani semua jenis pengecualian lain yang mungkin terjadi.
  - Pesan generik "Terjadi kesalahan:" akan dicetak, diikuti dengan objek pengecualian e untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/20.png?raw=true)

- Fungsi read_pemukiman() ini dirancang untuk menampilkan dan mencari data pemukiman dari database MySQL.
- Fungsi menggunakan mycursor.execute("SELECT * FROM pemukiman") untuk mengambil semua data dari tabel pemukiman.
- Hasil query disimpan dalam variabel myresult.
- Data kemudian diubah menjadi daftar yang dapat diakses menggunakan data_list = [] dan for data in myresult: data_list.append(data).
- Fungsi menampilkan menu utama dengan opsi berikut:
  - Tampilkan Data (urutkan berdasarkan ID - A-Z)
  - Tampilkan Data (urutkan berdasarkan ID - Z-A)
  - Cari Data (berdasarkan ID)
  - Kembali ke Menu Utama
- Fungsi menggunakan loop while True untuk terus menampilkan menu utama dan memproses pilihan pengguna.
- Pengguna memasukkan pilihannya melalui pilihan = input("Masukkan pilihan Anda: ").
- Jika pilihan adalah "1" atau "2":
   - "1": Urutkan menaik (A-Z)
   - "2": Urutkan menurun (Z-A)
  - Fungsi menggunakan quick_sort() untuk mengurutkan data.
  - Data yang diurutkan kemudian diubah menjadi objek LinkedList menggunakan ll = LinkedList().
  - Data ditampilkan menggunakan ll.display_pemukiman().
- Jika pilihan adalah "3":
  - Pengguna memasukkan ID yang ingin dicari melalui id_to_search = int(input("Masukkan ID yang ingin dicari: ")).
  - Fungsi menggunakan jump_search() untuk mencari data dengan ID yang diberikan.
  - Jika data ditemukan:
   - Data ditampilkan dalam tabel yang rapi menggunakan PrettyTable.
  - Jika data tidak ditemukan, pesan "Data tidak ditemukan." akan dicetak.
- Jika pilihan adalah "4":
  - Loop while True diakhiri dengan break, yang membawa pengguna kembali ke menu utama program.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi saat membaca input pengguna.
   - Pesan "Input tidak valid." akan dicetak.
  - Blok except Error menangani semua jenis pengecualian lain yang mungkin terjadi.
   - Pesan generik "Error saat membaca data pemukiman:" akan dicetak, diikuti dengan objek pengecualian e untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/21.png?raw=true)

- Fungsi tambah_data_pemukiman() ini dirancang untuk menambahkan data pemukiman baru ke database MySQL.
- ungsi meminta pengguna untuk memasukkan informasi berikut:
  - nama_pemukiman: Nama pemukiman (string)
  - id_perkotaan: ID perkotaan yang terkait dengan pemukiman (integer)
  - jenis_pemukiman: Jenis pemukiman (formal atau informal, string)
  - akses_air_bersih: Akses air bersih (ya atau tidak, string)
  - akses_sanitasi_layak: Akses sanitasi layak (ya atau tidak, string)
  - id_admin: ID admin yang bertanggung jawab atas pemukiman (integer)
- Fungsi menjalankan query SQL SELECT id_perkotaan FROM perkotaan WHERE id_perkotaan = {id_perkotaan} untuk memeriksa apakah ID Perkotaan yang dimasukkan ada di tabel perkotaan.
  - Jika ID Perkotaan tidak ditemukan, pesan "ID Perkotaan tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan.
- Fungsi menjalankan query SQL serupa SELECT id_admin FROM admin WHERE id_admin = {id_admin} untuk memeriksa apakah ID Admin yang dimasukkan ada di tabel admin.
  - Jika ID Admin tidak ditemukan, pesan "ID Admin tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan.
- Fungsi membangun string query SQL INSERT INTO untuk menambahkan data pemukiman baru ke tabel pemukiman.
  - Query menggunakan placeholder untuk memasukkan nilai-nilai yang diperoleh dari input pengguna.
- Query dijalankan menggunakan mycursor.execute(query_insert_pemukiman).
- Fungsi menggunakan mydb.commit() untuk mengkomit perubahan ke database.
- Fungsi menggunakan mydb.commit() untuk mengkomit perubahan ke database.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi selama validasi input.
  - Pesan "Input tidak valid:" beserta objek pengecualian e akan dicetak untuk membantu pengguna memahami jenis kesalahan yang terjadi.
- Blok except Error menangani semua jenis pengecualian lain yang mungkin terjadi.
  - Pesan generik "Error saat menambahkan data pemukiman:" beserta objek pengecualian e akan dicetak untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/22.png?raw=true)

- Fungsi hapus_data_pemukiman() ini dirancang untuk menghapus data pemukiman dari database MySQL berdasarkan ID pemukiman yang diberikan.
- Fungsi meminta pengguna untuk memasukkan ID pemukiman yang ingin dihapus melalui id_pemukiman = int(input("Masukkan ID Pemukiman yang ingin dihapus: ")).
- Input diubah menjadi tipe data integer menggunakan int().
- Fungsi membangun string query SQL DELETE untuk menghapus data pemukiman dari tabel pemukiman.
  - Query menggunakan placeholder {id_pemukiman} untuk memasukkan nilai ID pemukiman yang diperoleh dari input pengguna.
- Query dijalankan menggunakan mycursor.execute(query).
- Perubahan pada database kemudian dikomit menggunakan mydb.commit().
- Jika proses penghapusan data berhasil, pesan "Data berhasil dihapus" akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi jika input ID pemukiman bukan bilangan bulat yang valid.
  - Pesan "Input tidak valid." akan dicetak.
- Blok except Error menangani semua jenis pengecualian lain yang mungkin terjadi selama proses penghapusan data.
  - Pesan generik "Error saat menghapus data pemukiman:" beserta objek pengecualian e akan dicetak untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/23.png?raw=true)

- Fungsi perbarui_data_pemukiman() ini dirancang untuk memperbarui data pemukiman di database MySQL.
- Fungsi meminta pengguna untuk memasukkan informasi berikut untuk memperbarui data pemukiman:
  - id_pemukiman: ID pemukiman yang ingin diperbarui (harus bilangan bulat)
  - nama_pemukiman: Nama pemukiman baru
  - id_perkotaan: ID perkotaan baru (harus bilangan bulat)
  - jenis_pemukiman: Jenis pemukiman baru
  - akses_air_bersih: Akses air bersih baru
  - akses_sanitasi_layak: Akses sanitasi layak baru
  - id_admin: ID admin yang terkait dengan pemukiman (harus bilangan bulat)
- Fungsi menjalankan query SQL SELECT id_perkotaan FROM perkotaan WHERE id_perkotaan = {id_perkotaan} untuk memeriksa apakah ID Perkotaan yang dimasukkan ada di tabel perkotaan.
  - Jika ID Perkotaan tidak ditemukan, pesan "ID Perkotaan tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan.
- Fungsi menjalankan query SQL serupa SELECT id_admin FROM admin WHERE id_admin = {id_admin} untuk memeriksa apakah ID Admin yang dimasukkan ada di tabel admin.
  - Jika ID Admin tidak ditemukan, pesan "ID Admin tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan.
- Fungsi membangun string query SQL UPDATE untuk memperbarui data pemukiman di tabel pemukiman.
  - Query menggunakan placeholder untuk memasukkan nilai-nilai baru yang diperoleh dari input pengguna.
- Query dijalankan menggunakan mycursor.execute(query).
- Fungsi memeriksa nilai mycursor.rowcount untuk mengetahui apakah data berhasil diperbarui.
  - Jika rowcount sama dengan 0, berarti tidak ada data yang diperbarui, dan pesan "ID Pemukiman tidak ditemukan." akan dicetak.
  - Jika rowcount lebih besar dari 0, berarti data berhasil diperbarui, dan pesan "Data berhasil diperbarui" akan dicetak.
- Terakhir, perubahan pada database dikomit menggunakan mydb.commit().
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi selama validasi input ID pemukiman dan ID perkotaan.
  - Pesan informatif "Pastikan input berupa bilangan bulat untuk ID pemukiman dan ID perkotaan." akan dicetak untuk membantu pengguna memahami jenis kesalahan yang terjadi.
  - Blok except Exception menangani semua jenis pengecualian lain yang mungkin terjadi.
  - Pesan generik "Terjadi kesalahan:", beserta objek pengecualian e akan dicetak untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/24.png?raw=true)

- Fungsi read_proyek() ini dirancang untuk menampilkan dan mencari data proyek dari database MySQL.
- Fungsi menggunakan mycursor.execute("SELECT * FROM proyek") untuk mengambil semua data dari tabel proyek.
- Hasil query disimpan dalam variabel myresult.
- Data kemudian diubah menjadi daftar yang dapat diakses menggunakan data_list = [] dan for data in myresult: data_list.append(data).
- Fungsi menampilkan menu utama dengan opsi berikut:
  - Tampilkan Data (urutkan berdasarkan ID - A-Z)
  - Tampilkan Data (urutkan berdasarkan ID - Z-A)
  - Cari Data (berdasarkan ID)
  - Kembali ke Menu Utama
- Fungsi menggunakan loop while True untuk terus menampilkan menu utama dan memproses pilihan pengguna.
- Pengguna memasukkan pilihannya melalui pilihan = input("Masukkan pilihan Anda: ").
- Jika pilihan adalah "1" atau "2":
  - Data diurutkan berdasarkan ID:
  - "1": Urutkan menaik (A-Z)
  - "2": Urutkan menurun (Z-A)
  - Fungsi menggunakan quick_sort() untuk mengurutkan data.
  - Data yang diurutkan kemudian diubah menjadi objek LinkedList menggunakan ll = LinkedList().
  - Data ditampilkan menggunakan ll.display_proyek().
- Jika pilihan adalah "3":
  - Pengguna memasukkan ID yang ingin dicari melalui id_to_search = int(input("Masukkan ID yang ingin dicari: ")).
  - Fungsi menggunakan jump_search() untuk mencari data dengan ID yang diberikan.
  - Jika data ditemukan:
  - Data ditampilkan dalam tabel yang rapi menggunakan PrettyTable.
  - Jika data tidak ditemukan, pesan "Data tidak ditemukan." akan dicetak.
- Jika pilihan adalah "4":
  - Loop while True diakhiri dengan break, yang membawa pengguna kembali ke menu utama program.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi saat membaca input pengguna.
  - Pesan "Input tidak valid." akan dicetak.
- Blok except Error menangani semua jenis pengecualian lain yang mungkin terjadi.
  - Pesan generik "Error saat membaca data proyek:" beserta objek pengecualian e akan dicetak untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/25.png?raw=true)

- Fungsi tambah_data_proyek() dirancang untuk menambahkan data proyek baru ke database MySQL.
- Fungsi meminta pengguna untuk memasukkan informasi berikut untuk proyek baru:
  - nama_proyek: Nama proyek (string)
  - id_pemukiman: ID pemukiman terkait proyek (integer)
  - deskripsi_proyek: Deskripsi singkat tentang proyek (string)
  - jenis_proyek: Jenis proyek (string)
  - dana_proyek: Anggaran proyek (integer)
  - status_proyek: Status proyek saat ini (string)
  - id_admin: ID admin yang bertanggung jawab atas proyek (integer)
-  Fungsi menggunakan if dana_proyek < 0: untuk memeriksa apakah nilai dana_proyek negatif.
  - Jika nilai negatif, pengecualian ValueError dengan pesan "Dana proyek tidak boleh negatif" akan dibuat dan diangkat.
- Fungsi menjalankan query SQL SELECT id_pemukiman FROM pemukiman WHERE id_pemukiman = {id_pemukiman} untuk memeriksa apakah ID Pemukiman yang dimasukkan ada di tabel pemukiman.
  - Jika ID Pemukiman tidak ditemukan, pesan "ID pemukiman tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan.
- Fungsi menjalankan query SQL serupa SELECT id_admin FROM admin WHERE id_admin = {id_admin} untuk memeriksa apakah ID Admin yang dimasukkan ada di tabel admin.
  - Jika ID Admin tidak ditemukan, pesan "ID admin tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan.
- Fungsi membangun string query SQL INSERT INTO untuk menambahkan data proyek baru ke tabel proyek.
  - Query menggunakan placeholder untuk memasukkan nilai-nilai yang diperoleh dari input pengguna.
- Query dijalankan menggunakan mycursor.execute(query).
- Fungsi menggunakan mydb.commit() untuk mengkomit perubahan ke database.
- Jika proses insert data berhasil, pesan "Data berhasil ditambahkan" akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi selama validasi input atau jika ID Pemukiman/Admin tidak valid.
  - Pesan "Input tidak valid." akan dicetak.
  - Blok except Error menangani semua jenis pengecualian lain yang mungkin terjadi selama proses insert data.
  - Pesan generik "Error saat menambahkan data proyek:" beserta objek pengecualian e akan dicetak untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/26.png?raw=true)

- Fungsi hapus_data_proyek() dirancang untuk menghapus data proyek dari database MySQL berdasarkan ID proyek yang diberikan.
- Fungsi meminta pengguna untuk memasukkan ID proyek yang ingin dihapus melalui id_proyek = int(input("Masukkan ID Proyek yang ingin dihapus: ")).
- Input diubah menjadi tipe data integer menggunakan int().
- Fungsi membangun string query SQL DELETE untuk menghapus data proyek dari tabel proyek.
  - Query menggunakan placeholder {id_proyek} untuk memasukkan nilai ID proyek yang diperoleh dari input pengguna.
- Query dijalankan menggunakan mycursor.execute(query).
- Perubahan pada database kemudian dikomit menggunakan mydb.commit().
- Jika proses penghapusan data berhasil, pesan "Data berhasil dihapus" akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi jika input ID proyek bukan bilangan bulat yang valid.
  - Pesan "Input tidak valid." akan dicetak.
  - Blok except Error menangani semua jenis pengecualian lain yang mungkin terjadi selama proses penghapusan data.
  - Pesan generik "Error saat menghapus data proyek:" beserta objek pengecualian e akan dicetak untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/27.png?raw=true)

- Fungsi perbarui_data_proyek() dirancang untuk memperbarui data proyek di database MySQL.
- Fungsi meminta pengguna untuk memasukkan informasi berikut untuk memperbarui data proyek:
  - id_proyek: ID proyek yang ingin diperbarui (harus bilangan bulat)
  - nama_proyek: Nama proyek baru
  - id_pemukiman: ID pemukiman baru (harus bilangan bulat)
  - deskripsi_proyek: Deskripsi singkat baru tentang proyek
  - jenis_proyek: Jenis proyek baru
  - dana_proyek: Anggaran proyek baru (harus bilangan bulat)
  - status_proyek: Status proyek baru
  - id_admin: ID admin yang bertanggung jawab atas proyek (harus bilangan bulat)
- Fungsi menggunakan if dana_proyek < 0: untuk memeriksa apakah nilai dana_proyek negatif.
  - Jika nilai negatif, pengecualian ValueError dengan pesan "Dana proyek tidak boleh negatif" akan dibuat dan diangkat.
- Fungsi menjalankan query SQL SELECT id_pemukiman FROM pemukiman WHERE id_pemukiman = {id_pemukiman} untuk memeriksa apakah ID Pemukiman yang dimasukkan ada di tabel pemukiman.
  - Jika ID Pemukiman tidak ditemukan, pesan "ID pemukiman tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan.
- Fungsi menjalankan query SQL serupa SELECT id_admin FROM admin WHERE id_admin = {id_admin} untuk memeriksa apakah ID Admin yang dimasukkan ada di tabel admin.
  - Jika ID Admin tidak ditemukan, pesan "ID admin tidak ditemukan dalam database." akan dicetak dan fungsi akan dihentikan
- Fungsi membangun string query SQL UPDATE untuk memperbarui data proyek di tabel proyek.
  - Query menggunakan placeholder untuk memasukkan nilai-nilai baru yang diperoleh dari input pengguna.
- Query dijalankan menggunakan mycursor.execute(query).
- Fungsi memeriksa nilai mycursor.rowcount untuk mengetahui apakah data berhasil diperbarui.
  - Jika rowcount sama dengan 0, berarti tidak ada data yang diperbarui, dan pesan "ID Proyek tidak ditemukan." akan dicetak.
  - Jika rowcount lebih besar dari 0, berarti data berhasil diperbarui, dan pesan "Data berhasil diperbarui" akan dicetak.
- Terakhir, perubahan pada database dikomit menggunakan mydb.commit().
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
  - Blok except ValueError menangani pengecualian ValueError yang mungkin terjadi selama validasi input ID proyek, ID pemukiman, dan dana proyek.
  - Pesan informatif "Pastikan input berupa bilangan bulat untuk ID proyek, ID pemukiman, dan dana proyek." akan dicetak untuk membantu pengguna memahami jenis kesalahan yang terjadi.
  - Blok except Exception menangani semua jenis pengecualian lain yang mungkin terjadi.
  - Pesan generik "Terjadi kesalahan:", beserta objek pengecualian e akan dicetak untuk informasi lebih lanjut.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/28.png?raw=true)

- fungsi menu_utama_admin() ini dirancang untuk menampilkan menu utama bagi administrator database dan menangani pilihan pengguna.
- Fungsi menggunakan loop while True untuk menampilkan menu utama secara berulang sampai pengguna memilih untuk keluar.
- Di dalam loop, fungsi menggunakan perintah print untuk menampilkan teks yang membentuk menu utama, termasuk judul, pilihan yang tersedia, dan instruksi untuk memasukkan pilihan.
- Fungsi menggunakan variabel pilihan = input("Masukkan pilihan Anda: ") untuk menampung input pengguna.
- Pernyataan if bersarang digunakan untuk mengevaluasi pilihan pengguna dan menjalankan fungsi yang sesuai:
  - Jika pilihan == "1": Memanggil fungsi tambah_data_admin() untuk menambahkan data admin baru.
  - Jika pilihan == "2": Memanggil fungsi hapus_data_admin() untuk menghapus data admin.
  - Jika pilihan == "3": Memanggil fungsi perbarui_data_admin() untuk memperbarui data admin.
  - Jika pilihan == "4": Memanggil fungsi read_admin() untuk menampilkan data admin.
  - Jika pilihan == "5": Mencetak pesan "Terima kasih!" dan keluar dari loop while True, mengakhiri program.
  - Jika pilihan tidak valid (bukan salah satu opsi yang tersedia), pesan "Pilihan tidak valid. Silakan pilih kembali." akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
- Blok except (EOFError, KeyboardInterrupt) menangani dua jenis pengecualian:
  - EOFError: Muncul ketika pengguna menekan Ctrl+D (Windows) atau Ctrl+Z (Linux) untuk mengakhiri input.
  - KeyboardInterrupt: Muncul ketika pengguna menekan Ctrl+C (Windows/Linux) untuk menghentikan program secara paksa.
- Di dalam blok except, pesan "Program keluar." akan dicetak dan loop while True akan dihentikan, mengakhiri program.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/29.png?raw=true)

- Fungsi menu_utama_perkotaan() ini dirancang untuk menampilkan menu utama bagi pengelola database perkotaan dan menangani pilihan pengguna.
- Fungsi menggunakan loop while True untuk menampilkan menu utama secara berulang sampai pengguna memilih untuk keluar.
- Di dalam loop, fungsi menggunakan perintah print untuk menampilkan teks yang membentuk menu utama, termasuk judul, pilihan yang tersedia, dan instruksi untuk memasukkan pilihan.
- Fungsi menggunakan variabel pilihan = input("Masukkan pilihan Anda: ") untuk menampung input pengguna.
- Pernyataan if bersarang digunakan untuk mengevaluasi pilihan pengguna dan menjalankan fungsi yang sesuai:
  - Jika pilihan == "1": Memanggil fungsi tambah_data_perkotaan() untuk menambahkan data perkotaan baru.
  - Jika pilihan == "2": Memanggil fungsi hapus_data_perkotaan() untuk menghapus data perkotaan.
  - Jika pilihan == "3": Memanggil fungsi perbarui_data_perkotaan() untuk memperbarui data perkotaan.
  - Jika pilihan == "4": Memanggil fungsi read_perkotaan() untuk menampilkan data perkotaan.
  - Jika pilihan == "5": Mencetak pesan "Terima kasih!" dan keluar dari loop while True, mengakhiri program.
  - Jika pilihan tidak valid (bukan salah satu opsi yang tersedia), pesan "Pilihan tidak valid. Silakan pilih kembali." akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
- Blok except (EOFError, KeyboardInterrupt) menangani dua jenis pengecualian:
  - EOFError: Muncul ketika pengguna menekan Ctrl+D (Windows) atau Ctrl+Z (Linux) untuk mengakhiri input.
  - KeyboardInterrupt: Muncul ketika pengguna menekan Ctrl+C (Windows/Linux) untuk menghentikan program secara paksa.
- Di dalam blok except, pesan "Program keluar." akan dicetak dan loop while True akan dihentikan, mengakhiri program.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/30.png?raw=true)

- Fungsi menu_utama_pemukiman() dirancang untuk menampilkan menu utama bagi pengelola database pemukiman dan menangani pilihan pengguna.
- Fungsi menggunakan loop while True untuk menampilkan menu utama secara berulang sampai pengguna memilih untuk keluar.
- Di dalam loop, fungsi menggunakan perintah print untuk menampilkan teks yang membentuk menu utama, termasuk judul, pilihan yang tersedia, dan instruksi untuk memasukkan pilihan.
- Fungsi menggunakan variabel pilihan = input("Masukkan pilihan Anda: ") untuk menampung input pengguna.
- Pernyataan if bersarang digunakan untuk mengevaluasi pilihan pengguna dan menjalankan fungsi yang sesuai:
  - Jika pilihan == "1": Memanggil fungsi tambah_data_pemukiman() untuk menambahkan data pemukiman baru.
  - Jika pilihan == "2": Memanggil fungsi hapus_data_pemukiman() untuk menghapus data pemukiman.
  - Jika pilihan == "3": Memanggil fungsi perbarui_data_pemukiman() untuk memperbarui data pemukiman.
  - Jika pilihan == "4": Memanggil fungsi read_pemukiman() untuk menampilkan data pemukiman.
  - Jika pilihan == "5": Mencetak pesan "Terima kasih!" dan keluar dari loop while True, mengakhiri program.
  - Jika pilihan tidak valid (bukan salah satu opsi yang tersedia), pesan "Pilihan tidak valid. Silakan pilih kembali." akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
- Blok except (EOFError, KeyboardInterrupt) menangani dua jenis pengecualian:
  - EOFError: Muncul ketika pengguna menekan Ctrl+D (Windows) atau Ctrl+Z (Linux) untuk mengakhiri input.
  - KeyboardInterrupt: Muncul ketika pengguna menekan Ctrl+C (Windows/Linux) untuk menghentikan program secara paksa.
- Di dalam blok except, pesan "Program keluar." akan dicetak dan loop while True akan dihentikan, mengakhiri program.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/31.png?raw=true)

- Fungsi menu_utama_proyek() dirancang untuk menampilkan menu utama bagi pengelola database proyek dan menangani pilihan pengguna.
- Fungsi menggunakan loop while True untuk menampilkan menu utama secara berulang sampai pengguna memilih untuk keluar.
- Di dalam loop, fungsi menggunakan perintah print untuk menampilkan teks yang membentuk menu utama, termasuk judul, pilihan yang tersedia, dan instruksi untuk memasukkan pilihan.
- Fungsi menggunakan variabel pilihan = input("Masukkan pilihan Anda: ") untuk menampung input pengguna.
- Pernyataan if bersarang digunakan untuk mengevaluasi pilihan pengguna dan menjalankan fungsi yang sesuai:
  - Jika pilihan == "1": Memanggil fungsi tambah_data_proyek() untuk menambahkan data proyek baru.
  - Jika pilihan == "2": Memanggil fungsi hapus_data_proyek() untuk menghapus data proyek.
  - Jika pilihan == "3": Memanggil fungsi perbarui_data_proyek() untuk memperbarui data proyek.
  - Jika pilihan == "4": Memanggil fungsi read_proyek() untuk menampilkan data proyek.
  - Jika pilihan == "5": Mencetak pesan "Terima kasih!" dan keluar dari loop while True, mengakhiri program.
  - Jika pilihan tidak valid (bukan salah satu opsi yang tersedia), pesan "Pilihan tidak valid. Silakan pilih kembali." akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
- Blok except (EOFError, KeyboardInterrupt) menangani dua jenis pengecualian:
  - EOFError: Muncul ketika pengguna menekan Ctrl+D (Windows) atau Ctrl+Z (Linux) untuk mengakhiri input.
  - KeyboardInterrupt: Muncul ketika pengguna menekan Ctrl+C (Windows/Linux) untuk menghentikan program secara paksa.
- Di dalam blok except, pesan "Program keluar." akan dicetak dan loop while True akan dihentikan, mengakhiri program.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/32.png?raw=true)

- Fungsi menu_utama_SUPER_ADMIN() dirancang untuk menyediakan antarmuka bagi SUPER_ADMIN untuk mengelola berbagai database dalam aplikasi.
- Fungsi menggunakan loop while True untuk menampilkan menu utama secara berulang sampai SUPER_ADMIN memilih untuk keluar.
- Di dalam loop, fungsi menggunakan perintah print untuk menampilkan teks yang membentuk menu utama, termasuk:
  - Ucapan selamat datang dengan nama pengguna SUPER_ADMIN.
  - Judul menu.
  - Daftar pilihan menu (database admin, database perkotaan, database pemukiman, database proyek, dan keluar).
  - Instruksi untuk memasukkan pilihan.
- Fungsi menggunakan variabel pilihan = input("Masukkan pilihan Anda: ") untuk menampung input SUPER_ADMIN.
- Pernyataan if bersarang digunakan untuk mengevaluasi pilihan SUPER_ADMIN dan menjalankan fungsi yang sesuai:
  - Jika pilihan == "1": Memanggil fungsi menu_utama_admin() untuk menampilkan menu admin dan menangani pilihan terkait pengelolaan data admin.
  - Jika pilihan == "2": Memanggil fungsi menu_utama_perkotaan() untuk menampilkan menu perkotaan dan menangani pilihan terkait pengelolaan data perkotaan.
  - Jika pilihan == "3": Memanggil fungsi menu_utama_pemukiman() untuk menampilkan menu pemukiman dan menangani pilihan terkait pengelolaan data pemukiman.
  - Jika pilihan == "4": Memanggil fungsi menu_utama_proyek() untuk menampilkan menu proyek dan menangani pilihan terkait pengelolaan data proyek.
  - Jika pilihan == "5": Mencetak pesan "Terima kasih!" dan keluar dari loop while True, mengakhiri program.
  - Jika pilihan tidak valid (bukan salah satu opsi yang tersedia), pesan "Pilihan tidak valid. Silakan pilih kembali." akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
- Blok except (EOFError, KeyboardInterrupt) menangani dua jenis pengecualian:
  - EOFError: Muncul ketika SUPER_ADMIN menekan Ctrl+D (Windows) atau Ctrl+Z (Linux) untuk mengakhiri input.
  - KeyboardInterrupt: Muncul ketika SUPER_ADMIN menekan Ctrl+C (Windows/Linux) untuk menghentikan program secara paksa.
- Di dalam blok except, pesan "Program keluar." akan dicetak dan loop while True akan dihentikan, mengakhiri program.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/33.png?raw=true)

- Fungsi menu_user() dirancang untuk menyediakan antarmuka bagi pengguna aplikasi untuk mengakses dan melihat data dari berbagai database.
- Fungsi menggunakan loop while True untuk menampilkan menu utama secara berulang sampai pengguna memilih untuk keluar.
- Di dalam loop, fungsi menggunakan perintah print untuk menampilkan teks yang membentuk menu utama, termasuk:
  - Ucapan selamat datang dengan nama pengguna.
  - Judul menu.
  - Daftar pilihan menu (database perkotaan, database pemukiman, database proyek, dan keluar).
  - Instruksi untuk memasukkan pilihan.
- Fungsi menggunakan variabel pilihan = input("Masukkan pilihan Anda: ") untuk menampung input pengguna.
- Pernyataan if bersarang digunakan untuk mengevaluasi pilihan pengguna dan menjalankan fungsi yang sesuai:
  - jika pilihan == "1": Memanggil fungsi read_perkotaan() untuk menampilkan data dari database perkotaan.
  - Jika pilihan == "2": Memanggil fungsi read_pemukiman() untuk menampilkan data dari database pemukiman.
  - Jika pilihan == "3": Memanggil fungsi read_proyek() untuk menampilkan data dari database proyek.
  - Jika pilihan == "4": Mencetak pesan "Terima kasih!" dan keluar dari loop while True, mengakhiri program.
  - Jika pilihan tidak valid (bukan salah satu opsi yang tersedia), pesan "Pilihan tidak valid. Silakan pilih kembali." akan dicetak.
- Blok try digunakan untuk membungkus bagian kode yang berpotensi menimbulkan kesalahan.
- Blok except (EOFError, KeyboardInterrupt) menangani dua jenis pengecualian:
  - EOFError: Muncul ketika pengguna menekan Ctrl+D (Windows) atau Ctrl+Z (Linux) untuk mengakhiri input.
  - KeyboardInterrupt: Muncul ketika pengguna menekan Ctrl+C (Windows/Linux) untuk menghentikan program secara paksa.
- Di dalam blok except, pesan "Program keluar." akan dicetak dan loop while True akan dihentikan, mengakhiri program.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/34.png?raw=true)

- Kelas Login ini dirancang untuk menangani proses login pengguna dalam aplikasi Anda.
- mycursor:
  - Merupakan objek kursor yang kemungkinan terhubung ke database Anda.
  - Objek kursor ini digunakan untuk menjalankan query ke database dan mengambil hasil.
- users:
  - Merupakan kamus (dictionary) kosong yang kemungkinan akan diisi dengan informasi pengguna yang valid.
- Metode __init__ adalah konstruktor untuk kelas Login.
- Konstruktor dipanggil ketika objek Login dibuat.
- Konstruktor ini mengambil dua argumen:
  - mycursor: Objek kursor yang terhubung ke database.
  - users: Kamus kosong yang akan digunakan untuk menyimpan informasi pengguna.
- Di dalam konstruktor, argumen mycursor disimpan ke atribut self.mycursor dan argumen users disimpan ke atribut self.users.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/35.png?raw=true)

- Fungsi register() pada kelas Login dirancang untuk mendaftarkan pengguna baru ke dalam aplikasi
- Fungsi register menerima dua argumen: username dan password.
- Pertama, fungsi mencoba memeriksa apakah username yang diberikan sudah ada di kamus self.users menggunakan operator in.
  - Jika username sudah ada, fungsi akan:
  - Membangkitkan pengecualian ValueError dengan pesan "Username sudah ada. Silakan pilih username lain."
  - Pernyataan raise akan menghentikan fungsi dan mengembalikan kontrol ke blok except.
  - Jika username belum ada, fungsi akan beralih ke langkah selanjutnya.
- Jika username belum ada, fungsi akan membuat entri baru di kamus self.users dengan kunci username dan nilai password.
- Ini berarti informasi login pengguna (username dan password) disimpan dalam kamus self.users.
- Fungsi kemudian mencetak pesan "Pendaftaran berhasil. Silakan login dengan akun baru Anda." untuk memberi tahu pengguna bahwa proses pendaftaran telah berhasil.
- Jika username belum ada, fungsi akan membuat entri baru di kamus self.users dengan kunci username dan nilai password.
- Ini berarti informasi login pengguna (username dan password) disimpan dalam kamus self.users.
- Fungsi kemudian mencetak pesan "Pendaftaran berhasil. Silakan login dengan akun baru Anda." untuk memberi tahu pengguna bahwa proses pendaftaran telah berhasil.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/36.png?raw=true)

- Fungsi login() pada kelas Login dirancang untuk mengotentikasi pengguna dan memberikan akses ke menu yang sesuai berdasarkan peran pengguna.
- Fungsi login menerima dua argumen: username dan password.
- Di dalam blok try, fungsi menggunakan objek self.mycursor untuk menjalankan query SQL berikut:
  - SELECT * FROM admin WHERE \Nama_Admin` = '{username}' AND `Password_Admin` = '{password}'`
- Query ini memilih semua data (*) dari tabel admin di mana kolom Nama_Admin sama dengan username yang diberikan dan kolom Password_Admin sama dengan password yang diberikan.
- Hasil query disimpan dalam variabel admin.
- Jika variabel admin berisi nilai (artinya query berhasil menemukan data yang cocok dengan username dan password yang diberikan), fungsi akan:
  - Mencetak pesan "Login berhasil."
  - Mengambil nilai dari kolom ke-5 hasil query (indeks 4 dalam Python) dan menyimpannya dalam variabel role. Nilai ini mewakili peran pengguna yang login.
  - Memanggil fungsi menu yang sesuai berdasarkan nilai role:
  - Jika role == "super admin database": Memanggil fungsi menu_utama_SUPER_ADMIN().
  - Jika role == "perkotaan_database": Memanggil fungsi menu_utama_perkotaan().
  - Jika role == "pemukiman_database": Memanggil fungsi menu_utama_pemukiman().
  - Jika role == "pemukiman_database": Memanggil fungsi menu_utama_proyek().
  - Jika role tidak sama dengan salah satu nilai yang valid, fungsi akan mencetak pesan "Role tidak valid."
- Jika variabel admin kosong (artinya query tidak menemukan data yang cocok), fungsi akan:
  - Memeriksa apakah username ada di kamus self.users.
  - Jika username ada di kamus:
  - Membandingkan nilai password yang diberikan dengan nilai password yang disimpan dalam kamus untuk username tersebut.
  - Jika password cocok, fungsi akan:
  - Mencetak pesan "Login berhasil."
  - Memanggil fungsi menu_user().
  - Jika password tidak cocok, fungsi akan:
  - Membangkitkan pengecualian ValueError dengan pesan "Password pengguna salah. Silakan coba lagi."
  - Jika username tidak ada di kamus, fungsi akan:
  - Membangkitkan pengecualian ValueError dengan pesan "Username tidak ditemukan."
- Blok except digunakan untuk menangkap pengecualian ValueError yang mungkin dibangkitkan dalam blok try.
- Jika pengecualian ValueError tertangkap, fungsi akan mencetak pesan kesalahan yang terkait dengan pengecualian tersebut (dalam kasus ini, "Password pengguna salah. Silakan coba lagi." atau "Username tidak ditemukan.").
- login: Ini adalah nama variabel yang akan menyimpan hasil dari sebuah pemanggilan fungsi. Kemungkinan besar variabel ini akan menyimpan jenis objek yang terkait dengan proses login.
- Login(mycursor): Ini adalah pemanggilan fungsi.
  - Login: Ini adalah nama fungsi yang dipanggil. Fungsi ini kemungkinan didefinisikan di bagian lain kode dan menangani logika login.
  - mycursor: Ini adalah argumen yang dilewatkan ke fungsi Login. Berdasarkan namanya, kemungkinan besar ini adalah objek kursor basis data. Objek kursor ini mungkin digunakan oleh fungsi Login untuk berinteraksi dengan basis data untuk keperluan login.

![alt text](https://github.com/MuhammadLuqmanSi/PA-B23-KELOMPOK-2/blob/master/37.png?raw=true)

- Loop while True memastikan program berjalan terus menerus hingga pengguna memilih untuk keluar.
- Pernyataan print membuat header menu, opsi, dan garis pemisah.
- input("Pilih menu: ") meminta pengguna untuk memasukkan pilihan mereka.
- if choice == "1":
  - username = input("Masukkan username: ") meminta username pengguna.
  - password = getpass.getpass("Masukkan password: ") meminta password dengan aman.
  - login.login(username, password) memanggil fungsi login untuk mengotentikasi pengguna.
- elif choice == "2":
  - username = input("Masukkan username baru: ") meminta username baru.
  - password = getpass.getpass("Masukkan password baru: ") meminta password baru dengan aman.
  - login.register(username, password) memanggil fungsi register untuk membuat akun baru.
- elif choice == "3":
  - print("Terima kasih!") menampilkan pesan terima kasih.
  - break keluar dari loop utama, mengakhiri program.
- else:
  - print("Pilihan tidak valid. Silakan pilih kembali.") menampilkan pesan kesalahan untuk pilihan yang tidak valid.
- Blok try...except menangani potensi kesalahan selama input pengguna atau eksekusi program.
- EOFError dan KeyboardInterrupt ditangkap masing-masing untuk akhir file dan interupsi keyboard.
- print("Program keluar.") menampilkan pesan penutup.
- break keluar dari loop utama, mengakhiri program.
