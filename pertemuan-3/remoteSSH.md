#remote SSH dari AWS AC2 server

1. unduh dan install putty di https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

![alt text](image.png)

2. konversi ekstensi private key dari .pem menjadi .ppk
- buka putty gen
- load private key .pem
- klik save private key menjadi ekstensi file .ppk

![alt text](image-1.png)

3. setting-up remote SSH dengan putty
- isi Ipv4 addres public data berasal dari instance masing2
- port SSH (22)
- load private key .ppk di menu connection->auth->credential
- user dari instance masing2

![alt text](image-2.png)

4. setiap awal remote kita lakukan patching OS 
- sudo apt-get update && sudo apt-get upgrade

5. coba lakukan instalasi web server
- dalam keadaan kosong

![alt text](image-3.png)

- install salah satu web server
sudo apt install nginx

![alt text](image-4.png)
