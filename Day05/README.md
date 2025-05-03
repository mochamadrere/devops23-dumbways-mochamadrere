# Application In Server

Di materi kali ini saya akan mencoba untuk mendeploy application di server, web server yang digunakan adalah nginx.

## 1. NodeJS

### A. Deploy app wayshub-frontend


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

  

