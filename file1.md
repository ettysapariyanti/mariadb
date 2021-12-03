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

Perintah untuk memberi hak akses ke sebuah database terhadap seorang user :

```sql
GRANT ALL PRIVILEGES ON saham.* TO 'steven'@'%' IDENTIFIED BY 'tahugoreng';
```

Perintah untuk terkoneksi ke server MariaDB yang posisi fisiknya berada di remote, semisal di VPS yang ada di cloud, maka dari komputer pribadi jalankan perintah ini:

```sql
C:\xampp\mysql\bin\mysql.exe -h 100.100.100.100 -u steven -p
```


Contoh perintah untuk dump tabel datakomputer1 yang ada di dalam database ke file .sql, sehingga nantinya data-data di tabel datakomputer1 bisa di restore ke server MariaDB yg lain:

```sql
C:\xampp\mysql\bin\mysqldump.exe saham datakomputer1 > datakomputer1.sql
```








