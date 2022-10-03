**Ana Maria Parasanti - 2110131320009**

---

### Perbedaan Struktur Sistem Operasi Sederhana, Berlapis, dan Kernel

1. Struktur Sistem Operasi Sederhana

    System monolitik ini berisikan kumpulan dari berbagai prosedur yang dapat dipanggil oleh persedur lainnya untuk menjalankan sistem. Sehingga antar prosedur dapat saling bekerja sama dalam menjalankan sebuah sistem.

    Sistem operasi sebagai kumpulan prosedur dimana prosedur dapat saling dipanggil oleh prosedur lain di sistem bila diperlukan. Banyak sistem operasi komersial yang tidak terstruktur dengan baik. Kemudian sistem operasi dimulai dari yang terkecil, sederhana dan terbatas lalu berkembang dengan ruang lingkup originalnya. Berikut contoh penerapan dari struktur sistem operasi monolitik/sederhana:

    + Gambar struktur lapisan pada MS-DOS:

        <img width="224" src="https://user-images.githubusercontent.com/112605121/193626728-5ae40017-7420-42f2-ae82-e45393351c71.PNG">

        Di MS-DOS, antarmuka dan tingkat fungsionalitas tidak dipisahkan dengan baik. Misalnya, program aplikasi dapat mengakses rutinitas I/O dasar untuk menulis langsung ke layar dan drive disk. Kebebasan seperti itu membuat MS-DOS rentan terhadap program yang salah (atau berbahaya), menyebabkan seluruh sistem crash ketika program pengguna gagal. Tentu saja, MS-DOS juga dibatasi oleh perangkat keras pada zamannya. 

    + Gambar struktur sistem pada UNIX tradisional:

        <img width="373" src="https://user-images.githubusercontent.com/112605121/193626979-77ec153f-0e75-4e27-ac8f-8059676f2b11.PNG">

        Contoh lain dari penataan terbatas adalah sistem operasi UNIX asli. Seperti MS-DOS, UNIX awalnya dibatasi oleh fungsionalitas perangkat keras. Ini terdiri dari dua bagian yang dapat dipisahkan: kernel dan program sistem. Kernel selanjutnya dipisahkan menjadi serangkaian antarmuka dan driver perangkat, yang telah ditambahkan dan diperluas selama bertahun-tahun seiring berkembangnya UNIX. Kita dapat melihat sistem operasi UNIX tradisional sebagai berlapis sampai batas tertentu, seperti yang ditunjukkan pada gambar diatas. 
        
        Segala sesuatu di bawah antarmuka panggilan sistem dan di atas perangkat keras fisik adalah kernel. Kernel menyediakan sistem file, penjadwalan CPU, manajemen memori, dan fungsi sistem operasi lainnya melalui panggilan sistem. Singkatnya, itu adalah sejumlah besar fungsi untuk digabungkan menjadi satu tingkat. Struktur monolitik ini sulit untuk diterapkan dan dipelihara. Namun, ia memiliki keunggulan kinerja yang berbeda: hanya ada sedikit overhead di antarmuka panggilan sistem atau dalam komunikasi di dalam kernel.


    

2. Struktur Sistem Operasi Berlapis

    Salah satu metode adalah pendekatan berlapis, di mana sistem operasi dipecah menjadi beberapa lapisan (level). Lapisan bawah (lapisan 0) adalah perangkat keras; yang tertinggi (lapisan N) adalah antarmuka pengguna. Struktur layering ini digambarkan pada gambar dibawah ini.

    <img width="231" src="https://user-images.githubusercontent.com/112605121/193627033-3c7fb6e6-b07d-42d6-bfd6-332cc672adf4.PNG">

    Lapisan sistem operasi yang khas—misalnya, lapisan M—terdiri dari struktur data dan serangkaian rutinitas yang dapat dipanggil oleh lapisan tingkat yang lebih tinggi. Lapisan M, pada gilirannya, dapat menjalankan operasi pada lapisan tingkat yang lebih rendah. Keuntungan utama dari pendekatan berlapis adalah kesederhanaan konstruksi dan debugging.

    Keuntungan:

    + kesederhanaan konstruksi dan debugging.

        Lapisan dipilih sehingga masing-masing menggunakan fungsi (operasi) dan layanan hanya lapisan tingkat yang lebih rendah. Pendekatan ini menyederhanakan debugging dan verifikasi sistem.

    Kekurangan:

    + Perlu untuk mendefinisikan lapisan-lapisan tersebut

        Karena sebuah lapisan hanya dapat menggunakan lapisan tingkat yang lebih rendah, sehingga perencanaan yang cermat diperlukan. Misalnya, driver perangkat untuk penyimpanan cadangan (ruang disk yang digunakan oleh algoritme memori virtual) harus berada pada tingkat yang lebih rendah daripada rutinitas manajemen memori, karena manajemen memori memerlukan kemampuan untuk menggunakan penyimpanan cadangan.
    
    + Cenderung kurang efisien daripada jenis lainnya.
    
        Hal ini dikarenakan Hasil akhirnya dari panggilan sistem membutuhkan waktu lebih lama daripada yang dilakukan pada sistem tidak berlapis.

3. Struktur Sistem Operasi Kernel

   Metode struktur ini adalah menghilangkan komponen-komponen yang tidak diperlukan dari kernel dan mengimplementasikannya sebagai sistem dan program-program level user. Hal ini akan menghasilkan kernel yang kecil. Fungsi utama dari jenis ini adalah menyediakan fasilitas komunikasi antara program client dan bermacam pelayanan yang berjalan pada ruang user. Gambar dibawah ini mengilustrasikan arsitektur tipikal mikrokernel.

    <img width="322" src="https://user-images.githubusercontent.com/112605121/193627137-b5586bf4-60f6-47e8-aa2b-7dfb88c07c9f.PNG">

    Fungsi utama dari mikrokernel adalah untuk menyediakan komunikasi antara program klien dan berbagai layanan yang juga berjalan di ruang pengguna. Komunikasi dilakukan melalui penyampaian pesan. Misalnya, jika program klien ingin mengakses file, ia harus berinteraksi dengan server file. Program dan layanan klien tidak pernah berinteraksi secara langsung. Sebaliknya, mereka berkomunikasi secara tidak langsung dengan bertukar pesan dengan mikrokernel.

    Keuntungan:

    + Membuat perluasan sistem operasi menjadi lebih mudah.

        Semua layanan baru ditambahkan ke ruang pengguna dan akibatnya tidak memerlukan modifikasi kernel. Ketika kernel memang harus dimodifikasi, perubahannya cenderung lebih sedikit, karena mikrokernel adalah kernel yang lebih kecil.
        
    + Sistem operasi yang dihasilkan lebih mudah untuk dipindahkan dari satu desain perangkat keras ke desain perangkat keras lainnya.

    + Memberikan lebih banyak keamanan dan keandalan

        Hal ini dikarenakan sebagian besar layanan berjalan sebagai proses pengguna—bukan kernel. Jika layanan gagal, sisa sistem operasi tetap tidak tersentuh.

    Kekurangan:

    + kinerja mikrokernel dapat menurun karena peningkatan overhead fungsi sistem.
---
