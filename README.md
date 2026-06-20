# Laporan Analisis Perancangan Berorientasi Objek - Kelompok 1

## Anggota Kelompok
| **Nama** | **NPM** |
| :--- | :--- |
| Chandra Cornelius L Tobing | 4524210022 |
| Andika Prasetyo | 4524210013 |
| Damar Syeka | 4524210023 |

<br>

# Informasi dan Ruang Lingkup Proyek

## Topik dan Judul Proyek
* **Topik:** Bisnis – Manajemen Kost
* **Judul Project:** **Sistem Manajemen Kost** Aplikasi Pengelolaan Kost Berbasis Web dengan Fitur Notifikasi dan Pelacakan Pembayaran

## Sasaran Pengguna (Aktor)
Sistem Manajemen Kost ini dirancang untuk mempermudah komunikasi dan proses administrasi antara pihak pengelola dan penyewa kamar. Di dalam sistem ini, terdapat tiga peran utama yang terlibat:

* **Penjaga atau Admin Kost:** Merupakan pihak yang bertugas mengurus operasional sehari-hari di lokasi kost. Admin memiliki akses untuk melakukan pendataan ketika ada penghuni baru yang masuk, memantau kamar mana saja yang sedang kosong atau terisi, melakukan verifikasi terhadap status pembayaran bulanan, serta mengelola hal-hal terkait fasilitas dan kebersihan.
* **Penghuni (Penyewa):** Merupakan target pengguna utama dari aplikasi ini, yang sebagian besar terdiri dari mahasiswa atau pekerja kantoran. Penghuni akan diberikan akses ke dalam sistem untuk mengisi dan mengunggah biodata diri, melihat rincian tagihan setiap bulannya, melakukan proses pembayaran secara langsung melalui platform, serta menerima pengingat apabila tenggat waktu pembayaran sudah dekat.
* **Pemilik Kost (Owner):** Merupakan pemilik bisnis yang mungkin tidak selalu berada di lokasi kost. Melalui sistem ini, pemilik dapat dengan mudah memantau jalannya bisnis, seperti melihat laporan rekapitulasi pendapatan setiap bulan, memantau daftar penghuni yang mengalami keterlambatan pembayaran, dan mengecek status okupansi kamar tanpa harus menanyakan laporan teknis kepada penjaga kost secara terus-menerus.

---

## Hasil Wawancara Pengelolaan Kost Saat Ini
Berdasarkan hasil observasi langsung dan wawancara yang kami lakukan dengan pihak pengelola kost, berikut adalah rangkuman mengenai prosedur operasional yang saat ini masih berjalan:

<details>
<summary><b>Bagian 1: Pengelolaan Data Penghuni dan Tugas Harian</b></summary>

<br>

**Q: Siapa saja yang terlibat dalam pengelolaan kost ini dan apa saja kegiatan utamanya setiap hari?**
> Pengelolaan kost ini pada dasarnya melibatkan dua pihak utama, yaitu pemilik kost dan penjaga kost yang bertindak sebagai admin. Untuk kegiatan sehari-harinya, penjaga kost rutin melakukan pendataan jika ada penghuni yang baru masuk, mengecek kondisi kamar-kamar, serta memastikan kebersihan di setiap area dan lorong kost tetap terjaga.

**Q: Bagaimana cara pihak pengelola mencatat data penghuni kost saat ini?**
> Untuk keperluan pemasaran dan mencari penyewa baru, pengelola sudah memanfaatkan aplikasi pihak ketiga seperti Mamikos. Namun, ketika penghuni sudah resmi masuk, pendataan administrasinya masih mengandalkan cara manual (dicatat di buku). Hal ini sering menjadi masalah, terutama ketika pihak RT atau RW setempat meminta laporan data penduduk sementara. Admin sering kali lupa mencatat atau kehilangan kertas datanya karena belum ada sistem penyimpanan digital yang terpusat.

</details>

<details>
<summary><b>Bagian 2: Sistem Pembayaran dan Kendala di Lapangan</b></summary>

<br>

**Q: Bagaimana mekanisme pembayaran kost bulanan yang diterapkan saat ini?**
> Mayoritas penghuni melakukan pembayaran sewa kamar melalui metode transfer bank. Walaupun begitu, pengelola juga masih menerima pembayaran menggunakan uang tunai secara langsung bagi anak-anak kost yang lebih memilih metode tersebut.

**Q: Apakah sering terjadi kasus keterlambatan pembayaran sewa?**
> Kejadian keterlambatan pembayaran bisa dibilang cukup sering terjadi. Hal ini wajar mengingat rata-rata penghuni di sini adalah mahasiswa. Mereka biasanya harus menunggu kiriman uang bulanan dari orang tua masing-masing di kampung halaman, sehingga jadwal pembayarannya sering kali meleset dari tanggal jatuh tempo.

**Q: Apa saja kendala terbesar yang dirasakan dalam mengelola bisnis kosan ini?**
> Kendala yang paling terasa ada pada aspek pemasaran dan letak geografis. Lokasi bangunan kost ini berada cukup dalam di area gang, sehingga sangat menyulitkan jika ada penghuni yang membawa kendaraan roda empat (mobil). Posisi di dalam gang ini juga membuat bangunan kost kurang terlihat dari jalan utama, sehingga mengurangi jangkauan visibilitas bagi calon penyewa baru.

</details>

<details>
<summary><b>Bagian 3: Harapan Terhadap Pengembangan Sistem</b></summary>

<br>

**Q: Jika nantinya ada sebuah sistem manajemen digital yang dibangun, fitur apa yang paling diharapkan?**
> Harapan terbesar dari pengelola adalah terciptanya efisiensi dalam alur pembayaran bulanan. Pihak pengelola ingin agar penghuni tidak perlu lagi repot-repot mengirim pesan konfirmasi transfer (mengirim bukti struk) secara manual melalui WhatsApp kepada admin. Sistem diharapkan mampu memproses pembayaran secara otomatis, misalnya dengan menyediakan opsi pembayaran melalui QRIS atau Virtual Account. Selain itu, diharapkan ada fitur notifikasi yang bisa langsung memberitahukan kepada pemilik kost apabila ada pembayaran yang masuk. Sistem juga diharapkan memiliki kemampuan untuk mengarsip biodata diri penghuni serta merinci tagihan secara otomatis.

</details>

<br>

# Latar Belakang dan Rumusan Masalah
Dari hasil observasi tersebut, kami menyimpulkan bahwa pengelolaan operasional kost saat ini masih memiliki banyak celah administratif. Hal-hal yang masih dikerjakan secara manual ini sangat menghambat efisiensi waktu dan tenaga. Beberapa masalah utama yang kami temukan antara lain:

1. **Konfirmasi Pembayaran yang Masih Manual:** Saat ini, setelah mentransfer uang, penghuni harus mengirimkan tangkapan layar (screenshot) bukti transfer melalui obrolan WhatsApp kepada penjaga atau pemilik kost. Proses ini memiliki risiko tinggi di mana pesan bisa tertumpuk, terlewat, atau terlupa untuk dicatat ke dalam pembukuan.
2. **Keterlambatan Pembayaran Akibat Tidak Adanya Pengingat:** Banyak mahasiswa yang sering terlambat membayar uang sewa. Karena belum ada sistem yang bisa mengirimkan notifikasi peringatan secara otomatis, penjaga kost sering kali harus menagih secara langsung dari pintu ke pintu, yang mana terkadang menimbulkan rasa tidak enak atau sungkan.
3. **Data Administrasi Penghuni yang Sering Tercecer:** Proses pengumpulan data diri penyewa, seperti fotokopi KTP untuk keperluan pelaporan ke pihak lingkungan (RT/RW), masih mengandalkan pencatatan manual. Data ini rawan hilang, terselip, atau bahkan terlupa untuk dikumpulkan oleh penjaga kost di awal masa sewa.
4. **Kesulitan dalam Memantau Ketersediaan Kamar:** Pihak pemilik atau pengelola kesulitan untuk mengetahui status kamar (kamar mana yang kosong, terisi, atau sedang direnovasi) secara tepat waktu (real-time). Mereka sering kali hanya mengandalkan ingatan atau harus mengecek kembali ke catatan kertas yang bisa saja tidak akurat.

---

# Solusi dan Perbandingan Prosedur Operasional (SOP)

Untuk mengatasi permasalahan di atas, kami mengusulkan pembangunan sebuah sistem berbasis web. Sistem ini akan mengubah alur kerja yang sebelumnya serba manual menjadi serba digital. Pendekatannya adalah memberikan keleluasaan bagi penghuni untuk mengurus administrasinya sendiri (self-service), dan memberikan sebuah halaman dasbor bagi pengelola untuk memantau semuanya secara mudah.

## Analisis Perbandingan SOP (Sebelum dan Sesudah Implementasi Sistem)

<details>
<summary><b>1. Proses Pendataan Penghuni Baru</b></summary><br>

* **Sebelum Menggunakan Sistem (Manual):** Penjaga kost harus meminta identitas KTP secara langsung bertatap muka atau meminta penghuni mengirimkannya lewat obrolan WhatsApp. Setelah itu, penjaga harus menyalin data tersebut secara manual ke dalam buku tulis untuk nantinya dilaporkan kepada pengurus RT/RW. Proses ini sering kali membuat admin lupa untuk mencatat.
* **Setelah Menggunakan Sistem:** Penghuni baru yang akan masuk diwajibkan untuk mengunggah biodata lengkap beserta foto KTP secara mandiri melalui formulir digital (E-Form) yang ada di dalam aplikasi. Kunci kamar baru akan diserahkan jika formulir ini sudah diisi. Semua data akan langsung tersimpan dengan aman dan rapi di dalam pangkalan data (database) sistem.
</details>

<details>
<summary><b>2. Proses Pembayaran Sewa Bulanan</b></summary><br>

* **Sebelum Menggunakan Sistem (Manual):** Alurnya sangat panjang. Penghuni mentransfer uang, kemudian mengambil tangkapan layar bukti transfer, lalu mengirimkannya melalui WhatsApp kepada admin. Setelah itu, admin harus mencatat transaksi tersebut di buku besar, dan terakhir admin harus melaporkan pemasukan tersebut kepada pemilik kost secara berkala.
* **Setelah Menggunakan Sistem:** Penghuni hanya perlu masuk (login) ke dalam aplikasi dan melihat rincian tagihan bulanannya. Penghuni bisa langsung melakukan pembayaran dan mengunggah buktinya di sana, atau menggunakan metode pembayaran digital yang terintegrasi (seperti QRIS). Setelah divalidasi, sistem akan mengubah status tagihannya menjadi "Lunas" secara otomatis. Pemilik dan admin bisa langsung melihat pembaruan data pendapatan tersebut pada detik itu juga.
</details>

<details>
<summary><b>3. Penanganan Jatuh Tempo dan Keterlambatan</b></summary><br>

* **Sebelum Menggunakan Sistem (Manual):** Admin kost harus mengingat-ingat atau membuka buku catatan satu per satu untuk mencari tahu siapa saja penghuni yang belum membayar bulan ini. Setelah itu, admin harus mengetuk pintu kamar mereka satu per satu atau mengirimkan pesan WhatsApp untuk menagih.
* **Setelah Menggunakan Sistem:** Sistem akan dilengkapi dengan fitur pengingat otomatis. Pada waktu tiga hari sebelum tanggal jatuh tempo, dan tepat pada hari batas pembayaran, sistem akan otomatis mengirimkan pemberitahuan tagihan langsung ke akun dasbor penghuni yang bersangkutan, sehingga admin tidak perlu lagi menagih secara manual.
</details>

---

# Use Case Sistem

## Ringkasan Aktor dan Tujuan

| Aktor | Tujuan Utama | Skenario Tindakan yang Dilakukan |
| :--- | :--- | :--- |
| **Admin** | **Melakukan Manajemen Kamar** | Admin dapat memperbarui status setiap kamar di dalam aplikasi, misalnya mengubah status menjadi Kosong, Terisi, atau Sedang Dalam Perbaikan. |
| | **Melakukan Validasi Data** | Admin dapat memeriksa kembali kelengkapan dan keabsahan dokumen biodata yang diunggah oleh penghuni, yang nantinya berguna untuk pelaporan ke RT/RW. |
| | **Mengecek Status Pembayaran** | Admin bertugas memverifikasi apabila ada pembayaran yang dilakukan secara tunai atau transfer manual, serta mencetak laporan jika dibutuhkan. |
| **Penghuni** | **Mengakses Informasi Pribadi** | Penghuni dapat masuk ke aplikasi untuk melihat sisa durasi sewa kamar mereka, mengecek rincian tagihan bulan ini, serta melihat rekam jejak pembayaran bulan-bulan sebelumnya. |
| | **Melakukan Pembayaran Digital** | Penghuni dapat menyelesaikan proses pembayaran tagihan secara mandiri melalui antarmuka sistem tanpa harus menghubungi admin. |
| **Pemilik Kost**| **Memantau Kondisi Bisnis** | Pemilik dapat masuk ke sistem untuk melihat rekapitulasi total pendapatan bulanan secara transparan dan mengecek daftar penghuni mana saja yang sedang menunggak pembayaran. |

## Detail Skenario Use Case

### A. Registrasi dan Pendataan Penghuni Baru
**Aktor yang Terlibat:** Penghuni dan Admin
1. Langkah pertama, admin akan membuatkan akun sementara yang ditautkan dengan nomor kamar yang akan disewa oleh penghuni baru tersebut.
2. Selanjutnya, penghuni masuk (login) ke aplikasi untuk pertama kalinya. Sistem akan memaksa penghuni untuk melengkapi formulir biodata diri yang mencakup unggahan KTP, nomor kontak darurat, serta informasi pekerjaan atau kampus.
3. Setelah diserahkan, sistem akan menyimpan seluruh data tersebut secara terpusat di dalam database.
4. Di kemudian hari, apabila pihak RT atau RW meminta laporan mengenai data penduduk musiman, admin dapat dengan mudah mengunduh rekapitulasi data tersebut dari dalam sistem untuk dicetak.

### B. Proses Pelacakan Pembayaran dan Konfirmasi Otomatis
**Aktor yang Terlibat:** Penghuni dan Pemilik Kost
1. Secara otomatis, sistem akan menerbitkan surat tagihan bulanan pada halaman dasbor milik penghuni, tepatnya pada tujuh hari sebelum tanggal jatuh tempo sewa mereka.
2. Penghuni kemudian memilih metode pembayaran yang tersedia dan memproses transaksinya (misalnya dengan mengunggah gambar bukti transfer atau melakukan pindai QRIS).
3. Sistem akan melakukan validasi terhadap pembayaran tersebut. Jika sesuai, sistem akan segera mengubah status tagihan penghuni dari yang sebelumnya belum dibayar menjadi "Lunas".
4. Dengan alur ini, sistem memotong keharusan penghuni untuk mengirimkan pesan konfirmasi manual kepada admin. Seluruh data keuangan akan langsung diperbarui dan ditampilkan di halaman dasbor milik Admin dan Pemilik Kost secara seketika.

### C. Sistem Notifikasi Peringatan Keterlambatan
**Aktor yang Terlibat:** Sistem
1. Setiap harinya, sistem dirancang untuk melakukan pengecekan ke dalam database secara otomatis di latar belakang.
2. Apabila sistem menemukan bahwa tanggal hari ini sudah melewati batas waktu jatuh tempo penyewaan dan status tagihan masih tercatat sebagai "Belum Lunas", maka sistem akan secara otomatis memberikan penanda berwarna merah (status Terlambat) pada data tersebut.
3. Sebagai tindak lanjutnya, sistem akan mengirimkan pesan pengingat berupa peringatan keterlambatan pembayaran secara langsung ke dalam akun aplikasi milik penghuni.

### Diagram Use Case
![Diagram Use Case Sistem Manajemen Kost](USECASE_DIAGRAM.png)

---

## Target Hasil Akhir yang Diharapkan
* **Bagi Pihak Pengelola (Admin):** Sistem ini sangat diharapkan mampu menghilangkan beban kerja berat terkait penagihan pembayaran yang harus dilakukan dari kamar ke kamar, serta meminimalisir kesalahan atau kehilangan data dalam proses pencatatan administrasi.
* **Bagi Pihak Penghuni:** Sistem ini bertujuan untuk memberikan pengalaman pelayanan yang lebih modern dan praktis. Penghuni dapat melakukan pembayaran dengan lancar, memiliki rekam jejak keuangan yang terdata dengan rapi, dan mendapatkan transparansi tagihan.
* **Bagi Pemilik Kost:** Melalui implementasi sistem ini, pemilik akan mendapatkan akses terhadap laporan keuangan dan tingkat hunian bulanan yang sangat akurat, berjalan secara otomatis, dan memiliki tingkat kesalahan manusia (human-error) yang sangat minim.

---

## Tautan Video Dokumentasi
https://youtu.be/YygnO0hJeKc?si=Hsz79v9YUS0XCvSs
