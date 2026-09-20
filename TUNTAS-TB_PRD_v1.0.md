# PRODUCT REQUIREMENTS DOCUMENT

## TUNTAS-TB

**Versi:** 1.0  
**Status:** Product blueprint untuk prototipe kompetisi  
**Kategori:** Teknologi kesehatan / pendampingan pengobatan tuberkulosis  
**Platform:** Web app petugas + WhatsApp pasien  
**Bahasa utama:** Bahasa Indonesia  
**Prinsip:** Teknologi membaca sinyal dan membantu prioritisasi; keputusan medis tetap pada tenaga kesehatan.

---

## 1. Ringkasan Produk

TUNTAS-TB adalah sistem pendampingan digital adaptif untuk membantu petugas layanan primer mengenali pasien tuberkulosis yang mulai menghadapi hambatan pengobatan. Pasien tidak diwajibkan mengunduh aplikasi. Interaksi harian berlangsung melalui WhatsApp, sedangkan petugas menggunakan web app untuk memantau respons, meninjau tingkat prioritas, dan mencatat tindak lanjut.

Produk tidak dimaksudkan untuk memastikan secara klinis bahwa obat telah ditelan, mendiagnosis efek samping, mengganti regimen, atau memberikan keputusan medis otomatis. Respons pasien diperlakukan sebagai **sinyal pendampingan** yang perlu diverifikasi manusia.

### Nilai utama

TUNTAS-TB mengubah pendampingan dari pengingat seragam menjadi alur:

**check-in singkat → identifikasi hambatan → prioritas risiko → dukungan yang relevan → tindak lanjut petugas.**

---

## 2. Masalah yang Diselesaikan

Pengobatan TB berlangsung berbulan-bulan. Selama proses tersebut, pasien dapat lupa, kehabisan obat, merasa tidak nyaman setelah minum obat, kesulitan datang ke fasilitas kesehatan, mengalami stigma, atau mulai lelah menjalani terapi. Pemantauan manual dapat terlambat mengenali perubahan ini, sedangkan pengingat digital biasa hanya menanyakan apakah pasien sudah minum obat.

TUNTAS-TB berfokus pada satu kesenjangan: **petugas belum selalu mengetahui alasan di balik perubahan keterlibatan pasien cukup dini untuk memberikan dukungan yang tepat.**

---

## 3. Tujuan Produk

### Tujuan utama

Membantu petugas TB mendeteksi dan menindaklanjuti hambatan pengobatan lebih awal dengan memanfaatkan kanal yang sudah familier bagi pasien.

### Tujuan operasional

1. Memudahkan pasien melakukan check-in tanpa mengunduh aplikasi baru.
2. Mengidentifikasi jenis hambatan, bukan hanya mencatat jawaban ya atau tidak.
3. Menyusun antrean tindak lanjut berdasarkan tingkat prioritas.
4. Memperpendek waktu antara munculnya sinyal risiko dan kontak petugas.
5. Menyimpan jejak tindak lanjut yang ringkas dan dapat diaudit.
6. Mengurangi beban petugas dengan tampilan berbasis tindakan, bukan kumpulan grafik.

### Non-goals

TUNTAS-TB tidak:

- mendiagnosis TB atau kondisi medis lain;
- mengubah atau merekomendasikan dosis dan regimen;
- menyatakan kepatuhan berdasarkan satu jawaban pasien;
- menggantikan petugas TB, dokter, perawat, PMO, atau layanan darurat;
- mengirimkan data klinis lengkap melalui pesan WhatsApp;
- memakai AI generatif untuk membuat saran medis;
- menjadi rekam medis elektronik utama.

---

## 4. Pengguna dan Peran

| Peran | Kebutuhan utama | Kanal |
|---|---|---|
| Pasien TB | Check-in cepat, bahasa aman, bantuan sesuai hambatan | WhatsApp |
| Petugas TB | Mengetahui siapa yang perlu dihubungi dan mengapa | Web app |
| Dokter/perawat | Menerima eskalasi yang membutuhkan penilaian klinis | Web app dan prosedur fasilitas |
| PMO/pendamping | Mendukung pasien sesuai persetujuan dan kewenangan | Tindak lanjut manusia |
| Admin fasilitas | Mengelola akun, template, jam layanan, dan audit akses | Web app |

### Batas peran

- Pasien tidak memiliki dashboard klinis.
- Petugas TB hanya melihat pasien pada fasilitasnya.
- Dokter/perawat menangani eskalasi klinis sesuai SOP.
- Admin tidak boleh mengubah catatan tindak lanjut klinis tanpa jejak audit.

---

## 5. Prinsip Pengalaman Produk

1. **Tenang, bukan menakutkan.** Bahasa tidak menghakimi pasien.
2. **Berbasis tindakan.** Halaman utama menjawab: siapa yang perlu dihubungi hari ini?
3. **Privasi sejak tampilan pertama.** Diagnosis tidak muncul di notifikasi terbuka.
4. **Satu tugas utama per layar.** Hindari dashboard penuh kartu dan angka dekoratif.
5. **Tidak berpura-pura cerdas.** Mesin aturan harus dapat dijelaskan kepada petugas.
6. **Manusia memegang keputusan.** Sistem menyarankan prioritas, bukan tindakan medis.
7. **Dapat dipakai pada perangkat sederhana.** Antarmuka ringan dan responsif.

---

## 6. Ruang Lingkup MVP

### Alur inti yang wajib berfungsi

1. Petugas masuk ke web app.
2. Petugas mendaftarkan pasien dengan persetujuan yang tercatat.
3. Jadwal check-in dibuat berdasarkan jadwal pendampingan.
4. Sistem mengirim template WhatsApp yang netral.
5. Pasien menjawab melalui tombol atau angka sederhana.
6. Webhook menerima dan menyimpan respons.
7. Mesin aturan memperbarui tingkat prioritas.
8. Dashboard menampilkan alasan prioritas dengan bahasa yang dapat dijelaskan.
9. Petugas membuka detail pasien, menghubungi pasien, dan mencatat hasil.
10. Status kasus berubah menjadi dipantau, ditindaklanjuti, dirujuk, atau selesai.

### Fitur MVP

- autentikasi petugas;
- pengelolaan fasilitas dan peran;
- registrasi pasien dengan identitas minimum;
- pencatatan persetujuan WhatsApp;
- pengaturan jadwal check-in;
- pengiriman dan penerimaan pesan WhatsApp;
- check-in harian satu ketukan;
- pemetaan hambatan;
- mesin aturan prioritas hijau, kuning, merah;
- antrean tindak lanjut;
- detail pasien dan lini masa respons;
- catatan tindak lanjut;
- pengaturan template pesan;
- log aktivitas;
- Mode Demo tanpa kredensial WhatsApp nyata;
- ekspor data agregat tanpa identitas langsung.

### Di luar MVP

- AI diagnosis atau triase klinis;
- computer vision/video minum obat;
- integrasi langsung ke SATUSEHAT atau SITB tanpa persetujuan dan spesifikasi resmi;
- aplikasi pasien terpisah;
- prediksi berbasis machine learning;
- konsultasi video;
- pembayaran dan asuransi;
- pelacakan lokasi pasien.

---

## 7. Arsitektur Informasi Web App

### Navigasi utama

1. **Hari Ini**
2. **Pasien**
3. **Tindak Lanjut**
4. **Pesan**
5. **Laporan**
6. **Pengaturan**

### 7.1 Hari Ini

Halaman utama tidak memakai hero promosi. Bagian teratas berisi tanggal, nama fasilitas, dan kalimat operasional: **“Ada 4 pasien yang perlu ditinjau hari ini.”**

Komponen:

- antrean prioritas merah;
- antrean prioritas kuning;
- check-in belum masuk;
- tindak lanjut jatuh tempo;
- ringkasan singkat tujuh hari;
- tombol utama: **Tinjau pasien berikutnya**.

### 7.2 Pasien

Daftar dapat dicari dan difilter berdasarkan:

- nama/kode pasien;
- fase pendampingan;
- prioritas;
- status check-in;
- petugas penanggung jawab;
- status aktif atau selesai.

Setiap baris menampilkan informasi yang dapat ditindaklanjuti: kode/nama tersamarkan, prioritas, hambatan terakhir, waktu respons terakhir, dan petugas.

### 7.3 Detail Pasien

Susunan layar:

1. identitas ringkas dan status persetujuan;
2. alasan pasien masuk antrean;
3. tindakan yang tersedia;
4. lini masa check-in dan tindak lanjut;
5. pola hambatan;
6. jadwal pendampingan;
7. catatan internal;
8. riwayat perubahan data.

Tombol utama:

- Hubungi melalui WhatsApp;
- Tandai sudah dihubungi;
- Catat hasil;
- Eskalasi ke tenaga klinis;
- Atur check-in berikutnya.

### 7.4 Tindak Lanjut

Tampilan berupa daftar kerja, bukan kalender penuh. Setiap item memiliki:

- pasien;
- penyebab eskalasi;
- tenggat;
- penanggung jawab;
- status;
- hasil terakhir.

### 7.5 Pesan

Menampilkan status pesan: dijadwalkan, dikirim, diterima, dibaca bila tersedia, dibalas, dan gagal. Pesan medis sensitif tidak boleh muncul sebagai preview panjang.

### 7.6 Laporan

Laporan MVP hanya berisi indikator proses:

- tingkat respons check-in;
- distribusi hambatan;
- jumlah eskalasi;
- median waktu respons petugas;
- status tindak lanjut;
- jumlah pasien aktif;
- kegagalan pengiriman pesan.

Laporan tidak boleh mengklaim keberhasilan klinis sebelum penelitian dilakukan.

### 7.7 Pengaturan

- profil fasilitas;
- anggota dan peran;
- jam operasional;
- aturan eskalasi;
- template pesan;
- koneksi WhatsApp;
- retensi dan ekspor data;
- audit akses.

---

## 8. Alur WhatsApp Pasien

### 8.1 Persetujuan awal

Petugas menjelaskan tujuan, jenis data, siapa yang dapat mengakses, cara berhenti, serta batas fungsi sistem. Persetujuan dicatat sebelum pesan rutin diaktifkan.

### 8.2 Pesan pembuka netral

> Halo, ini pengingat pendampingan kesehatan Anda. Bagaimana jadwal hari ini?
>
> 1. Sudah sesuai jadwal  
> 2. Belum sesuai jadwal  
> 3. Saya membutuhkan bantuan

Pesan tidak menyebut TB, nama obat, atau diagnosis pada notifikasi awal.

### 8.3 Jika pasien memilih “Belum sesuai jadwal”

> Terima kasih sudah menjawab. Apa hambatan utamanya?
>
> 1. Lupa  
> 2. Merasa tidak nyaman setelah minum obat  
> 3. Obat hampir habis/habis  
> 4. Sulit datang ke layanan  
> 5. Sedang lelah atau ingin berhenti  
> 6. Lainnya

### 8.4 Respons berdasarkan hambatan

- **Lupa:** tawarkan perubahan jam pengingat.
- **Tidak nyaman:** berikan pesan keselamatan netral dan masukkan ke tinjauan petugas; tidak memberi diagnosis.
- **Obat habis:** tandai kebutuhan koordinasi obat.
- **Akses layanan:** masukkan ke tindak lanjut logistik.
- **Ingin berhenti:** prioritas tinggi dan tindak lanjut manusia.
- **Lainnya:** simpan jawaban singkat dan masukkan ke tinjauan.

### 8.5 Kata kunci keselamatan

Kata seperti `BANTUAN`, `PETUGAS`, dan `BERHENTI` selalu menawarkan koneksi ke petugas. Kata `DARURAT` menampilkan arahan layanan darurat yang telah disetujui fasilitas. Chatbot tidak melakukan percakapan medis terbuka.

### 8.6 Berhenti menerima pesan

Pasien dapat mengetik `STOP`. Sistem meminta konfirmasi, menghentikan pesan otomatis, dan membuat tugas bagi petugas agar kesinambungan pendampingan tetap terjaga melalui kanal lain.

---

## 9. Mesin Aturan Prioritas

Mesin MVP bersifat **rule-based**, transparan, dan dapat diaudit. Tidak memakai model AI generatif.

### Sinyal masukan

- check-in diterima atau tidak;
- jawaban pasien;
- hambatan yang dipilih;
- pengulangan hambatan;
- jumlah dosis yang dilaporkan terlewat;
- status pengiriman pesan;
- catatan tindak lanjut petugas;
- aturan keselamatan yang disetujui fasilitas.

### Logika konseptual awal

| Prioritas | Contoh kondisi | Respons sistem |
|---|---|---|
| Hijau | Respons stabil, tidak melaporkan hambatan | Lanjutkan check-in rutin |
| Kuning | Satu check-in terlewat, hambatan berulang, atau dosis dilaporkan terlewat | Masuk antrean tinjauan |
| Merah | Ingin berhenti, obat habis, tidak merespons berulang, atau sinyal keselamatan | Notifikasi prioritas dan tugas petugas |

Aturan numerik final harus disusun bersama petugas TB dan ditinjau tenaga klinis. Label merah bukan diagnosis dan tidak boleh otomatis mengubah terapi.

### Explainability

Setiap label wajib menampilkan alasan, misalnya:

> Prioritas merah karena pasien memilih “ingin berhenti” hari ini dan belum memiliki tindak lanjut aktif.

Sistem dilarang menampilkan label tanpa alasan.

---

## 10. Integrasi WhatsApp

### Pilihan produksi

Gunakan **WhatsApp Business Platform/Cloud API** resmi. Integrasi membutuhkan akun bisnis Meta, nomor pengirim, token akses yang disimpan di server, template pesan yang disetujui, serta endpoint webhook untuk menerima status dan balasan.

### Arus teknis

1. Scheduler membuat pekerjaan check-in.
2. Backend memilih template yang sesuai.
3. Server mengirim permintaan ke WhatsApp Cloud API.
4. WhatsApp mengirim status pengiriman ke webhook.
5. Balasan pasien diterima webhook.
6. Backend memverifikasi signature dan melakukan idempotency check.
7. Respons dinormalisasi lalu disimpan.
8. Mesin aturan memperbarui prioritas.
9. Jika ambang eskalasi terpenuhi, tugas petugas dibuat.
10. Dashboard diperbarui secara real-time atau near-real-time.

### Ketentuan desain integrasi

- Pesan proaktif di luar jendela percakapan mengikuti template yang disetujui platform.
- Token dan secret tidak boleh berada di frontend.
- Webhook harus memverifikasi permintaan dan mencegah pemrosesan ganda.
- Kegagalan pengiriman tidak boleh dianggap sebagai ketidakpatuhan pasien.
- Perubahan aturan atau biaya WhatsApp harus dibaca dari dokumentasi resmi saat implementasi.
- Sistem wajib memiliki fallback berupa panggilan/SMS/prosedur manual fasilitas.

### Mode Demo

Mode Demo mensimulasikan pesan masuk tanpa menggunakan nomor pasien nyata. Tersedia tiga skenario:

1. pasien stabil;
2. pasien mulai lupa dan kehabisan obat;
3. pasien ingin berhenti dan membutuhkan tindak lanjut.

Mode Demo diberi label permanen **Data simulasi** dan tidak boleh bercampur dengan data produksi.

---

## 11. Arsitektur Sistem

### Rekomendasi stack

- **Frontend:** Next.js, TypeScript, Tailwind CSS.
- **Backend/API:** Next.js server routes atau service backend terpisah.
- **Database:** PostgreSQL/Supabase.
- **Autentikasi:** Supabase Auth dengan role-based access.
- **WhatsApp:** Meta WhatsApp Cloud API.
- **Scheduler:** Vercel Cron atau job queue yang mendukung retry.
- **Deployment:** Vercel untuk web; layanan server sesuai kebutuhan webhook.
- **Monitoring:** log terstruktur, error tracking, dan audit trail.

### Komponen

```text
Pasien WhatsApp
      ↕
WhatsApp Cloud API
      ↕ webhook
Integration Service
      ↓
Message Processor → Rules Engine → Follow-up Queue
      ↓                    ↓
PostgreSQL/Supabase   Notification Service
      ↕
Web App Petugas
```

---

## 12. Model Data Minimum

### facilities

- id
- name
- timezone
- operating_hours
- emergency_message
- created_at

### staff_profiles

- id
- facility_id
- full_name
- role
- status
- last_login_at

### patients

- id
- facility_id
- patient_code
- display_name_or_initial
- encrypted_phone
- responsible_staff_id
- support_status
- consent_status
- consent_at
- message_preference
- active
- created_at

### care_schedules

- id
- patient_id
- start_date
- expected_end_date
- checkin_time
- timezone
- status

### message_events

- id
- patient_id
- provider_message_id
- direction
- template_key
- status
- payload_reference
- sent_at
- received_at

### checkins

- id
- patient_id
- scheduled_for
- response_status
- adherence_signal
- barrier_code
- free_text_redacted
- responded_at

### risk_assessments

- id
- patient_id
- level
- reason_codes
- rule_version
- calculated_at
- reviewed_by
- reviewed_at

### followups

- id
- patient_id
- trigger_assessment_id
- assigned_to
- due_at
- status
- contact_method
- outcome_code
- clinical_escalation
- notes
- completed_at

### audit_logs

- id
- actor_id
- action
- entity_type
- entity_id
- metadata
- created_at

---

## 13. Hak Akses

| Aksi | Petugas TB | Dokter/Perawat | Admin fasilitas |
|---|:---:|:---:|:---:|
| Melihat pasien fasilitas | Ya | Ya | Terbatas |
| Mendaftarkan pasien | Ya | Ya | Opsional |
| Meninjau prioritas | Ya | Ya | Tidak |
| Mencatat tindak lanjut | Ya | Ya | Tidak |
| Membuat keputusan klinis | Tidak | Ya | Tidak |
| Mengelola anggota | Tidak | Tidak | Ya |
| Mengubah aturan | Usul | Persetujuan | Publikasi |
| Melihat audit log | Terbatas | Terbatas | Ya |

Semua query produksi harus dibatasi berdasarkan `facility_id` dan role. Akses lintas fasilitas ditolak.

---

## 14. Desain Visual

### Arah visual

Produk harus terasa seperti alat kerja layanan primer Indonesia: hangat, tenang, jelas, dan dapat dipercaya. Hindari tampilan futuristik, robot, otak bercahaya, glassmorphism, serta gradien biru-ungu yang identik dengan produk AI.

### Palet

- Latar utama: `#F7F7F2` — putih hangat.
- Permukaan: `#FFFFFF`.
- Teks utama: `#1E2A26` — arang kehijauan.
- Hijau utama: `#246B55`.
- Hijau muda: `#DDECE5`.
- Kuning prioritas: `#B7791F` dengan latar `#FFF4D6`.
- Merah prioritas: `#A43A3A` dengan latar `#FBE6E4`.
- Garis: `#D8DED9`.

Warna tidak boleh menjadi satu-satunya penanda prioritas; selalu sertakan label dan ikon.

### Tipografi

- UI: Inter, Source Sans 3, atau Plus Jakarta Sans.
- Ukuran isi minimum desktop 14–16 px.
- Heading tegas tetapi tidak terlalu besar.
- Hindari judul pemasaran seperti “Revolutionizing TB Care”.

### Gaya komponen

- radius 8–12 px;
- bayangan sangat ringan;
- tabel dan daftar menjadi struktur utama;
- kartu hanya untuk informasi yang memang perlu dikelompokkan;
- touch target minimum sekitar 44 px;
- status fokus keyboard terlihat;
- animasi terbatas pada perubahan status dan loading.

---

## 15. Kondisi Antarmuka

Setiap halaman harus mempunyai:

- loading state;
- empty state dengan arahan tindakan;
- error state yang menjelaskan langkah berikutnya;
- success feedback;
- offline/connection warning;
- permission denied state;
- data simulation badge untuk Mode Demo.

Contoh empty state:

> Belum ada pasien yang perlu ditinjau. Check-in berikutnya dijadwalkan pukul 18.00.

Contoh kegagalan pesan:

> Pesan belum terkirim. Sistem tidak mengubah prioritas pasien dan akan mencoba kembali sesuai kebijakan pengiriman.

---

## 16. Privasi, Etika, dan Keselamatan

1. Persetujuan eksplisit sebelum aktivasi pesan.
2. Data minimum; diagnosis lengkap tidak dibutuhkan untuk tampilan harian.
3. Nomor telepon dienkripsi saat tersimpan.
4. Seluruh trafik memakai HTTPS.
5. Secret hanya tersedia pada lingkungan server.
6. Hak akses berdasarkan fasilitas dan peran.
7. Audit untuk melihat, mengubah, mengekspor, dan menghapus data.
8. Pesan menggunakan bahasa netral agar tidak membuka diagnosis pada layar terkunci.
9. Catatan bebas dibatasi dan data sensitif diringkas bila memungkinkan.
10. Retensi data ditentukan fasilitas dan diinformasikan kepada pasien.
11. Pasien dapat berhenti dari pesan otomatis tanpa kehilangan hak atas pelayanan.
12. Insiden privasi dan salah eskalasi memiliki prosedur pelaporan.
13. Tidak ada saran diagnosis, perubahan obat, atau tindakan darurat otomatis.

---

## 17. Notifikasi Petugas

Petugas tidak boleh menerima notifikasi untuk setiap check-in. Notifikasi dikirim jika:

- muncul prioritas merah baru;
- tindak lanjut melewati tenggat;
- pesan gagal berulang kali;
- pasien meminta petugas;
- ada perubahan aturan yang membutuhkan persetujuan.

Notifikasi berisi kode pasien dan alasan ringkas, tanpa diagnosis lengkap.

---

## 18. Analitik dan KPI Pilot

### KPI produk

- persentase check-in yang memperoleh respons;
- persentase pesan berhasil dikirim;
- jumlah dan jenis hambatan teridentifikasi;
- median waktu sinyal merah hingga ditinjau;
- median waktu tinjauan hingga tindak lanjut;
- persentase tugas selesai sebelum tenggat;
- tingkat alarm salah setelah verifikasi petugas;
- skor kegunaan pasien dan petugas;
- waktu rata-rata petugas menggunakan dashboard per hari;
- jumlah insiden privasi.

### Outcome eksploratif

- retensi pasien dalam pendampingan;
- perubahan frekuensi dosis yang dilaporkan terlewat;
- penyelesaian terapi pada evaluasi lebih panjang.

Outcome klinis tidak ditampilkan sebagai keberhasilan produk sebelum studi yang memadai.

---

## 19. Event Tracking

- `patient_enrolled`
- `consent_recorded`
- `checkin_scheduled`
- `message_sent`
- `message_failed`
- `checkin_received`
- `barrier_selected`
- `risk_level_changed`
- `followup_created`
- `followup_opened`
- `followup_completed`
- `clinical_escalation_recorded`
- `patient_opted_out`
- `report_exported`

Event analitik tidak menyimpan isi pesan medis secara langsung.

---

## 20. Acceptance Criteria MVP

### Integrasi

- Sistem dapat mengirim template uji ke nomor yang diizinkan.
- Webhook menerima balasan dan status pesan.
- Event duplikat tidak membuat check-in ganda.
- Kegagalan provider menghasilkan retry dan log yang jelas.

### Mesin aturan

- Setiap prioritas memiliki alasan yang terlihat.
- Aturan memiliki versi.
- Perubahan aturan tidak mengubah riwayat penilaian lama.
- Kegagalan pesan tidak menaikkan risiko pasien.

### Dashboard

- Petugas dapat menyelesaikan alur tinjau hingga mencatat hasil.
- Filter dan pencarian berfungsi pada mobile dan desktop.
- Tidak ada data lintas fasilitas.
- Mode Demo selalu berlabel data simulasi.

### Privasi

- Tidak ada token di browser bundle.
- Nomor telepon tidak muncul pada daftar umum.
- Semua akses dan perubahan penting tercatat.
- Pesan awal tidak menyebut diagnosis TB.

### Aksesibilitas

- Navigasi utama dapat digunakan dengan keyboard.
- Kontras teks memadai.
- Prioritas tidak hanya dibedakan melalui warna.
- Tombol utama memiliki label yang jelas.

---

## 21. Skenario Demo Kompetisi

Durasi ideal: 3–4 menit.

1. Buka halaman **Hari Ini**; tampilkan dua pasien simulasi yang membutuhkan tinjauan.
2. Perlihatkan skenario WhatsApp pasien memilih “obat hampir habis”.
3. Jalankan balasan simulasi melalui webhook demo.
4. Dashboard menampilkan prioritas merah beserta alasannya.
5. Petugas membuka detail dan memilih **Hubungi melalui WhatsApp**.
6. Petugas mencatat hasil: koordinasi pengambilan obat.
7. Status berubah dari “Perlu tindakan” menjadi “Sedang ditangani”.
8. Tutup dengan laporan waktu respons dan distribusi hambatan, diberi label simulasi.

Pesan utama demo: teknologi tidak mengambil keputusan klinis; teknologi memastikan sinyal pasien tidak tenggelam.

---

## 22. Roadmap

### Fase 0 — Prototipe kompetisi

- antarmuka dashboard;
- tiga skenario pasien simulasi;
- simulator WhatsApp;
- mesin aturan dasar;
- catatan tindak lanjut;
- laporan simulasi.

### Fase 1 — Integrasi sandbox

- WhatsApp Cloud API test number;
- webhook nyata;
- template uji;
- autentikasi dan database;
- audit log.

### Fase 2 — Co-design dan uji kegunaan

- validasi bahasa bersama pasien dan petugas;
- review aturan oleh tenaga klinis;
- uji aksesibilitas;
- perbaikan beban kerja.

### Fase 3 — Pilot terbatas

- satu fasilitas;
- pengguna dengan persetujuan;
- monitoring keselamatan;
- evaluasi proses dan pengalaman.

### Fase 4 — Validasi

- revisi aturan;
- evaluasi outcome jangka lebih panjang;
- kajian integrasi sistem kesehatan;
- perluasan hanya setelah hasil mendukung.

---

## 23. Risiko Produk

| Risiko | Dampak | Mitigasi |
|---|---|---|
| Jawaban pasien tidak mencerminkan konsumsi obat | Salah interpretasi kepatuhan | Sebut sebagai sinyal; verifikasi petugas |
| Alarm terlalu banyak | Petugas mengabaikan dashboard | Tuning aturan dan pengukuran alarm salah |
| Pasien berbagi telepon | Risiko terbukanya informasi | Pesan netral dan pilihan waktu |
| WhatsApp tidak tersedia | Check-in terputus | Fallback manual/SMS/telepon |
| Token atau webhook bocor | Akses tidak sah | Secret server-side, signature verification, rotasi token |
| Free text disalahartikan | Salah eskalasi | Batasi pilihan terstruktur; review manusia |
| Sistem dianggap alat diagnosis | Risiko klinis dan etik | Disclaimer, non-goals, serta SOP eskalasi |
| Petugas tidak menindaklanjuti alert | Manfaat sistem hilang | SLA internal, penanggung jawab, notifikasi jatuh tempo |

---

## 24. Keputusan Produk yang Dikunci

1. TUNTAS-TB bukan bagian atau turunan AURA Health.
2. Subtema produk adalah teknologi dengan dampak kesehatan.
3. Pasien menggunakan WhatsApp; web app diprioritaskan untuk petugas.
4. MVP menggunakan mesin aturan transparan, bukan AI generatif.
5. Sistem tidak mendiagnosis atau mengganti keputusan klinis.
6. Data respons merupakan sinyal, bukan bukti pasien menelan obat.
7. Mode Demo dan data produksi dipisahkan secara tegas.
8. Desain visual tenang dan operasional, tanpa estetika AI generik.
9. Integrasi WhatsApp produksi menggunakan kanal resmi.
10. Pilot didahului co-design dan review tenaga kesehatan.

---

## 25. Definition of Done

Prototipe dianggap siap ketika:

- seluruh golden path dapat didemonstrasikan tanpa bug;
- pasien simulasi dapat membalas alur WhatsApp;
- respons masuk memperbarui dashboard dan prioritas;
- setiap prioritas memiliki alasan yang dapat dijelaskan;
- petugas dapat mencatat tindak lanjut hingga selesai;
- tampilan mobile dan desktop dapat digunakan;
- data simulasi ditandai secara konsisten;
- halaman privasi dan batas fungsi tersedia;
- tidak ada klaim hasil klinis palsu;
- koneksi sandbox WhatsApp dapat diaktifkan tanpa mengubah arsitektur utama.

---

## 26. Referensi Implementasi

- World Health Organization. *WHO operational handbook on tuberculosis: Module 4 - treatment and care*.
- World Health Organization. *Handbook for the use of digital technologies to support tuberculosis medication adherence*.
- Stop TB Partnership. *Digital Adherence Technologies*.
- Meta for Developers. *WhatsApp Cloud API documentation*.

Dokumentasi teknis WhatsApp, biaya, kebijakan template, dan jendela percakapan harus diverifikasi kembali saat implementasi karena dapat berubah.

