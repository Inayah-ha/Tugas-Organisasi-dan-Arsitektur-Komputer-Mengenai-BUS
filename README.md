# Tugas-Organisasi-dan-Arsitektur-Komputer-Mengenai-BUS

## 1. Jelaskan Struktur Antar Hubungan dan Beri Contohnya?
Struktur antar hubungan dalam sistem komputer merupakan kerangka kerja yang berfokus pada pengaturan jalur komunikasi, atau yang dikenal sebagai sistem bus, untuk menghubungkan komponen-komponen utama seperti prosesor (CPU), memori utama, perangkat input/output (I/O), dan penyimpanan. Sistem bus ini berperan sebagai jalur fisik maupun logis yang memungkinkan transfer data, instruksi, dan sinyal kontrol di antara komponen-komponen tersebut. Dengan adanya sistem bus, struktur antar hubungan dapat memastikan komunikasi yang efisien dan terkoordinasi, sehingga setiap komponen dapat menjalankan fungsinya secara optimal. Sistem bus menjadi elemen inti dalam implementasi struktur antar hubungan karena menyediakan mekanisme yang diperlukan untuk mendukung operasi dan interaksi antar komponen dalam sistem komputer.

Contohnya :
1. PCI (Peripheral Component Interconnect)
PCI adalah salah satu jenis bus yang dirancang untuk menghubungkan perangkat keras seperti kartu grafis, kartu suara, atau kartu jaringan ke motherboard komputer. PCI memberikan jalur komunikasi yang stabil dan cepat antara perangkat-perangkat tersebut dengan prosesor, sehingga mendukung kinerja komputer secara keseluruhan. Dengan menggunakan slot PCI, perangkat keras dapat dengan mudah dipasang dan berfungsi sebagai bagian dari sistem tanpa memerlukan konfigurasi yang kompleks.

2. USB (Universal Serial Bus)
USB adalah bus yang sangat fleksibel dan paling sering digunakan pada komputer modern untuk menghubungkan perangkat seperti flash drive, mouse, keyboard, atau printer. Salah satu keunggulan utama USB adalah fitur plug-and-play, di mana perangkat dapat dikenali dan digunakan secara instan setelah terhubung. Selain itu, USB juga dapat memberikan daya listrik, memungkinkan perangkat seperti smartphone atau perangkat portabel lainnya untuk diisi dayanya saat terhubung ke komputer.

3. SATA (Serial Advanced Technology Attachment)
SATA adalah bus yang digunakan untuk menghubungkan perangkat penyimpanan, seperti hard disk dan SSD, ke motherboard. Dibandingkan teknologi lama seperti PATA, SATA menawarkan kecepatan transfer data yang jauh lebih tinggi, sehingga memungkinkan akses data yang cepat dan efisien. Ini menjadikannya standar utama dalam komputer modern, terutama untuk perangkat yang membutuhkan performa penyimpanan tinggi.

4. PCIe (Peripheral Component Interconnect Express)
PCIe adalah pengembangan dari PCI yang dirancang untuk memberikan kecepatan transfer data yang lebih tinggi melalui jalur point-to-point. PCIe banyak digunakan dalam perangkat keras modern, seperti kartu grafis dan SSD NVMe, karena kebutuhan bandwidth yang besar untuk aplikasi seperti gaming, rendering video, atau komputasi intensif. PCIe memungkinkan komunikasi data yang cepat dan efisien antara perangkat keras dan prosesor.

**Sumber :**

IDCloudHost. (n.d.). Universal Serial Bus (USB): Pengertian dan Fungsinya. Diakses pada 24 Maret 2025, dari https://idcloudhost.com/kamus-hosting/universal-serial-bus-usb/

Belajar Online. (2020). Komunikasi I2C dan SPI pada Sistem Embedded. Diakses pada 24 Maret 2025, dari https://www.belajaronline.net/2020/07/komunikasi-i2c-dan-spi.html

IBM Knowledge Center. (n.d.). Understanding Bus Architectures, dari

https://www.ibm.com/docs/en


## 2. Bila terlalu banyak modul atau perangkat dihubungkan pada bus maka akan terjadi penurunan kinerja, sebutkan penyebabnya?
Ketika terlalu banyak modul atau perangkat terhubung pada satu bus, kinerja sistem komputer dapat menurun karena beberapa alasan utama. Salah satu penyebab utamanya adalah keterbatasan bandwidth. Setiap bus memiliki kapasitas maksimal untuk mentransfer data, sehingga jika terlalu banyak perangkat mengirimkan data secara bersamaan, kapasitas tersebut dapat melebihi batasnya. Hal ini dapat mengakibatkan penundaan proses atau bahkan kegagalan sistem. Selain itu, konflik pada bus juga menjadi masalah yang signifikan. Karena semua perangkat dalam sistem komputer menggunakan bus data dan bus alamat yang sama, tanpa pengaturan yang baik, dapat terjadi benturan dalam penggunaannya yang mengganggu aliran data.

Peningkatan latensi juga menjadi faktor yang berkontribusi terhadap penurunan kinerja. Saat jumlah perangkat yang terhubung semakin banyak, waktu yang dibutuhkan untuk mentransfer data dari satu komponen ke komponen lainnya menjadi lebih lama. Akibatnya, respons sistem melambat, dan efisiensi keseluruhan menurun. Selain itu, beban berlebih pada bus juga dapat menyebabkan pemanasan yang berlebihan. Hal ini sering terjadi karena aktivitas listrik yang tinggi dan kurangnya sirkulasi udara di sekitar perangkat, yang pada akhirnya memengaruhi performa serta daya tahan perangkat tersebut. Oleh sebab itu, penting untuk mengelola koneksi perangkat pada bus dengan baik agar stabilitas dan kinerja sistem tetap terjaga.

**Sumber :**

Adikarta, Kusuma. (2015). Pengenalan Sistem Bus. Diakses dari https://adikartakusuma.wordpress.com/2015/11/13/pengenalan-3-sistem-bus 

Natha.id. (n.d.). Bus Komputer. Diakses dari https://natha.id/bus-komputer/ 

## 3. Umumnya perangkat berprioritas paling rendah memiliki waktu tunggu rata-rata yang paling singkat. Dengan dasar ini biasanya CPU diberi perioritas tertinggi pada SBI. Sebutkan alasan perangkat berprioritas 16 memiliki waktu tunggu rata-rata paling rendah? Dibawah kondisi seperti apa keadaan diatas tidak berlaku?
Dalam sistem komputer, penjadwalan interupsi menentukan urutan penanganan sinyal interupsi berdasarkan prioritas yang telah ditetapkan. Secara umum, perangkat dengan prioritas lebih tinggi, seperti CPU, akan dilayani terlebih dahulu untuk memastikan operasi sistem berjalan efisien. Namun, dalam beberapa kasus, perangkat dengan prioritas lebih rendah, seperti yang memiliki prioritas 16, dapat mengalami waktu tunggu rata-rata yang lebih singkat.​

Alasan Perangkat Berprioritas 16 Memiliki Waktu Tunggu Rata-Rata Paling Rendah:

Algoritma Penjadwalan yang Digunakan: Jika sistem menerapkan algoritma penjadwalan seperti Round-Robin, setiap perangkat diberikan jatah waktu eksekusi secara bergilir tanpa memandang prioritasnya. Dalam skenario ini, perangkat berprioritas 16 mungkin mendapatkan waktu layanan lebih cepat karena tidak harus menunggu hingga semua perangkat berprioritas lebih tinggi selesai dilayani. ​

Kondisi di Mana Keadaan Tersebut Tidak Berlaku:

Penjadwalan Berbasis Prioritas Absolut: Dalam sistem yang menerapkan penjadwalan berdasarkan prioritas absolut, perangkat dengan prioritas tertinggi selalu dilayani terlebih dahulu. Akibatnya, perangkat dengan prioritas lebih rendah, seperti prioritas 16, akan mengalami waktu tunggu yang lebih lama karena harus menunggu hingga semua perangkat berprioritas lebih tinggi selesai dilayani. 

**Sumber  :**

Elrachman, D. (2016). Algoritma Penjadwalan dalam Sistem Operasi. Diakses pada 24 Maret 2025, dari https://dhewielrachman.blogspot.com/2016/10/algoritma-penjadwalan-dalam-sistem.html.

Musthofa, T. (2015). Algoritma Penjadwalan dalam Sistem Operasi. Diakses pada 24 Maret 2025, dari https://thohirmusthofa.wordpress.com/2015/04/13/algoritma-penjadwalan-dalam-sistem-operasi/.



