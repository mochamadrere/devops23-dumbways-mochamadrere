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
