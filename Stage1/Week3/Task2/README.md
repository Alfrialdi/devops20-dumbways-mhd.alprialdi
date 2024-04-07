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

> <img src="./media/image1.png" style="width:4.9846in;height:3.03185in" />

- Masuk kedalam direktori yang dibuat dan buat file
  my.reverse-proxy.conf kemudian masukkan script kedalamnya

> <img src="./media/image2.png"
> style="width:5.01343in;height:3.04049in" />
>
> <img src="./media/image3.png"
> style="width:4.98067in;height:2.96269in" />

- Keluar dari direktori skrng lalu masuk ke dalam file nginx.conf

> <img src="./media/image4.png"
> style="width:4.98144in;height:3.02109in" />

- Scroll ke bawah ke bagian include lalu masukkan direktori folder yang
  sudah dibuat tadi

> <img src="./media/image5.png"
> style="width:4.96138in;height:3.00948in" />

- Mengecek apakah konfigurasi sudah tidak ada error dengan perintah
  berikut

> <img src="./media/image6.png"
> style="width:4.93113in;height:2.99277in" />

- Melakukan reload nginx

> <img src="./media/image7.png" style="width:5.05876in;height:3.0551in" />

- Selanjutnya membuat virtual host di local yaitu windows (karna
  nantinya mengkases domain melalui windows) untuk memasukkan domain
  yang sudah kita buat tadi

> <img src="./media/image8.png"
> style="width:5.06726in;height:2.87496in" />
>
> <img src="./media/image9.png" style="width:5.0661in;height:4.23541in" />

- Run aplikasi di multipass dengan cara npm run start

> <img src="./media/image10.png"
> style="width:5.08301in;height:2.53024in" />
>
> <img src="./media/image11.png"
> style="width:5.09896in;height:2.51841in" />

- Terakhir mengkases domain yang sudah dibuat tadi

> <img src="./media/image12.png"
> style="width:5.10474in;height:2.86852in" />

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
> style="width:5.04037in;height:2.47551in" />
>
> <img src="./media/image14.png"
> style="width:5.03577in;height:2.50784in" />

- Selanjutnya menginstall appnya dengan perintah nvm install express
  –save lalu jalankan aplikasi dengan perintah npm run start

> <img src="./media/image15.png"
> style="width:5.06006in;height:2.52442in" />

- Mengecek apakah app sudah berjalan di web browser dengan cara ip:3000

> <img src="./media/image16.png"
> style="width:5.05981in;height:2.84327in" />

- Sekarang sudah dua server yang berjalan, yaitu 192.168.204.52 dan
  192.168.204.238, selanjutnya mengatur konfigurasi load balancing

- Masuk ke konfigurasi reverse proxy sebelumnya

> <img src="./media/image17.png"
> style="width:5.09304in;height:3.04928in" />

- Lalu ubah konfigurasinya sesuai ip diatas

> <img src="./media/image18.png"
> style="width:5.06861in;height:3.03128in" />

- Mengecek apakah konfigurasi sudah benar dengan cara sudo nginx -t

> <img src="./media/image19.png"
> style="width:5.05579in;height:3.0337in" />

- Melakukan reload pada nginx dengan perintah “sudo systemctl reload
  nginx” dan mengecek statusnya

> <img src="./media/image20.png"
> style="width:5.06207in;height:3.01952in" />

- Membuka browser dengan nama domain yang sudah dibuat sebelumnya

> <img src="./media/image21.png"
> style="width:5.05049in;height:2.83803in" />

- Untuk memastikan load balancing sudah berhasil, coba matikan salah
  satu apps dan buka kembali domain

> <img src="./media/image22.png"
> style="width:5.05293in;height:2.52647in" />
>
> <img src="./media/image23.png"
> style="width:5.0581in;height:2.84231in" />
>
> Dapat dilihat masih bisa berjalan, yang artinya load balancing
> berhasil.
