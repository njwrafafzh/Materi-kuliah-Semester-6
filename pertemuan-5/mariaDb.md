# setting up database di aws ec2 menggunakan mariadb

1. Aktifkan Instance AWs Ec2
2. Remote Instance Via Open SSH Powershell / putty
3. Patching OS (sudo apt-get update && sudo apt-get upgrade)
4. Install MariaDb (sudo apt install mariadb-server -y)
5. Cek Status MariaDb (systemctl status mariadb)
![alt text](image.png)


6. test default setting database server login (sudo mysql -u root -p)
![alt text](image-1.png)


7. Hardening Database Server (sudo mysql_secure_installation)
-Change the password for the root user = Y
-Remove anonymous users = Y
-Disallow root login remotely = Y
-Remove test database and access to it = Y
-Reload privilege tables = Y 
![alt text](image-2.png)


8. create db untuk website company profile
-login sebagai root
-create db nama compro_nim
![alt text](image-3.png)

-Create User dengan nama = usrcompro_NIM dan password = [PASSWORD] => CREATE USER 'usrcompro_NIM'@'localhost' IDENTIFIED BY '[PASSWORD]';
![alt text](image-3.png)

-Grant user akses ke DB yang baru dibuat => GRANT ALL PRIVILEGES ON dbcompro_NIM.* TO 'usrcompro_NIM'@'localhost';
-Flush privileges => FLUSH PRIVILEGES;
-exit;
![alt text](image-5.png)


