Week 1 task 1

1.  Perbedaan IP statik dan IP dinamik & perbedaan IP private dan IP
    publik.

<!-- -->

1.  IP statis dan IP dinamis

- IP static yaitu IP yang di isi secara manual, IP akan tetap selama
  tidak berubah sedangkan IP dinamis adalah IP address yang diberikan
  oleh server, IP bisa berubah ubah tergantung settingan server.

- IP statis adalah pemberian alamat IP pada perangkat yang terhubung
  dalam jaringan komputer secara manual, IP ini biasanya dimiliki oleh
  layanan publik yang memerlukan koneksi stabil dan alamat web yang
  konsisten. IP statis tidak akan berubah selama atidak dirubah.
  Sedangkan IP dinamis adalah pemberian otomatis dalam jaringan publik
  dan pribadi, IP dinamis diberikan secara otomatis kepada perangkat
  yang terhubung dalam jaringan komputer. IP dinamis selalu berubah-ubah
  setiap waktu. IP dinamis diberikan oleh ISP, menetapkan alamat IP
  dinamis untuk perangkat yang tersambung dan berubah setiap kali
  mematikan ulang perangkat, menambahkan perangkat baru atau mengubah
  konfigurasi jaringan.

- IP statis kurang aman dibandingkan IP dinamis. Perangkat yang
  menggunakan IP statis dapat dilacak sedangkan IP dinamis tidak dapat
  dilacak.

- IP statis biasanya digunakan oleh bisnis sedangkan IP dinamis biasanya
  digunakan oleh rumah dan kantor.

2.  IP private dan IP publik

- IP private dipakai untuk komunikasi didalam jaringan yang sama, dengan
  memakai IP private, data atau informasi dapat dikirim atau diterima
  melalui jaringan yang sama. Sedangkan IP publik digunakan untuk
  komunikasi diluar jaringan, sehingga memungkinkan komunkasi antar
  perangkat di jaringan yang berbeda.

- IP private umumnya digunakan oleh ruang lingkup kecil seperti kantor,
  perusahaan, atau perumahan. Sedangkan IP publik digunakan oleh
  masyarakat global.

- IP private digunakan dalam jaringan lokal dan tidak dapat diakses
  langsung oleh internet. Sedangkat IP publik ip yang dapat diakses
  langsung oleh internet.

- IP publik diberikan oleh ISP sengakan IP private diberikan oleh locak
  admi

- IP publik kurang aman karena dapat dilihat secara online sedangkan IP
  private lebih aman karena hanya tersedia pada jaringan lokal.

2.  Virtualisasi adalah teknologi yang memungkinkan satu mesin fisik
    dapat menjalankan beberapa sistem operasi atau lingkungan aplikasi
    secara bersamaan. Misalnya dapat menjalankan beberapa OS atau server
    dalam satu komputer. Teknologi ini memungkinkan untuk membuat mesin
    virtual didalam mesin fisik yang sama. Untuk menggunakannya di
    perlukan aplikasi atau emulator seperti VMware atau Virtualbox.
    Dengan adanya teknologi ini kita dapat memaksimalkan penggunaan
    sumber daya komputer atau server dan juga dapat memperoleh efesiensi
    dan penghematan biaya serta memudahkan melakukan monitoring server.

3.  Membuat rancangan jaringan dengan:

- CIDR Block: 192.168.1.xxx/24

- Subnet: 255.255.255.0

- Gateway: 192.168.1.1

> Hasilnya adalah sebagai berikut:
>
> <img src="./media/image1.png"
> style="width:5.33544in;height:0.52491in" />
>
> Rancangan jaringan berikut didapatkan dengan melakukan subnetting
> sebagai berikut:
>
> 192.168.1.xxx/24:
>
> /24 dalam tabel subnetting adalah 11111111.11111111.11111111.00000000.
> jadi dalam desimal adalah 255.255.255.0.
>
> Karena ini kelas C, maka X= jumlah binary 1 pada oktet terakhir maka =
> 0. Y= jumlah binary 0 pada oktet terakhir maka = 8.
>
> Jadi,
>
> Subnet = 2<sup>x</sup> = 2 pangkat 0 = 1
>
> Jumlah host = 2<sup>8</sup> = 256 – 2 = 254 host.
>
> Jumlah subnet = 256 – 0 (angka terkahir pada subnet 255.255.255.0) =
> 256 = (0, 256). Karena 256 di jaringan tidak digunakan jadi jumlah
> gang subnet hanya ada 1 yaitu 0, maka didaptlah hanya 1 gang subnet =
> 192.168.1.0. Jadi:
>
> IP network = 192.168.1.0
>
> IP broadcast = 256 – 1 = 192.168.1.255
>
> IP awal = 192.168.1.1 (IP netwok + 1)
>
> IP akhir = 192.168.1.254 (IP broadcast -1)

4.  Langkah-langkah menginstall VM ubuntu server melalui VMware:

- Membuka VMware dan memilih “create new virtual machine”

> <img src="./media/image2.jpeg"
> style="width:4.94304in;height:3.94085in" />

- Pada installer disc image pilih file OS ubuntu server yang telah di
  unduh sebelumnya

> <img src="./media/image3.jpeg"
> style="width:4.9557in;height:4.08107in" />

- Lalu klik next dan pada “personalize linux” isi sesuai yang di
  inginkan

> <img src="./media/image4.jpeg"
> style="width:4.99367in;height:3.92644in" />

- Selanjutnya isi nama dari VM ubuntu server sesuai yang di inginkan
  lalu klik next

> <img src="./media/image5.jpeg"
> style="width:4.96203in;height:3.94224in" />

- Berikutnya mengisi jumlah storage sesuai yang diperlukan, disini saya
  mengisi 13 GB

> <img src="./media/image6.jpeg"
> style="width:4.94937in;height:4.00566in" />

- Lalu akan keluar tampilan seperti ini, kemudian pilih costumize
  hardware

> <img src="./media/image7.jpeg"
> style="width:4.96924in;height:3.99367in" />

- Pada bagian memory, isi sesuai kebutuhan, disini saya mengisi 2048 MB

> <img src="./media/image8.jpeg" style="width:5in;height:4.65045in" />

- Berikutnya pada bagian processor, isi sesuai kebutuhan

- Lalu pada bagian network adapter, pilih adapter yang digunakan sebagai
  internet pada local, disini saya memilih Intel(R) Wi-fi 6

> <img src="./media/image9.png"
> style="width:4.97315in;height:4.70152in" />

- Setelah itu klik ok kemudian finish maka akan memasuki proses
  instalasi ubuntu server

- Langkah berikutnya pilih bahasa yang di inginkan

> <img src="./media/image10.jpeg"
> style="width:5.0443in;height:3.22073in" />

- Kemudian pada keyboard configuration pilih done

- Lalu pada network configuration pilih edit IPv4 kemudian pilih manual

> <img src="./media/image11.png"
> style="width:4.9835in;height:3.29399in" />

- Dibagian ini isi sesuai default gateway dan subnet pada local OS

> <img src="./media/image12.png"
> style="width:4.97476in;height:5.16822in" />

- Berikutnya pada bagian storage configuration, pertama pilih reset
  kemudian klik pada free space dan pilih add GPT partition

> <img src="./media/image13.jpeg"
> style="width:5.06329in;height:4.35591in" />

- Lalu isi size nya, disini saya mengisi 11GB dari total 13GB memory,
  dan pada bagian format pilih ext4 dan create

> <img src="./media/image14.jpeg"
> style="width:4.96083in;height:3.51266in" />

- Ulangi langkah sebelumnya, namut format yang di pilih adalah swap dan
  isi size nya 1.5 GB lalu create, maka tampilan akan seperti ini, lalu
  klik done.

> <img src="./media/image15.jpeg"
> style="width:5.01899in;height:4.27331in" />

- Selanjutnya pada SSH setup, ceantang bagian install OpenSSH server

> <img src="./media/image16.jpeg"
> style="width:4.94304in;height:4.21358in" />

- Tunggu hinga proses instalasi selesai dan akan menampilkan halaman
  login

> <img src="./media/image17.jpeg"
> style="width:5.01149in;height:4.26582in" />
>
> <img src="./media/image18.jpeg"
> style="width:5.0443in;height:4.17862in" />
