# MY-SQL-PART-2

			- CODING DATABASE PROGRAM CONTOH " MAHASISWA " PART #2 -

mysql> create database mahasiswa;

mysql> use mahasiswa;

mysql> show databases;

mysql> create table biodata
    -> (nim varchar(10)primary key,
    -> nama varchar (20) not null,
    -> alamat_jalan varchar(20) not null,
    -> kota varchar(15) not null,
    -> kode_pos varchar(15) not null,
    -> no_hp varchar(15) not null,
    -> jenis_kelamin varchar(15) not null,
    -> kode_dosen varchar(20) not null);

mysql> desc biodata;

mysql> alter table biodata
    -> add tanggal_lahir date after jenis_kelamin;


mysql> desc biodata;

mysql> insert into biodata
    -> (nim, nama, alamat_jalan, kota, kode_pos, no_hp, jenis_kelamin, tanggal_lahir, kode_dosen)
    -> values
    -> ("11223344","ari santoso"," ","bekasi"," "," ","laki-laki","1998-10-12"," "),
    -> ("11223345","ario talib"," ","cikarang"," "," ","laki-laki","1998-11-16"," "),
    -> ("11223346","dina marlina"," ","karawang"," "," ","perempuan","1997-12-01"," ");


mysql> select * from biodata;

mysql> insert into biodata
    -> values
    -> ("11223347","lisa ayu"," ","bekasi"," "," ","perempuan","1996-01-02"," "),
    -> ("11223348","tiara wahidah"," ","bekasi"," "," ","perempuan","1998-02-05"," "),
    -> ("11223349","anton sinaga"," ","cikarang"," "," ","laki laki","1998-03-10"," ");


mysql> select *from biodata;

mysql> update biodata set tanggal_lahir = "1979-08-31" where nim = " 11223344";

mysql> select *from biodata;

mysql> select *from biodata where nim = "11223344";

mysql> delete from biodata where nim = "11223346";

mysql> select *from biodata;

mysql> select *from biodata
    -> where tanggal_lahir >= "1998-11-16";

mysql> select nama, kota, jenis_kelamin from biodata
    -> where kota = "bekasi"
    -> and jenis_kelamin = "perempuan";

mysql> select *from biodata
    -> where kota = "bekasi" and jenis_kelamin = "laki-laki"
    -> or tanggal_lahir <="1997" and jenis_kelamin = "perempuan";

mysql> select nama, alamat_jalan from biodata;

mysql> select *from biodata
    -> order by nama asc;
	
	- SELESAI -
