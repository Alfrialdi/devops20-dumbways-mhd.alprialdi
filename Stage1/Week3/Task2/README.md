Week 3 task 2

1.  Web server adalah sebuah software yang memberikan layanan data. Web
    server berfungsi untuk menerima permintaan HTTP atau HTTPS dari
    klien (Chrome, Firefox, Edge, dll) lalu akan mengirimkan respon
    tersebut kedalam bentuk halaman web misalnya Shoope. Peran web
    server yaitu memproses berbagai data (dari database server) yang di
    minta oleh client melalui web server dan kemudian web server akan
    memberikan jawaban berupa dokumen, foto, video atau beragaram berkas
    lainnya dalam bentuk halaman website sesuai permintaan dari client.

2.  Reverse proxy dari task week 2 day 1

    Disini terdapat 2 server yaitu vmware dan multipass yang sudah ada
    aplikasi wayshub dan sudah membuat index.js pada task sebelumnya di day
    1:

- Pada vmware, masuk ke direktori cd /etc/nginx, kemudian buat direkrori
  baru

> <img src="./media/image1.png"
> style="width:4.46218in;height:2.71409in" />

- Masuk kedalam direktori yang dibuat dan buat file
  my.reverse-proxy.conf kemudian masukkan script kedalamnya

> <img src="./media/image2.png" style="width:4.466in;height:2.70849in" />
>
> <img src="./media/image3.png" style="width:4.4371in;height:2.63935in" />

- Keluar dari direktori skrng lalu masuk ke dalam file nginx.conf

> <img src="./media/image4.png" style="width:4.47195in;height:2.7121in" />

- Scroll ke bawah ke bagian include lalu masukkan direktori folder yang
  sudah dibuat tadi

> <img src="./media/image5.png" style="width:4.53542in;height:2.7511in" />

- Mengecek apakah konfigurasi sudah tidak ada error dengan perintah
  berikut

> <img src="./media/image6.png" style="width:4.5058in;height:2.73463in" />

- Melakukan reload nginx

> <img src="./media/image7.png"
> style="width:4.46815in;height:2.69841in" />

- Selanjutnya membuat virtual host di local yaitu windows (karna
  nantinya mengkases domain melalui windows) untuk memasukkan domain
  yang sudah kita buat tadi

> <img src="./media/image8.png"
> style="width:4.42619in;height:2.51125in" />
>
> <img src="./media/image9.png"
> style="width:4.43646in;height:3.70901in" />

- Run aplikasi di multipass dengan cara npm run start

> <img src="./media/image10.png"
> style="width:4.45727in;height:2.21876in" />
>
> <img src="./media/image11.png"
> style="width:4.46696in;height:2.20626in" />

- Terakhir mengkases domain yang sudah dibuat tadi

> <img src="./media/image12.png"
> style="width:4.48938in;height:2.52273in" />

3.  Load balance adalah suatu jaringan komputer dengan metode
    mendistribusikan beban kerja pada dua atau lebih suatu koneksi
    jaringan secara seimbang agar pekerjaan dapat berjalan optimal dan
    tidak overload atau kelebihan beban pada salah satu jalur koneksi.

Load balance bekerja dengan cara mendistribusikan lalu lintas kunjungan
ke dalam beberapa server sehingga tidak ada salah satu server yang
mengalami kelebihan beban.

4.  Mengimplementasikan load balance dari apliaksi wayshub diatas tadi

- Disini perlu menambahkan satu server lagi yang sudah terinstall node,
  nvm, npm, dan sudah melakukan konfigurasi nodejs seperti pada task
  sebelumnya.

- Install app diatas tadi di server baru

> <img src="./media/image13.png"
> style="width:4.44106in;height:2.18117in" />
>
> <img src="./media/image14.png"
> style="width:4.43951in;height:2.2109in" />

- Selanjutnya menginstall appnya dengan perintah nvm install express
  –save lalu jalankan aplikasi dengan perintah npm run start

> <img src="./media/image15.png"
> style="width:4.43264in;height:2.21141in" />

- Mengecek apakah app sudah berjalan di web browser dengan cara ip:3000

> <img src="./media/image16.png"
> style="width:4.46485in;height:2.50895in" />

- Sekarang sudah dua server yang berjalan, yaitu 192.168.204.52 dan
  192.168.204.238, selanjutnya mengatur konfigurasi load balancing

- Masuk ke konfigurasi reverse proxy sebelumnya

> <img src="./media/image17.png"
> style="width:4.45979in;height:2.67014in" />

- Lalu ubah konfigurasinya sesuai ip diatas.

> <img src="./media/image18.png"
> style="width:4.4639in;height:2.66963in" />

- Mengecek apakah konfigurasi sudah benar dengan cara sudo nginx -t

> <img src="./media/image19.png"
> style="width:4.46671in;height:2.68022in" />

- Melakukan reload pada nginx dengan perintah “sudo systemctl reload
  nginx” dan mengecek statusnya

> <img src="./media/image20.png"
> style="width:4.4842in;height:2.67482in" />

- Membuka browser dengan nama domain yang sudah dibuat sebelumnya

> <img src="./media/image21.png"
> style="width:4.45706in;height:2.50456in" />

- Untuk memastikan load balancing sudah berhasil, coba matikan salah
  satu apps dan buka kembali domain

> <img src="./media/image22.png"
> style="width:4.47506in;height:2.23753in" />
>
> <img src="./media/image23.png"
> style="width:4.42446in;height:2.48625in" />
>
> Dapat dilihat masih bisa berjalan, yang artinya load balancing
> berhasil.
