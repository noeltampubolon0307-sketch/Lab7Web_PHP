# Praktikum 7: PHP Dasar - Pemrograman Web
 
Repository ini dibuat untuk memenuhi tugas **Praktikum 7 Pemrograman Web** di **Universitas Pelita Bangsa**.
 
## Identitas Mahasiswa
 
| Keterangan | Data |
|---|---|
| **Nama** | Noel Marihot Tampubolon |
| **Kelas** | I251D |
| **NIM** | 312510419 |
| **Mata Kuliah** | Pemrograman Web |
 
---
 
## 1. Tujuan Praktikum
 
Tujuan dari praktikum ini adalah sebagai berikut:
 
1. Menjalankan PHP di server lokal dan membuka hasilnya di browser.
2. Menggunakan variabel, operator, percabangan (`if / elseif / else`), array, dan `foreach`.
3. Membuat dan memanggil `function` dengan parameter dan nilai kembalian.
4. Memproses input form dengan metode GET dan POST, termasuk validasi dan pengamanan output dengan `htmlspecialchars()`.
5. Mengembangkan program secara mandiri melalui lima eksperimen mandiri.
---
 
## 2. Perangkat yang Digunakan
 
Perangkat yang digunakan pada praktikum ini adalah sebagai berikut:
 
| Kebutuhan | Keterangan |
|---|---|
| **PHP** | Interpreter PHP (paket XAMPP atau instalasi PHP mandiri) |
| **Web Server** | Apache dari XAMPP, atau server bawaan PHP (`php -S`) |
| **Editor** | Visual Studio Code |
| **Browser** | Google Chrome |
 
---
 
## 3. Cara Menjalankan Server Lokal
 
### Opsi 1: XAMPP (Apache)
 
1. Salin folder proyek ke `htdocs`, misalnya `C:\xampp\htdocs\Lab7_php`.
2. Buka XAMPP Control Panel, lalu klik **Start** pada modul **Apache**.
3. Buka alamat berikut di browser:
   - `http://localhost/Lab7_php/` untuk `index.php`
   - `http://localhost/Lab7_php/MiniProject/form_mahasiswa.php` untuk formulir mahasiswa
### Opsi 2: Server Bawaan PHP
 
```bash
cd Lab7_php
php -S localhost:8000
```
 
Lalu buka `http://localhost:8000/` dan `http://localhost:8000/MiniProject/form_mahasiswa.php`.
 
---
 
## 4. Struktur File
 
Struktur file pada praktikum ini adalah sebagai berikut:
 
```text
Lab7_php/
├── index.php                  # Materi 1-7 dan eksperimen 1-3
├── MiniProject/
│   └── form_mahasiswa.php     # Form data mahasiswa, eksperimen 4-5
├── images/                    # Tangkapan layar untuk README
└── README.md
```
 
---
 
## 5. Ringkasan Hasil
 
### 5.1 Halaman PHP Pertama
 
`index.php` menampilkan teks dan waktu server menggunakan `echo` dan `date()`.
 
<img width="576" height="305" alt="php 2" src="https://github.com/user-attachments/assets/ec0a2428-c6a8-4fc1-bc44-56a14b413ba5" />

 
<img width="304" height="142" alt="php 1" src="https://github.com/user-attachments/assets/3b61c18c-b525-4af7-b589-b129d80d2431" />

 
### 5.2 Variabel dan Percabangan: Nilai Akhir dan Predikat
 
Nilai akhir dihitung dari bobot tugas, UTS, dan UAS, kemudian predikat ditentukan dengan `if / elseif / else` (A ≥ 85, B ≥ 75, C ≥ 60, selain itu D). Bobot diubah-ubah untuk melihat pengaruhnya terhadap hasil:
 
| Bobot (Tugas / UTS / UAS) | Nilai Akhir | Predikat |
|---|---|---|
| 0,30 / 0,30 / 0,40 | 84,90 | B |
| 0,20 / 0,10 / 0,30 | 51,80 | D |
| 0,35 / 0,50 / 0,30 | 95,75 | A |
| 0,25 / 0,30 / 0,30 (awal) | 71,65 | C |
 
**Kesimpulan:** perubahan bobot mengubah nilai akhir dan predikat, karena kondisi `if` dievaluasi ulang setiap halaman dijalankan.
----

### Sebelum diganti bobot nilainya 

<img width="654" height="520" alt="php 5" src="https://github.com/user-attachments/assets/953b0961-e0f5-4b8e-8d1f-1bfd6ce5ca5f" />

<img width="273" height="230" alt="php 6" src="https://github.com/user-attachments/assets/789983a8-7e48-4312-861f-5d93a8043ef1" />


Sesudah bobobt nilainya di ganti

<img width="654" height="521" alt="php 3" src="https://github.com/user-attachments/assets/1e7d878e-2da1-49a2-bf06-f617787768f5" />

<img width="262" height="235" alt="php 4" src="https://github.com/user-attachments/assets/67b751bd-94d5-4886-91a0-0f067a2f612a" />
 
### 5.3 Array dan `foreach`
 
Daftar mahasiswa disimpan dalam array dan ditampilkan sebagai daftar bernomor (`<ol>`) menggunakan `foreach`.
 
<img width="703" height="286" alt="php 7" src="https://github.com/user-attachments/assets/18d447d5-46b8-42d3-aa4e-305e6ad46c59" />

<img width="206" height="196" alt="php 8" src="https://github.com/user-attachments/assets/388fd580-66fa-4019-8a61-25c452bb7325" />


 
### 5.4 Function
 
Tiga function dibuat dan dipanggil:
 
- `hitungDiskon()` menghasilkan Rp135.000 untuk harga 150.000 dengan diskon 10%.
- `hitungLuasPersegiPanjang()` menghasilkan 50 untuk panjang 10 dan lebar 5.
- `cekKelulusan()` menghasilkan "Lulus" untuk nilai 80.
  
<img width="632" height="382" alt="php 9" src="https://github.com/user-attachments/assets/811b0442-47f6-4ad6-8375-ecaf5bd05632" />

<img width="238" height="95" alt="php 10" src="https://github.com/user-attachments/assets/88f01d1d-c557-4776-b7c1-1234c83c9bd4" />


 
### 5.5 Form GET
 
Kata kunci dikirim melalui URL (`?kata=Buku`) dan dibaca dengan `$_GET`. Data GET terlihat pada address bar browser.
 
<img width="634" height="210" alt="php 11" src="https://github.com/user-attachments/assets/1388a10b-a102-4bec-b67d-a8daebd00f14" />

<img width="310" height="59" alt="php 12" src="https://github.com/user-attachments/assets/cb42955b-c998-4c05-a904-b216d477b523" />


 
### 5.6 Form POST dan Keamanan Output
 
Form nama dan program studi dikirim dengan `POST`, lalu divalidasi agar tidak kosong. Input berisi tag HTML (`<"halo">`) ditampilkan apa adanya sebagai teks karena dilewatkan ke `htmlspecialchars()`, sehingga tidak dieksekusi sebagai HTML (pencegahan XSS).
 
<img width="698" height="499" alt="php 13" src="https://github.com/user-attachments/assets/c7f1c469-a5f6-4886-b33a-87ee989c6ab4" />

 
<img width="593" height="171" alt="php 14" src="https://github.com/user-attachments/assets/0e64defb-d1cd-4035-b322-c1e70603a11a" />

 
### 5.7 Form Subtotal dan Validasi
 
Subtotal dihitung dari harga × jumlah dan ditampilkan dengan `number_format()` (contoh 2500,50 × 2 = Rp5.001). Jumlah 0 atau negatif ditolak oleh validasi browser (`min="1"`), dan PHP tetap memeriksa ulang di sisi server.
 
<img width="680" height="599" alt="php 15" src="https://github.com/user-attachments/assets/2b075360-df14-4cc5-b673-71d8ba789430" />

<img width="769" height="151" alt="php 16" src="https://github.com/user-attachments/assets/eabe67db-4b99-49e6-95b3-ad82bbb8ab8d" />

<img width="804" height="150" alt="php 17" src="https://github.com/user-attachments/assets/b2f20df0-7450-4d17-b98b-bb7a521273a4" />

<img width="788" height="145" alt="php 18" src="https://github.com/user-attachments/assets/e531fa24-1bc5-4141-ab2e-878d0e10b776" />

 
### 5.8 Mini Project: Formulir Data Mahasiswa
 
`MiniProject/form_mahasiswa.php` menerima nama, NIM, program studi, semester (1-14), dan email. Data divalidasi di server, lalu ditampilkan jika semua valid.
 
<img width="557" height="269" alt="php 20" src="https://github.com/user-attachments/assets/83e18f2d-8dac-4a70-80d0-64be2f517f69" />

<img width="341" height="520" alt="php 21" src="https://github.com/user-attachments/assets/042a9ded-3130-4484-a230-41829fb78031" />


 
---
 
## 6. Eksperimen Mandiri
 
Ringkasan lima eksperimen mandiri adalah sebagai berikut:
 
| No | Eksperimen | File | Hasil |
|---|---|---|---|
| 1 | Rata-rata tiga komponen nilai | `index.php` | `($tugas + $uts + $uas) / 3`, ditampilkan di bawah nilai akhir |
| 2 | GET mencari nama dari array | `index.php` | `array_filter()` + `stripos()`, tidak membedakan huruf besar/kecil |
| 3 | Function format Rupiah | `index.php` | `formatRupiah()` dipakai untuk harga diskon dan subtotal (contoh Rp25.000) |
| 4 | Validasi NIM | `form_mahasiswa.php` | Hanya angka dan tepat 10 digit (`$panjangNim`), dicek di PHP dan HTML |
| 5 | Tombol reset | `form_mahasiswa.php` | `<button type="reset">`, mengosongkan isian tanpa request ke server |
 
### 6.1 Eksperimen 1: Rata-rata Nilai
 
<img width="707" height="614" alt="php 22" src="https://github.com/user-attachments/assets/95864f3a-4179-4f23-a1a6-4a258a95364c" />

<img width="329" height="447" alt="php 23" src="https://github.com/user-attachments/assets/06137c15-aa2f-4e9d-b93c-1e953f7a2c01" />


 
### 6.2 Eksperimen 2: Pencarian Nama dengan GET
 
<img width="650" height="346" alt="php 24" src="https://github.com/user-attachments/assets/178f0f17-6669-4677-bff1-ed7386d2856d" />

<img width="256" height="283" alt="php 25" src="https://github.com/user-attachments/assets/144afe59-aa62-4c03-9322-b3e0e3d3cb34" />


 
### 6.3 Eksperimen 3: Function Format Rupiah
 
<img width="707" height="97" alt="Screenshot 2026-11-12 163038" src="https://github.com/user-attachments/assets/3124b30f-738e-45ea-af13-cd56d6c1aa5e" />

<img width="795" height="147" alt="php 26" src="https://github.com/user-attachments/assets/bad441b5-9634-4fe0-9a12-120ec9b08eb6" />


 
### 6.4 Eksperimen 4: Validasi NIM
 
<img width="638" height="598" alt="php 27" src="https://github.com/user-attachments/assets/dd96f1cf-bad1-4c4f-af15-4aebe13e0116" />

<img width="337" height="298" alt="php 28" src="https://github.com/user-attachments/assets/5b2e2c9a-da83-48ba-bd86-ccdb4ec581a4" />



 
### 6.5 Eksperimen 5: Tombol Reset
 
<img width="859" height="480" alt="php 29" src="https://github.com/user-attachments/assets/e6ba4aad-2c99-40dd-aac7-ff9c792ae3f3" />

<img width="350" height="308" alt="php 30" src="https://github.com/user-attachments/assets/79a7b180-282f-49cf-8593-f1c7d739e78b" />


 
**Perbedaan tombol Reset dan pemrosesan ulang di server:**
 
| | Reset | Kirim (pemrosesan di server) |
|---|---|---|
| Tempat kerja | Browser (sisi klien) | Server PHP |
| Request ke server | Tidak ada | Ada (HTTP POST) |
| Efek | Isian form kembali ke nilai awal | Data divalidasi, halaman dibuat ulang |
| Hasil di bawah form | Tidak berubah | Diperbarui |
 
Menekan Reset hanya mengosongkan isian. Pesan hasil atau error yang sudah dibuat server pada request sebelumnya tetap tampil sampai halaman dimuat ulang atau form dikirim lagi.
 
---
 
## 7. Catatan
 
- Semua output dari input pengguna dilewatkan ke `htmlspecialchars()`.
- Validasi di browser (`required`, `min`, `pattern`) hanya membantu pengguna. Validasi yang menentukan tetap dilakukan di PHP.
