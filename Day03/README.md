# Manage Server with Terminal


## 1. Akses server menggunakan terminal (Windows Terminal)


- Untuk install ssh pada ubuntu server ketikkan perintah ``` sudo apt install openssh-server ```


  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/sudo%20apt%20install%20openssh-server.png)


- Cek apakah ssh server sudah terinstall dan aktif dengan ketikkan perintah ``` sudo systemctl status ssh ```

  
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/sudo%20systemctl%20status%20ssh.png)

  keterangan diatas menunjukkan bahwa ssh server sudah aktif dan bisa digunakan.


- Setelah itu saya akan test apakah sudah bisa digunakan atau belum, disini saya menggunakan Windows Terminal


  ketikkan perintah dengan format **ssh (username ubuntu)@(ip address ubuntu)**


  ```sh
  ssh mrua@192.168.1.9
  ```


  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/ssh%20mrua%40192.168.1.9.png)


## 2. Konfigurasi SSH agar bisa di akses hanya menggunakan _publickey_ (password dimatikan)


- Langkah awal saya akan mengenerate key ssh dengan ketikkan perintah ``` ssh-keygen ```

  selanjutnya ketikkan perintah ``` C:\Users\mocha/.ssh/kunci ``` /kunci adalah nama file yang ingin saya buat yang berisi password atau openssh key


  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/ssh-keygen.png)


- Cek apakah file kunci.pub sudah terbentuk atau belum di file direktori ``` C:\Users\mocha\.ssh ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/cek%20file%20kunci.pub%20di%20lokal.png)


- Buka file kunci.pub lalu copy yang nantinya akan saya paste ke dalam file ssh di server ubuntu

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/kunci.pub.png)


- Selanjutnya pada windows terminal kita masuk ke server ubuntu via ssh terlebih dahulu untuk mem paste _publickey_ yang sudah di generate kedalam file ssh server.

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/open%20file%20.ssh%20di%20server%20ubuntu.png)


  Paste _publickey_ lalu save

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/authorized_keys.png)


- Oke, saya akan test apakah sudah berhasil, dengan ketikkan perintah ``` ssh -i .ssh/kunci mrua@192.168.1.9 ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/ssh%20-i%20.ssh(slash)kunci%20mrua%40192.168.1.9.png)


## 3. Step by step penggunaan text manipulation (cat, sed, grep, echo)

- Jika ingin membuat sebuah file dan edit isi file tersebut bisa menggunakan ``` nano nama_file ``` atau ``` cat > nama_file ```
 

  namun disini saya akan menjelaskan detail apa saja fungsi penggunaan ``` cat ```


  contoh untuk membuat sebuah file menggunakan perintah ``` cat > file2 ``` lalu tekan ** Enter ** dan ** CTRL + C **
  
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/cat%20file2.png)
