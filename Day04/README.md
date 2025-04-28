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
