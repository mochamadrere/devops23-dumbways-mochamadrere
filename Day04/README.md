# Version Control System

**Version Control System** _(VCS)_ adalah sebuah tools yang berfungsi untuk mengelola perubahan dari setiap code yang memilki fitur mentracking dari setiap perubahan yang sudah dilakukan terus menerus atau lebih simpelnya memiliki fitur history perubahan, tools ini bersifat online yang harus terhubung dengan jaringan. Salah satu aplikasi VCS yaitu **GIT**


## 1. Penjelasan tentang GIT

**GIT** adalah sistem kontrol versi yang digunakan untuk mencatat perubahan pada file, yang biasanya dalam proyek pengembangan system atau software. Git dapat membantu melacak perubahan yang dibuat ke file dan memungkinkan kembali ke versi yang sebelumnya jika perlu. GIT juga memudahkan banyak pengguna untuk bekerja sama di sebuah proyek yang sama tanpa saling mengacaukan kerjaan masing - masing. GIT berkolaborasi dengan platform online seperti _GitHub, GitLab, atau BitBucket_.


## 2. Buat sebuah repository "dumbways-batch-23" yang berisi 3 file


- Buat user dan email git pada terminal

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20config%20global%20user%20dan%20email.png)

- Copy SSH keygen pada terminal di file id_rsa.pub ke platform online GitHub dengan cara klik ``` Setting ``` lalu pilih ``` SSH and GPG keys ``` klik ``` new SSH key ``` dan paste ke kolom **key** dan klik ``` Add SSH key ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/copy%20paste%20ssh%20key.png)


- cek apakah sudah berhasil dengan ketikkan perintah ``` ssh git@github.com -T ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/test%20masuk%20git%20pada%20terminal.png)

- membuat reposiroty "dumbways-batch-23" ketikkan perintah ``` git init dumbways-bacth-23 ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20init%20dumbways%20batch23.png)

- Masuk kedalam repository dumbways-batch-23

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/cd%20dumbways%20batch23.png)

- Buat 3 file didalam repository tersebut

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/cat%20file1%20file2%20file3.png)


## 3. Manage repository tugas menggunakan terminal

- Karna saya menggunakan repository yang sudah ada

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20clone%20https.png)

- Maka saya akan melakukan cloning file tersebut pada terminal dengan format ``` git clone code_url_https ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20clone%20devops23%20repo.png)

- Dan berhasil di cloning, lalu masuk kedalam repository tersebut cek apakah file file yang tersedia sudah sesuai

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/isi%20file%20repo%20devops23.png)

- Nah, disini saya akan mencoba memanage direktori Day04 yang berisi file **README.md**

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/nano%20readme.md%20file.png)

- Edit isi file **README.md** dan saya tambahkan sebuah kalimat yang saya beri tanda kotak merah, jika sudah tekan **CTRL + X** lalu save.

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/edit%20isi%20file%20readme.md.png)


### Step selanjutnya perubahan tersebut akan saya push ke platform online _GitHub_

- Cek apakah ada history perubahan yang tadi saya buat, dengan ketikkan perintah ``` git status ```.

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20status%20perubahan.png) 

- selanjutnya simpan perubahan tersebut ke database Git, dengan format ``` git add nama_file ``` jika mengarah ke 1 file saja atau ``` git add . ``` untuk kesemua file. dan cek lagi apakah sudah tersimpan atau belum dengan perintah ``` git status ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20add%20.%20dan%20git%20status.png)

- Lalu selanjutnya lakukan commit agar perubahan tersebut benar benar tersimpan ke dalam history Git, dengan format perintah ``` git commit -m "komen perubahan bebas" ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20commit.png)

- Lalu melakukan remote dari terminal. Namun disini saya mengalami kendala pada saat menjalankan perintah ``` git remote add origin link_url_repository_git ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20remote.png)

- Kendala tersebut dikarenakan pada saat cloning repository saya memasukkan code url yang _https_, seharusnya saya memasukkan code url yang **SSH** (karna pada case ini sedang fokus penggunaan SSH)

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20remote%20v.png)

- Saya akan hapus remote yang ada dengan ketikkan perintah ``` git remote remove origin ``` dan menambahkan kembali perintah remote dengan code url **SSH** ``` git remote add origin link_url_repository_git ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20remote%20remove%20origin.png)

- Nah step terakhir (karna kendala sudah teratasi) push perubahan ke platform _GitHub_ dengan format perintah ``` git push -u origin nama_branch ```

  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/Pict/git%20push%20-u%20origin%20main.png)


# Thank You
