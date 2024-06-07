# Tugas Praktikum { Pertemuan ke 12 } <img src=https://logos-download.com/wp-content/uploads/2016/05/MySQL_logo_logotype.png width="130px" >


|**Nama**|**NIM**|**Kelas**|**Matkul**|
|----|---|-----|------|
|Muhammad Arif Mulyanto|312310359|TI.23.A.5|Basis Data|

# Soal Latihan Praktikum 
# TABEL MAHASISWA
![k1](https://github.com/MuhArifyanto/mysql5/assets/147913440/acac967b-d3dd-4213-844b-213d6db32c56)
# TABEL DOSEN
![k2](https://github.com/MuhArifyanto/mysql5/assets/147913440/5560020c-0bb4-4649-a1a6-20eb59de6faf)
# TABEL MATKUL
![k3](https://github.com/MuhArifyanto/mysql5/assets/147913440/e819027f-cc9b-4157-a6b2-49414cd96a1b)
# TABEL JADWAL MENGAJAR
![k4](https://github.com/MuhArifyanto/mysql5/assets/147913440/95e8609d-9e1e-4851-8208-1ff7a3c88fc3)
# TABEL KRS MAHASISWA
![k5](https://github.com/MuhArifyanto/mysql5/assets/147913440/80fc21af-bc99-469f-b0c5-4469beda6ec7)

## Latihan

- Lakukan JOIN table Mahasiswa dan Dosen.
- Lakukan JOIN tabel Matakuliah dan Dosen.
- Lakukan JOIN table JadwalMengajar, Dosen, dan Matakuliah.
- Lakukan JOIN tabel KrsMahasiswa, Mahasiswa, Matakuliah, dan Dosen.

## Buat Script SQL JOIN Table berdasarkan skema data diatas.

```
INSERT INTO mahasiswa VALUES
    (1812345, 'Ari Santoso', 'L', '1999-10-11', NULL, 'Bekasi', NULL, NULL, 'DS002'),
    (1823456, 'Dina Marlina', 'P', '1998-11-20', NULL, 'Jakarta', NULL, NULL, NULL),
    (1834567, 'Rahmat Hidayat', 'L', '1999-05-10', NULL, 'Bekasi', NULL, NULL, NULL),
    (1845678, 'Jaka Sampurna', 'L', '2000-10-19', NULL, 'Cikarang', NULL, NULL, NULL),
    (1856789, 'Tia Lestari', 'P', '1999-02-15', NULL, 'Karawang', NULL, NULL, NULL),
    (1867890, 'Anton Sinaga', 'L', '1998-06-22', NULL, 'Bekasi', NULL, NULL, NULL),
    (1912345, 'Listia Nastiti', 'P', '2001-10-23', NULL, 'Jakarta', NULL, NULL, NULL),
    (1923456, 'Amira Jarisa', 'P', '2001-01-24', NULL, 'Karawang', NULL, NULL, 'DS004'),
    (1934567, 'Laksana Mardito', 'L', '1999-04-14', NULL, 'Cikarang', NULL, NULL, NULL),
    (1945678, 'Jura Marsina', 'P', '2000-05-10', NULL, 'Cikarang', NULL, NULL, NULL),
    (1956789, 'Dadi Martani', 'L', '2001-08-29', NULL, 'Bekasi', NULL, NULL, 'DS005'),
    (1967890, 'Bayu Laksono', 'L', '1999-07-22', NULL, 'Cikarang', NULL, NULL, 'DS004');
SELECT*FROM Mahasiswa;
`````
Output :
![k6](https://github.com/MuhArifyanto/mysql5/assets/147913440/d81f6c21-1349-4070-a126-c76b9dfd5599)

`````
insert into dosen values
    ("DS001", "Nofal Arianto"),
    ("DS002", "Ario Talib"),
    ("DS003", "Ayu Rahmadina"),
    ("DS004", "Ratna Kumala"),
    ("DS005", "Vika Prasetyo");
SELECT*FROM Dosen;
`````
Output :
![k7](https://github.com/MuhArifyanto/mysql5/assets/147913440/69497d2b-918c-46a8-a691-57a12f081bc9)


`````
INSERT INTO Matakuliah VALUES
('MK001', 'Algoritma Dan Pemrogaman', 3),
('MK002', 'Praktikum Algoritma Dan Pemrograman', 1),
('MK003', 'Teknologi Basis Data', 3),
('MK004', 'Praktikum Teknologi Basis Data', 1),
('MK005', 'Pemrograman Dasar', 3),
('MK006', 'Pemrograman Berorientasi Objek', 3),
('MK007', 'Struktur Data', 3),
('MK008', 'Arsitektur Komputer', 2);
SELECT * FROM Matakuliah;
`````
Output :
![k8](https://github.com/MuhArifyanto/mysql5/assets/147913440/77112223-29c3-4ebe-a6a8-5f77d2b70308)


`````
INSERT INTO JadwalMengajar VALUES
('MK001', 'DS002', 'Senin', '10:00:00', '102'),
('MK002', 'DS002', 'Senin', '13:00:00', 'Lab. 01'),
('MK003', 'DS001', 'Selasa', '08:00:00', '201'),
('MK004', 'DS001', 'Rabu', '10:00:00', 'Lab. 02'),
('MK005', 'DS003', 'Selasa', '10:00:00', 'Lab. 01'),
('MK006', 'DS004', 'Kamis', '09:00:00', 'Lab. 03'),
('MK007', 'DS005', 'Rabu', '08:00:00', '102'),
('MK008', 'DS005', 'Kamis', '13:00:00', '201');
SELECT*FROM JadwalMengajar;
`````
Output :
![k9](https://github.com/MuhArifyanto/mysql5/assets/147913440/cef291be-7a7e-4508-b6d4-03433d548eec)


`````
INSERT INTO KRSMahasiswa VALUES
(1823456, 'MK001', 'DS002', 3, NULL),
(1823456, 'MK002', 'DS002', 1, NULL),
(1823456, 'MK003', 'DS001', 3, NULL),
(1823456, 'MK004', 'DS001', 3, NULL),
(1823456, 'MK007', 'DS005', 3, NULL),
(1823456, 'MK008', 'DS005', 3, NULL);
SELECT * FROM KRSMahasiswa;
`````
Output :
![k10](https://github.com/MuhArifyanto/mysql5/assets/147913440/0176100d-04d6-42e6-86c0-85e5e7a1feee)


# Latihan
- JOIN table Mahasiswa dan Dosen
`````
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jk, Dosen.nama AS "Dosen PA"
FROM Mahasiswa INNER JOIN Dosen ON Dosen.kd_ds = Mahasiswa.kd_ds;
`````
Output :
![k11](https://github.com/MuhArifyanto/mysql5/assets/147913440/268685e6-d9bf-4a0c-9d84-f57b9c606638)


- LEFT JOIN table Mahasiswa dan Dosen
`````
SELECT Mahasiswa.nim, Mahasiswa.nama, Mahasiswa.jk, Dosen.nama AS "Dosen PA"
FROM Mahasiswa LEFT JOIN Dosen ON Dosen.kd_ds = Mahasiswa.kd_ds;
`````
Output:
![k12](https://github.com/MuhArifyanto/mysql5/assets/147913440/d2c829ab-eae0-4e69-97ed-d804dd83cd00)


- JOIN table JadwalMengajar, Dosen, dan Matakuliah
`````
SELECT Matakuliah.kd_mk, Matakuliah.nama, Matakuliah.sks, Dosen.nama AS "Dosen Pengampu"
FROM JadwalMengajar
LEFT JOIN Matakuliah ON JadwalMengajar.kd_mk = Matakuliah.kd_mk
LEFT JOIN Dosen ON JadwalMengajar.kd_ds = Dosen.kd_ds;
`````
Output:
![k13](https://github.com/MuhArifyanto/mysql5/assets/147913440/3e1fdd23-a8ad-4fa9-abce-49fced998f08)


- JOIN table JadwalMengajar, Dosen, dan Matakuliah
`````
SELECT Matakuliah.kd_mk, Matakuliah.nama, Matakuliah.sks, Dosen.nama AS "Dosen Pengampu", JadwalMengajar.hari, JadwalMengajar.jam, JadwalMengajar.ruang
FROM JadwalMengajar
LEFT JOIN Matakuliah ON JadwalMengajar.kd_mk = Matakuliah.kd_mk
LEFT JOIN Dosen ON JadwalMengajar.kd_ds = Dosen.kd_ds;
`````
Output :
![k14](https://github.com/MuhArifyanto/mysql5/assets/147913440/39a3eb71-91df-4749-a208-0626f8b2391d)


- JOIN tabel KRSMahasiswa, Mahasiswa, Matakuliah, dan Dosen
`````
SELECT Mahasiswa.nim, Mahasiswa.nama AS "nama", Dosen.nama AS "Dosen PA", Matakuliah.nama AS "Matakuliah", Matakuliah.sks, Dosen.nama AS "Dosen Pengampu"
FROM KRSMahasiswa
JOIN Mahasiswa ON KRSMahasiswa.nim = Mahasiswa.nim
JOIN Matakuliah ON KRSMahasiswa.kd_mk = Matakuliah.kd_mk
JOIN Dosen ON KRSMahasiswa.kd_ds = Dosen.kd_ds;
`````
Output :
![k15](https://github.com/MuhArifyanto/mysql5/assets/147913440/bf2b3e96-0cf8-4c72-9809-219846c7c049)

