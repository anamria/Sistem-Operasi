**Ana Maria Parasanti - 2110131320009**

---

### Perbedaan Struktur Sistem Operasi Sederhana, Berlapis, dan Kernel

1. Struktur Sistem Operasi Sederhana

    System monolitik ini berisikan kumpulan dari berbagai prosedur yang dapat dipanggil oleh persedur lainnya untuk menjalankan sistem. 
    Sehingga antar prosedur dapat saling bekerja sama dalam menjalankan sebuah sistem. Banyak sistem operasi komersial yang tidak 
    terstruktur dengan baik. Kemudian sistem operasi dimulai dari yang terkecil, sederhana dan terbatas lalu berkembang dengan ruang lingkup 
    originalnya.
    
    Struktur sistem operasi ini dilengkapi dengan operasi “dual” pelayanan {sistem call} yang diberikan oleh sistem operasi. Model 
    sistem call dilakukan dengan cara mengambil sejumlah parameter pada tempat yang telah ditentukan sebelumnya, seperti register atau stack 
    dan kemudian mengeksekusi suatu intruksi trap tertentu pada monitor mod.

    Berikut gambar struktur sister operasi sederhana:
    
    <p>
    <img width="200px" src="https://user-images.githubusercontent.com/112605121/192242903-b89b98d9-79b6-4834-ab05-5912cdac8115.jpg"></p>

2. Struktur Sistem Operasi Berlapis

    Sistem operasi memiliki sistem layer karena sistem operasi dibentuk secara hirarki berdasarkan lapisan-lapisan, Sehingga masing-masing layer 
    memiliki tujuan dan fungsi masing-masing. Lapisan-lapisan bawah akan memberi layanan kepada lapisan yang lebih atas. Lapisan yang paling 
    bawah adalah perangkat keras, dan yang paling tinggi adalah user-interface. Sebuah lapisan adalah implementasi dari obyek abstrak yang 
    merupakan enkapsulasi dari data dan operasi yang bisa memanipulasi data tersebut. Struktur berlapis dimaksudkan untuk mengurangi kompleksitas 
    rancangan dan implementasi sistem operasi. Tiap lapisan mempunyai fungsional dan antarmuka masukan-keluaran antara dua lapisan bersebelahan 
    yang terdefinisi bagus.

    Berikut gambar struktur sister operasi berlapis:

    <p>
    <img width="300px" src="https://user-images.githubusercontent.com/112605121/192242984-520259a2-566c-4e74-a800-f18b25054e36.png"></p>

3. Struktur Sistem Operasi Kernel

    Metode struktur ini adalah menghilangkan komponen-komponen yang tidak diperlukan dari kernel dan mengimplementasikannya sebagai sistem 
    dan program-program level user. Hal ini akan menghasilkan kernel yang kecil. Fungsi utama dari jenis ini adalah menyediakan fasilitas 
    komunikasi antara program client dan bermacam pelayanan yang berjalan pada ruang user. Selain itu, kernel mikro ini bertujuan untuk 
    mempermudah komunikasi yang terjadi antara program client dengan beragam layanan yang terdapat pada ruang user. Sehingga dengan adanya 
    kernel mikro ini dapat mempermudah dan memperluas sistem operasi, dan mudah ketika akan diubah (transformasi) ke arsitektur yang lebih baru. 
    Sehingga, dengan menggunakan kernel mikro, kode program akan aman karena lebih kecil.

    Berikut gambar struktur sister operasi kernel:

    <p>
    <img width="300px" src="https://user-images.githubusercontent.com/112605121/192243028-2af7983f-cdc5-4b1e-8738-8cad6d388268.jpg"></p>

---
