# Web Server

_Web Server_ adalah suatu **software** yang bertugas untuk menerima request dari client melalui protokol HTTP/HTTPS, dan mengirimkan respon kembali berupa halaman web. Salah satu fungsi utama web server adalah routing dan forwarding ke backend (**reverse proxy**)

Contoh jenis jenis Web Server :

- Apache2
- Nginx
- Caddy
- LiteSpeed


_Reverse Proxy_ adalah server perantara yang menerima request dari client melalui protokol HTTP/HTTPS lalu **meneruskannya ke server backend** dan mengembalikan respon dari backend ke client **seolah olah datang langsung dari reverse proxy**


## 1. Struktur Web Server dengan menggunakan Reserve Proxy

![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/struktur%20web%20server%20dengan%20menggunakan%20reverse%20proxy.png)

**Penjelasan** :

- **Client** mengirimkan request berupa HTTP/HTTPS, contoh : https//google.com
- **Reverse Proxy (nginx)** menerima request dari port 80/443 dan push request tersebut ke backend (App server & Database)
- **App Server** mengembalikan respon ke client yang seolah olah datang langsung dari reverse proxy

## 2. Konfigurasi Reverse Proxy untuk aplikasi yang sudah dilakukan deploy (wayshub) dan sesuaikan domain nya dengan nama masing masing (mochrere.xyz)

- Jalankan app wayshub yang sebelumnya sudah dibuat, masuk ke direktori **wayshub-frontend** lalu masukan perintah `` npm start ``

  _NOTE :_ Pastikan Node yang digunakan versi 13, karna module yang digunakan di app adalah versi node 13

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6.png)

- Buka terminal baru, lakukan update library ubuntu `` sudo upt update ``
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step0.png)

- Install web server nginx `` sudo apt install nginx `` dan pastikan sudah active `` systemctl status nginx ``

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step1.png)

- Selanjutnnya saya akan edit file txt yang bernama host, untuk menambahkan penamaan IP Address lokal saya dengan domain **mochrere.xyz**

  lokasi file txt berada di ``C:\Windows\System32\drivers\etc`` dan buka di aplikasi note++ sebagai administrator lalu **save**

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step2.png)

- lalu masuk ke terminal, karna nginx berjalan di port 80, pastikan port 80 sudah diberi akses di _ufw_ , jika belum masukkan perintah `` sudo ufw allow 80 `` dan cek apakah sudah berhasil, masukkan perintah `` sudo ufw status ``

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step3.png)

- test apakah pengimplemntasian penamaan domain **mochrere.xyz** sudah berhasil

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step4.png)

 - selanjutnya konfigurasi nginx, supaya app **wayshub** berhasil di implementasikan ke domain **mochrere.xyz**

   masuk terminal dan ketikkan perintah `` cd /etc/nginx/sites-enabled/ `` dan buat sebuah file wayshub.conf `` sudo nano wayshub.conf ``

   ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step5.png)

- di file tersebut masukkan script seperti dibawah ini, lalu **save**

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step6.png)

- lakukan test apakah konfigurasi tersebut berhasil dengan masukkan perintah `` sudo nginx -t ``

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step7.png)

- Restart app nginx dengan masukkan perintah `` sudo systemctl restart nginx `` dan cek kembali apakah nginx sudah ok `` sudo systemctl status nginx ``

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step8.png)

- Lakukan test apakah konfigurasi reverse proxy dari app wayshub ke domain **mochrere.xyz** sudah berhasil

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day6_a_step9.png)


  # Thank You
