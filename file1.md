## Catatan MariaDB

Berikut ini adalah perintah-perintah yg sering dipakai dalam menggunakan MariaDB . Untuk menginstal Mariadb di Debian 11, menggunakan perintah berikut :

```bash
apt install mariadb-server mariadb-client
```

Selanjutnya untuk membuat database, jalankan perintah:

```sql
CREATE DATABASE saham;
```

Setelah database selesai dibuat, maka kita akan membuat user, yg bisa memakai database itu. Untuk membuat user yg bisa mengakses database itu dari mana saja ( dari ip mana saja), maka kita jalankan perintah:

```sql
CREATE USER 'steven'@'%' IDENTIFIED BY 'tempegoreng';
```

Perintah untuk mengganti password dari user yg telah di buat:

```sql
ALTER USER 'steven'@'%' IDENTIFIED BY 'tahugoreng';
```



