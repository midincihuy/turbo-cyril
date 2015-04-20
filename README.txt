Installasi Openfire Server Chatting :
Paket yang dibutuhkan :
1. openfire_3_7_1-userservice.tar.gz
2. openfired

Langkah :
1. ekstrak file openfire_3_7_1.tar.gz dengan sintaks :
     # tar -xzvf openfire_3_7_1-userservice.tar.gz 
2. salin hasil ekstrak ke folder /opt
     # mv openfire /opt
3. salin file openfired ke /etc/init.d
     # cp openfired /etc/init.d 
4. buat openfired jadi service
     # chkconfig --add openfired
     # chkconfig --level 35 openfired on
5. openfire bisa dijalankan dengan command : 
          # service openfired start|stop|status

Mysql :
1. Create Database dengan nama openfire

Konfigurasi :
1. Buka browser ke url http://ip_address:9090/
2. pilih english untuk bahasa lalu klik continue (OP_Lang.png)
3. isi domain dengan chatting lalu klik continue (OP_Domain.png)
4. pilih standard database connection lalu klik continue (OP_Database.png)
5. pilih database driver presets = mysql lalu isi database url dengan alamat database yang sudah di buat tadi, contoh => jdbc:mysql://localhost:3306/openfire lalu masukkan username dan password database, lalu klik continue (OP_Database_Config.png)
6. pilih default lalu klik continue (OP_Profile.png)
7. isi password untuk admin lalu klik continue atau skip this step jika tidak ingin mengeset password untuk admin (OP_Admin.png)
8. klik login to the admin console untuk masuk ke halaman admin dari openfire (OP_Complete.png)
9. login ke halaman admin openfire menggunakan username admin dan password yang sudah dibuat sebelumnya
10. klik menu server settings, lalu pilih user service.
11. pilih enabled lalu tentukan secret key(secret key ini berguna saat melakukan request user service melalui HTTP) lalu klik save setting (OP_Setting_User_Service.png)



