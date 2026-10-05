# IMO Cam Manual & Rekap Bulanan — DAOP 1 Jakarta

Website mandiri menggunakan HTML, CSS, dan JavaScript. Tidak membutuhkan akun, database server, API key, atau instalasi paket JavaScript.

## Rekap foto satu bulan

Website pertama kali membuka **Rekap bulanan**. Bulan dan mode terakhir kemudian diingat agar pekerjaan yang dicicil bisa langsung dilanjutkan. Mode **Kamera satu foto** tetap tersedia pada tab di atas.

1. Pilih bulan dan petugas. Kalender menampilkan tanggal serta hari untuk seluruh bulan, termasuk bulan 28, 29, 30, atau 31 hari.
2. Pilih dinas untuk foto baru. Jika kumpulan foto sudah bertimestamp, aktifkan **Foto baru sudah bertimestamp**.
3. Tekan **Unggah banyak foto**, lalu pilih beberapa gambar. Foto diurutkan berdasarkan nama file (angka diurutkan secara alami: 1, 2, 10) dan dimasukkan ke tanggal kosong dari awal bulan. Satu tanggal memuat satu foto. Tanggal yang sudah berisi foto tidak ditimpa oleh unggah massal.
4. Periksa dan sesuaikan dinas/jam pada setiap kartu. Bisa juga memilih foto langsung pada tanggal tertentu melalui **Pilih / ganti foto**, atau menekan **Ambil foto** untuk mengambil selfie pada tanggal tersebut.
5. Klik gambar untuk membuka **Pratinjau hasil**. Di sini kamu dapat memindahkan foto ke tanggal lain, mengubah dinas dan jam, serta mengatur penutup timestamp lama. Pemindahan ke tanggal yang sudah terisi akan menukar kedua foto beserta pengaturannya.
6. Tekan **Unduh foto ini** untuk satu JPG, atau **Unduh … foto ZIP** untuk semua tanggal yang berisi foto. Paket berisi JPG 1200 × 1600 dan tabel `REKAP_YYYY-MM.csv`.

**Terapkan ke foto yang terisi** mengganti dinas foto kerja dalam bulan tersebut. Jam yang diatur manual dan tanggal LIBUR tetap dipertahankan; jam mode acak mengikuti rentang dinas baru.

Tanggal tanpa foto tetap kosong, kecuali jika ditandai LIBUR. Unggah massal melewati tanggal LIBUR. Bila file yang dipilih melebihi jumlah tanggal kerja kosong, file sisanya tidak dimasukkan dan jumlahnya ditampilkan. File rusak atau format tidak didukung juga dilaporkan. Maksimal ukuran tiap foto adalah 30 MB.

## Hari LIBUR

Pilih **LIBUR** pada menu dinas tanggal tertentu. Tanggal tersebut tidak memerlukan foto atau kamera. Kartu memakai poster KAI / OPERASI / DAOP 1 JAKARTA dari gambar yang diberikan, dengan nama, NIPP, jabatan, UPT, dan keterangan LIBUR. Tanggal serta nama hari mengikuti tanggal kartu. Jam tetap **17:16:39**, seperti contoh; tidak diacak.

Kartu LIBUR masuk ke unduhan ZIP dan tabel rekap. Poster mempertahankan bentuk potret asli dan diekspor berukuran **1200 × 2132**, sedangkan foto kerja tetap **1200 × 1600**. Jika tanggal sudah pernah memiliki foto, memilih LIBUR menyembunyikan foto tersebut; memilih dinas kembali memulihkan foto sebelumnya.

## Kamera per tanggal

Tekan **Ambil foto** pada tanggal kerja yang diinginkan. Kamera menampilkan pratinjau dengan tanggal, dinas, nama, serta jam yang sudah dipilih. Tekan **Ambil & simpan foto** untuk memasukkan hasil langsung ke tanggal itu. Kamera depan dicerminkan seperti pratinjau. Kamera dilepas saat dialog ditutup atau foto sudah diambil.

Bidang pandang kamera ditampilkan utuh, tanpa crop otomatis untuk memenuhi bingkai. Kamera tidak diminta memakai rasio potret tertentu; browser diminta mempertahankan rasio kamera jika mendukungnya. Jika rasio kamera berbeda dari 3:4, hasil memiliki tepi gelap agar gambar tetap utuh. Jika browser menyediakan pengaturan zoom yang sudah diizinkan, zoom dikembalikan ke nilai minimum kamera. Perilaku pilihan lensa tetap mengikuti perangkat dan browser.

Fitur ini membutuhkan HTTPS atau localhost, dan izin kamera browser. Gunakan **Go Live** di VS Code untuk menjalankannya di laptop. Jika kamera tidak tersedia, tetap bisa memilih foto dari perangkat pada tanggal tersebut.

## Foto yang sudah bertimestamp

Kode ini menutup area bawah dengan bidang gelap sebelum menambahkan timestamp baru. Aktifkan **Timestamp lama** pada kartu atau **Tutup timestamp lama** di pratinjau. Tinggi penutup dapat disesuaikan dari 19% sampai 45% foto. Periksa pratinjau karena posisi tulisan lama dapat berbeda untuk setiap gambar.

Bagian gambar yang tertutup tulisan lama tidak dipulihkan. Penutup juga menutupi bagian foto di area tersebut. Jika timestamp lama berada di luar area bawah, hasilnya perlu disesuaikan sebelum diunduh. Tidak ada pembacaan otomatis tanggal/dinas dari tulisan lama: tanggal dan dinas ditetapkan melalui kontrol website.

Pada foto yang sudah bertimestamp, penambahan logo KAI baru dimatikan secara bawaan untuk menjaga logo yang sudah ada. Aktifkan **Tambahkan logo KAI** jika sumber fotonya belum memiliki logo. Foto bersih memakai bidang transparan seperti template asli.

## Draf bulanan di perangkat

Foto asli, thumbnail, status LIBUR, tanggal, dinas, jam, dan pengaturan penutup disimpan otomatis di IndexedDB pada browser/perangkat yang sama. Menutup dan membuka kembali website memuat draf bulan terakhir. Mode **Kamera satu foto** juga menyimpan foto terakhir dan pengaturannya. Tidak ada server penyimpanan foto dan tidak perlu backend.

Gunakan alamat website yang sama setiap kali (termasuk port localhost yang sama) untuk memuat draf. Berpindah browser/perangkat, memakai mode privat, atau membersihkan data situs dapat menghapus akses ke draf. Unduh ZIP sebagai salinan hasil.

Jika penyimpanan diblokir atau ruang browser tidak cukup, status draf menampilkan keterbatasannya. Foto pada sesi yang masih terbuka tetap bisa diproses dan diunduh. Draf foto belum dianggap tersimpan sebelum status menampilkan **Draf tersimpan di perangkat**.

Setiap kartu juga menampilkan status penyimpanan. Kamu bisa mengisi satu atau beberapa tanggal hari ini lalu melanjutkan besok. Data ini berada di penyimpanan situs pada perangkat, bukan otomatis sebagai file di galeri/folder Downloads. Untuk mendapatkan file biasa, gunakan tombol unduh JPG atau ZIP.

## Cara paling mudah

1. Ekstrak ZIP. Semua file harus tetap berada di folder yang sama.
2. Buka `index.html` untuk melihat tampilan dan memakai **Pilih foto**.
3. Pilih petugas tersimpan atau isi nama dan NIPP, lalu tekan **Simpan Petugas**. Pilih tanggal foto dan dinas; nama hari muncul otomatis.
4. Ketik jam pada kolom **Jam pada foto**, atau tekan **Acak jam** untuk mengikuti rentang dinas.
5. Aktifkan kamera, ambil selfie, lalu tekan **Unduh foto JPG**. Foto hasilnya berukuran 1200 × 1600 piksel.

Kamera browser memerlukan alamat aman **HTTPS** atau **localhost**. Bila kamera tidak berjalan saat membuka file langsung, jalankan dengan cara di bawah. Pemilihan gambar tetap dapat dipakai langsung dari `index.html`.

## Menjalankan kamera di laptop

Jika Python sudah terpasang, buka terminal di folder ini dan jalankan:

```bash
python -m http.server 8000
```

Lalu buka `http://localhost:8000` di Chrome atau Edge. Di Windows kamu juga bisa mencoba `py -m http.server 8000`.

Alternatif di VS Code: buka folder ini, gunakan ekstensi Live Server, lalu pilih **Open with Live Server** pada `index.html`.

## Memasang di website sendiri

Upload seluruh file HTML/CSS/JS (`index.html`, `style.css`, `app.js`, `leave.js`, `monthly.js`, `daily-camera.js`, `zip.js`) dan folder `assets` ke direktori website kamu, misalnya `public_html/imocam/`. Buka alamatnya dengan **HTTPS**. Tidak ada proses build dan tidak memerlukan server backend.

Untuk selfie di HP, buka alamat HTTPS tersebut, izinkan akses kamera, lalu ambil foto. Membuka alamat IP laptop melalui HTTP dari HP biasanya tidak dapat mengakses kamera; gunakan hosting HTTPS.

## Ketentuan tanggal dan jam

| Dinas | Rentang jam acak |
| --- | --- |
| PAGI | 07:00:00 sampai 14:59:59 |
| SIANG | 15:00:00 sampai 21:59:59 |
| MALAM | 22:00:00 sampai 23:59:59 |

Tanggal pada hasil foto selalu mengikuti tanggal yang dipilih. Jam acak malam dibatasi sebelum 24:00 supaya tidak mengubah tanggal. Tanggal awal mengikuti Asia/Jakarta.

Jam dapat diketik manual (00:00:00–23:59:59) atau diacak mengikuti dinas. Mode **Manual** mempertahankan jam saat tanggal/dinas diganti. Tombol **Acak jam** mengaktifkan kembali mode **Acak**. Mengambil atau mengunduh foto tidak mengacak ulang jam.

## Simpan petugas

Nama dan NIPP bawaan adalah Andisa. Isi nama/NIPP lain, lalu tekan **Simpan Petugas**. Nama di foto otomatis memakai huruf besar. Menu **Petugas tersimpan** bisa dipakai memilih kembali petugas. Menyimpan NIPP yang sudah ada memperbarui namanya. Petugas terakhir yang disimpan/dipilih dimuat lagi saat halaman dibuka.

Data petugas tersimpan melalui localStorage di browser/perangkat yang sama. Data tidak disinkronkan antarperangkat dan dapat hilang saat data situs dibersihkan. Browser yang memblokir penyimpanan tetap bisa memakai petugas untuk sesi saat ini. Foto dan pengaturan draf disimpan otomatis melalui IndexedDB jika tersedia.

## Koordinat manual

Digit paling akhir latitude dan longitude dari template diberi variasi saat foto diambil atau dipilih. Contoh bentuknya tetap `-6.137646x, 106.8157x`. Tombol **Acak koordinat** mengganti variasi tanpa mengganti foto. Pratinjau dan unduhan menggunakan nilai yang sama; mengubah nama, tanggal, dan jam tidak mengacak koordinat. Ini merupakan data manual, bukan lokasi hasil GPS.

Dalam mode bulanan, setiap foto memiliki variasinya sendiri yang disimpan bersama draf. Mengekspor ulang ZIP mempertahankan koordinat dan jam yang sudah dipilih.

## Template dan nilai bawaan

Nama: ANDISA JATI APRILIA ABADI. NIPP: 76121. Jabatan: PLR. UPT: STASIUN JAKARTAKOTA. Lokasi: -6.1376467, 106.81578.

Logo kiri atas berasal dari template yang diberikan. Bidang gelap transparan dan enam baris teks mengikuti susunan foto referensi. Baris alamat menggunakan akhiran `KOTA JAKAR...` seperti referensi. Font memakai Courier New/monospace; hasil raster dapat sedikit berbeda dari font dan kompresi aplikasi asal.

Lokasi merupakan koordinat manual dengan variasi digit akhir, bukan pembacaan GPS. Waktu pada foto merupakan waktu manual, bukan waktu pengambilan yang terverifikasi. Website tidak mengubah EXIF foto asal. Foto diproses di browser dan tidak dikirim ke server oleh kode ini.

## Mengubah data dan tampilan

- `index.html`: struktur dan label tampilan.
- `style.css`: warna, ukuran, dan tata letak.
- `app.js`: nilai bawaan dalam `PROFILE`, daftar petugas, waktu manual/acak, dan jadwal dalam `SHIFT_WINDOWS`, kamera, dan penggambaran foto.
- `monthly.js`: kalender, unggah massal, IndexedDB, pratinjau, pemindahan tanggal, dan ekspor rekap.
- `leave.js` dan `assets/libur-template.jpg`: poster LIBUR asli beserta penggambaran data tanggal/petugas.
- `daily-camera.js`: kamera per tanggal serta penyimpanan/pemulihan foto mode individual.
- `zip.js`: penulisan arsip ZIP tanpa pustaka eksternal. File JPG sudah terkompresi sehingga disimpan langsung dalam arsip.
- `assets/kai.png`: salinan aset logo. Logo juga ditanam di `app.js` agar unduhan tetap berjalan saat file HTML dibuka langsung.

Foto kerja yang diunggah dipaskan dengan crop tengah ke rasio 3:4; kamera langsung menampilkan dan menyimpan seluruh bidang gambar dengan tepi gelap bila rasio berbeda. Poster LIBUR mempertahankan rasio aslinya. Kamera depan ditampilkan dan disimpan sebagai cermin; teks dan logo tetap terbaca normal. Sumber foto disimpan terpisah sehingga perubahan tanggal tidak menumpuk timestamp. Kedua mode menyimpan draf lokal bila penyimpanan tersedia.

Tema halaman memakai latar cerah dengan biru, mint, dan peach. Kartu foto beraksen mint, sedangkan kartu LIBUR beraksen peach. Warna tema dapat disesuaikan melalui variabel pada bagian awal `style.css`.
