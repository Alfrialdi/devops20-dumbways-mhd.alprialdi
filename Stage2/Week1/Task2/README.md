**STAGE 2**

Week 1 task 2

1.  Deploy database mysql

- Masuk ke server biznet appserver

> <img src="./media/image1.jpeg"
> style="width:4.38776in;height:2.28332in" />
>
> <img src="./media/image2.jpeg"
> style="width:4.44898in;height:2.41426in" />
>
> <img src="./media/image3.jpeg"
> style="width:4.44898in;height:2.33983in" />

- Menginstall mysql setelah melakukan update dan upgrade pada appserver

> <img src="./media/image4.jpeg"
> style="width:4.44218in;height:2.40958in" />

- Melakukan mysql secure installation yang betujuan untuk mengamankan
  mysql database dengan cara melakukan konfigurasi yaitu mengatur
  password untuk root

> <img src="./media/image5.jpeg"
> style="width:4.63946in;height:2.49655in" />
>
> <img src="./media/image6.jpeg"
> style="width:4.69388in;height:2.53883in" />

- Menambahkan password untuk root

> <img src="./media/image7.jpeg"
> style="width:4.6283in;height:2.68027in" />

- Masuk ke database mysql lalu buat user baru mysql

> <img src="./media/image8.jpeg"
> style="width:4.40136in;height:3.02331in" />
>
> <img src="./media/image9.jpeg"
> style="width:4.40136in;height:3.00722in" />

- Membuat database baru

> <img src="./media/image10.jpeg"
> style="width:4.65986in;height:2.69545in" />
>
> <img src="./media/image11.jpeg"
> style="width:4.68027in;height:2.69948in" />

- Mengatur agar user baru tadi dapat mengakses database yang telah
  dibuat sebelumnya

> <img src="./media/image12.jpeg"
> style="width:4.65464in;height:2.70068in" />

- Mengubah alamat bind-address pada konfigurasi mysql agar dapat di
  akses host lain

<img src="./media/image13.png"
style="width:4.68327in;height:5.2644in" />

- Mencoba remote database dari host lain

> <img src="./media/image14.jpeg"
> style="width:4.67347in;height:2.62876in" />

2.  Deploy aplikasi Wayshub-Backend

- Melakukan clone repository Wayshub-Backend

> <img src="./media/image15.png"
> style="width:4.73218in;height:2.2864in" />

- Menginstal Node 14

> <img src="./media/image16.png"
> style="width:4.69964in;height:4.03525in" />

- Mengatur konfigurasi di wayshub backend sesuai database yang telah
  dibuat

> <img src="./media/image17.jpeg"
> style="width:4.40818in;height:4.97959in" />
>
> <img src="./media/image18.jpeg"
> style="width:4.44384in;height:4.98639in" />
>
> <img src="./media/image19.jpeg"
> style="width:4.41511in;height:4.97959in" />

- Install sequelize-cli

> <img src="./media/image20.jpeg"
> style="width:4.39098in;height:4.95238in" />

- Melakukan running migration

> <img src="./media/image21.jpeg"
> style="width:4.47619in;height:4.10226in" />

- Deploy app menggunakan PM2

> <img src="./media/image22.jpeg"
> style="width:4.4197in;height:4.43537in" />
>
> <img src="./media/image23.jpeg"
> style="width:4.44898in;height:1.26579in" />
>
> <img src="./media/image24.jpeg"
> style="width:4.40818in;height:4.97959in" />
>
> <img src="./media/image25.jpeg"
> style="width:4.44218in;height:2.41057in" />
