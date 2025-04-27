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

  **A. CAT**

  - Jika ingin membuat sebuah file dan isi file tersebut bisa menggunakan ``` nano nama_file ``` atau ``` cat > nama_file ```
 
    namun disini saya akan menjelaskan detail apa saja fungsi penggunaan ``` cat ```

    contoh untuk membuat sebuah file menggunakan perintah ``` cat > file2 ``` lalu tekan **Enter** dan **CTRL + C**
  
    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/cat%20file2.png)

  - Menggabungkan isi dari 2 buah file sekaligus membuat file baru dengan menggunakan perintah ``` cat file1 file2 > file3 ```

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/menggabungkan%20kedua%20file%20dan%20masukkan%20ke%20file%20baru.png)


  **B. SED**

  - Jika ingin edit kata dari sebuah file secara langsung dengan 1 perintah, ketikkan perintah dengan format ``` sed -i 's/kata_before/kata_after/g' nama_file ```

    contoh saya memiliki file yang bernama file1 yang berisi **hello dumbways**

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/isi%20file1.png)

  - saya ingin mengubah kata **hello** menjadi **hai** dengan ketikkan perintah ``` sed -i 's/hello/hai/g' file1 ```

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/penggunaan%20sed%20-i.png)


  **C. GREP**

  - Jika ingin mencari kata dari sebuah file, ketikkan perintah dengan format ``` grep kata nama_file ```

    contoh saya ingin mencari kata **hai** didalam sebuah file **file1**

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/penggunaan%20grep%20untuk%20search%20kata%20didalam%20file.png)

  - Menghitung ada berapa banyak kata **hai** didalam **file1** dengan ketikkan perintah ``` grep -c hai file1 ```

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/grep%20c.png)

  - Menghitung ada berapa banyak kata **hello** di semua file dengan ketikkan perintah ``` grep -c hello * ```

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/grep%20c%20hello%20bintang.png)


  **D. ECHO**

  - Jika ingin mencetak sebuah kalimat, ketikkan perintah dengan format ``` echo "isi kalimat" ```

    contoh saya ingin mencetak kalimat **Hello World** ketikkan perintah ``` echo "Hello World" ```

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/echo%20mencetak%20kata.png)

  - Mencetak kalimat lalu memasukkannya kedalam sebuah file ``` echo "ini file4" > file4 ```

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/echo%20mencetak%20dan%20menambah%20file.png)

  - Mencetak kalimat dibaris berikutnya didalam sebuah file ``` echo "iya benar ini file4" >> file4 ```

    ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/echo%20mencetak%20baris%20baru%20di%20sebuah%20file.png)
