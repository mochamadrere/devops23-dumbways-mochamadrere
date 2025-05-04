# Application In Server

Di materi kali ini saya akan mencoba untuk mendeploy application di server, web server yang digunakan adalah nginx.

## 1. NodeJS (Deploy app wayshub-frontend, berjalan di port 3000 dan menggunakan NodeJS 13)

- Langkah pertama penginstallan **NodeJS**, buka website resmi NodeJS https://nodejs.org/en/download

  pilih versi LTS (Long Term Support) agar bisa digunakan dalam jangka panjang dan OS Linux dengan menggunakan nvm dan npm.

  ikuti step by step command penginstallan **NodeJS**

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step2.png)

- Masukkan perintah ``` curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash ```

  dan refresh _bash_ karna saya baru saja menginstall aplikasi baru, dengan masukkan perintah ``` exec bash ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step3.png)

- Download dan install nvm (node version manager) versi 13, dengan masukkan perintah ``` nvm install 13 ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step4.png)

- Dan cek kembali apakah versi node sudah sesuai

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step5.png)


- Jika NodeJS sudah berhasil terinstall, step selaanjutnya pastikan web server nginx sudah terinstall dan berstatus active, dengan masukkan perintah ``` sudo install nginx ```

  dan untuk mengecek status nginx ``` systemctl status nginx ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step0.png)

- Cloning repository https://github.com/dumbwaysdev/wayshub-frontend dengan masukkan perintah format ``` git clone code_https_repo_github ```

  dan cek apakah repository sudah berhasil di cloning

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step1.png)

- Masuk kedalam repository ``` cd wayshub-frontend ``` lalu saya akan install semua module didalam folder project tersebut, agar file _package.json_ bisa terbaca dengan perintah ``` npm install ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step6.png)

- Cek file didalam repository wayshub-frontend, apakah sudah ada file script yang di generate menjadi _package.json_

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step8.png)

- Selanjutnya saya akan jalankan app tersebut di port **3000**, edit file _package.json_ masukan perintah ``` nano package.json ``` lalu tambahkan perintah ``` PORT=3000 ``` di bagian scripts "start", jika sudah save

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step7.png)

- Sebelum menjalankan app, pastikan port **3000** sudah diberi akses, jika belum masukkan perintah ``` sudo ufw allow 3000 ``` dan cek kembali dengan perintah ``` sudo ufw status ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step9.png)

- Jika semua sudah oke, saatnya jalankan app **wayshub-frontend** dengan masukkan perintah ``` npm start ```

  test di terminal baru dengan perintah ``` curl localhost:3000 ``` dan juga test melalui browser ``` 192.168.1.9:3000 ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_a_step10.gif)


## 2. Python (Deploy app menampilkan text nama, berjalan di port 5000 dan bisa dibuka melalui web)

- Aplikasi **Python** di Ubuntu secara default sudah terinstall, jadi tidak perlu melakukan install app python tetapi yang perlu di install adalah _pip_.

  _pip_ adalah package manager untuk menginstall dan mengelola library atau modul external di Python.
  
  untuk cek versi python yang digunakan masukkan perintah ``` python3 -V ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_b_step0.png)

  untuk menginstall _pip_ masukan perintah ``` sudo apt install python3-pip ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_b_step1.png)

- Buat sebuah direktori yang bernama python ``` mkdir python ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_b_step2.png)

- Masuk kedalam direktori python lalu install module _flask_ yang berfungsi sebagai web framework di python.

  masukkan perintah ``` pip install flask ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_b_step4.png)

- Setelah install _flask_, saya akan membuat sebuah index.py yang berisi script python
  
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_b_step3.png)

- Pada bagian def index, masukkan script return 'Hello, Mochamad Rere Ulul Albab' yang artinya pada saat URL dijalankan akan mencetak **'Hello, Mochamad Rere Ulul Albab'**

  pada bagian app.run terdapat script host='0.0.0.0' artinya flask akan menerima koneksi dari semua alamat IP, tanpa ini flask hanya bisa diakses dari localhost.

  port=5000 artinya saya akan menempatkan bahwa flask ini akan berjalan di port **5000**
  
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_b_step5.png)

- Setelah itu save script tersebut pada file index.py, lalu pastikan port **5000** sudah diberi akses pada ufw, masukkan perintah ``` sudo ufw allow 5000 ```

  lalu cek kembali masukkan perintah ``` sudo ufw status ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_b_step6.png)

- Terakhir jalankan aplikasi tersebut di terminal dengan masukkan perintah ``` python3 index.py ```

  cek pada terminal apakah sudah berjalan, dengan perintah ``` curl localhost:5000 ``` dan cek pada browser masukkan ``` 192.168.1.9:5000 ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_b_step7.gif?raw=true)


## 3. Golang (Deploy app dengan menampilkan text "Golang geming!"

- Langkah pertama download terlebih dahulu aplikasi golang dengan masukkan perintah ``` wget -4 https://go.dev/dl/go1.24.2.linux-amd64.tar.gz ```

  disini saya tambahkan perintah **-4** untuk memaksa menggunakan IPv4 dikarenakan sistem saya gagal konekasi server go.dev via IPv6 pada port 443 (HTTPS)

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_c_step0.png)

- selanjutnya masukkan perintah ``` sudo su ``` untuk masuk sebagai root dikarenakan akan ada perubahan di sistem ubuntu,

  lalu masukkan perintah ``` rm -rf /usr/local/go && tar -C /usr/local -xzf go1.24.2.linux-amd64.tar.gz ``` dan tekan **CTRL + D** untuk exit

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_c_step1.png)

- Masukkan perintah ``` export PATH=$PATH:/usr/local/go/bin ``` yang berfungsi untuk menambahkan **Go** ke dalam PATH environment variable, yang nantinya saat masukkan perintah ```go``` diterminal, perintah tersebut dapat berjalan tanpa perlu mengetik path lengkap.

  lalu cek apakah sudah berhasil dengan ketik perintah ``` go version ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_c_step2.png)

- Buat sebuah direktori bernama golang ``` mkdir golang ``` lalu masuk ke direktori tersebut.

  Dan buat sebuah file yang bernama **index.go** ``` nano index.go ``` yang nantinya akan saya masukan script index sederhana untuk mencetak kalimat **Golang geming!** dan save script tersebut.

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_c_step3.png)

- selanjutnya jalankan script yang ada di file **index.go** dengan masukkan perintah ``` go run index.go ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/day5_c_step4.png)


# Thank You

  

  
  

  
  

