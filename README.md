# Script Wawancara via Zoom — Investigasi Insiden Keamanan Siber
## PT. Defender Nusa Semesta (Defenxor) — Final Project MIKS

> Versi daring dari script wawancara. Substansi pertanyaan tetap sama dengan versi tatap muka, namun logistik, etika, dan cara pengambilan bukti disesuaikan untuk sesi via Zoom.

---

## A. Persiapan Sebelum Hari-H (Versi Zoom)

**Logistik & Teknis**
- Kirim **link Zoom** ke narasumber minimal H-1, sertakan agenda singkat & estimasi durasi di email/WA.
- Cantumkan di email: tujuan wawancara, nama-nama anggota tim yang akan hadir beserta perannya, dan permintaan izin merekam sesi melalui fitur Record Zoom.
- H-1/H-0 pagi: **tes koneksi internet, mic, speaker, dan kamera** seluruh anggota tim. Pastikan tidak ada anggota yang join dari lokasi dengan koneksi tidak stabil.
- Siapkan **akun Zoom dengan kapasitas rekam** (cloud/local recording) — host sebaiknya dipegang salah satu anggota tim yang stabil koneksinya.
- Siapkan dokumen kuesioner dalam bentuk **digital (PDF/Google Doc)** agar mudah dibuka berdampingan dengan Zoom, atau di-screen share bila perlu menunjukkan poin tertentu.
- Siapkan **virtual background atau ruang netral & rapi** di belakang masing-masing anggota tim (hindari ruang berantakan, cahaya backlight, atau suara bising).
- Uji coba join Zoom 10–15 menit lebih awal dari jadwal untuk memastikan semua teknis berjalan baik sebelum narasumber bergabung.

**Pembagian Peran Tim (tetap 4 peran, disesuaikan ke konteks Zoom)**
1. **Moderator/Lead Interviewer** — memimpin alur tanya-jawab, kamera selalu on, fokus menjaga kontak mata ke kamera.
2. **Co-Interviewer** — mengajukan pertanyaan probing/follow-up, siap unmute saat gilirannya.
3. **Notetaker** — mencatat poin kunci di chat/dokumen terpisah, memantau fitur live transcript Zoom jika diaktifkan sebagai cadangan.
4. **Host/Dokumentator** — bertanggung jawab start/stop recording, mengelola fitur share screen, mengambil screenshot sesi sebagai bukti tambahan, serta mengirim file/dokumen pendukung lewat chat Zoom di akhir sesi.

---

## B. Overview Wawancara (Zoom)

| Segmen | Topik | Estimasi Waktu |
|---|---|---|
| 1 | Join & tes koneksi (sebelum narasumber masuk) | 10–15 menit (internal tim) |
| 2 | Pembukaan & perkenalan | 5 menit |
| 3 | Konfirmasi profil narasumber & konteks insiden | 5 menit |
| 4 | Bagian B — Analisis Teknis | 20–25 menit |
| 5 | Bagian C — Analisis Dampak | 10–15 menit |
| 6 | Bagian D — Respons & Pemulihan | 15 menit |
| 7 | Permintaan dokumen pendukung (via chat/email) | 5–10 menit |
| 8 | Penutup & follow-up | 5 menit |

**Total sesi bersama narasumber: 65–85 menit.** Sampaikan di awal bahwa sesi akan direkam via Zoom (dengan izin) sebagai dokumentasi resmi untuk laporan akademik.

---

## C. Script Pembukaan (Introduction) — Versi Zoom

> *Dibacakan Moderator setelah narasumber join dan basa-basi singkat (cek suara/gambar: "Apakah suara dan gambar kami sudah jelas terlihat, Pak/Bu?").*

"Selamat pagi/siang, Bapak Madani. Terima kasih banyak sudah meluangkan waktu untuk bergabung di sesi Zoom hari ini.

Perkenalkan, kami mahasiswa dari Institut Teknologi Sepuluh Nopember program studi Teknologi Informasi, sedang menempuh mata kuliah Manajemen Insiden Keamanan Siber. Saya Ahmad Idza Anafin, akan menjadi pewawancara utama. Bersama saya hadir Rafi` Adly yang akan membantu menggali detail teknis, Dina Ramadhani yang mencatat poin-poin penting, dan Ni'mah Fauziyyah yang bertugas mengelola rekaman serta dokumentasi sesi ini.

Sebelum mulai, kami izin untuk mengaktifkan **fitur record Zoom** untuk keperluan penyusunan laporan akademik kami — apakah Bapak berkenan? Rekaman ini hanya akan digunakan untuk kebutuhan tugas kuliah dan tidak akan disebarluaskan tanpa izin Bapak.

*(Setelah dapat persetujuan, Dokumentator menekan tombol Record dan menyebutkan secara verbal: "Baik, rekaman sudah kami mulai ya, Pak/Bu.")*

Tujuan kami hari ini adalah menyusun *Laporan Investigasi Insiden* berdasarkan salah satu insiden keamanan siber nyata yang pernah ditangani atau diketahui oleh Defenxor. Secara garis besar kami ingin memahami lima hal: **kronologi insiden, akar penyebab, dampak yang ditimbulkan, langkah respons dan pemulihan, serta rekomendasi pencegahan ke depan.**

Sebelum mulai ke pertanyaan inti, boleh kami konfirmasi nama lengkap, jabatan, dan kurang lebih sudah berapa lama Bapak menangani kasus terkait insiden ini? Ini untuk kebutuhan dokumentasi formal di laporan kami."

*(Notetaker mencatat: nama, jabatan, tanggal, jam mulai wawancara, dan platform "Zoom Meeting" — data ini wajib untuk Lampiran A "Detail Wawancara".)*

---

## D. Pertanyaan Wawancara

### Segmen 1 — Bagian B: Analisis Teknis

**1. Sistem & Data yang Terdampak**
- "Untuk insiden yang akan kita bahas, aset apa saja yang berhasil dikompromi pihak penyerang? Apakah terbatas pada server/workstation tertentu, atau sempat meluas ke subnet jaringan lain?"
- *Follow-up:* "Kira-kira berapa jumlah sistem/endpoint yang terdampak secara langsung?"
- "Jenis data apa yang terdampak — apakah lebih ke kredensial internal, data finansial, atau ada juga PII pelanggan/klien yang ikut terekspos?"

**2. Sumber Informasi & Penemuan**
- "Bagaimana awal mula insiden ini terdeteksi? Melalui alert otomatis (SIEM/EDR), laporan pengguna, atau informasi dari pihak eksternal/klien?"
- "Saat indikasi pertama muncul, bukti digital atau log apa yang pertama kali dianalisis tim untuk memvalidasi situasi?"

**3. Indikator Kompromi (IoC)**
- "Selama investigasi, apakah ditemukan IoC spesifik — misalnya hash malware, IP penyerang, domain mencurigakan, atau akun yang disalahgunakan?"
- *Jika dijawab confidential:* "Mohon maaf Pak/Bu, kalau detail tersebut bersifat rahasia, apakah kami diperkenankan mendapatkan versi anonim atau gambaran umum tipe artefaknya saja untuk kebutuhan laporan?"

**4. Analisis Akar Penyebab**
- "Apa vektor akses awal (initial access) yang dimanfaatkan penyerang — phishing, eksploitasi CVE tertentu, atau kebocoran kredensial?"
- "Celah keamanan atau kelemahan konfigurasi apa yang membuat vektor tersebut berhasil dieksploitasi?"

**5. Jenis Serangan & Kronologi Teknis**
- "Jika dikategorikan, jenis serangan ini condong ke arah apa — ransomware, APT, SQL injection, defacement, atau lainnya?"
- "Bisa diceritakan kronologi siklus hidup serangannya — mulai dari jam-jam awal akses, pergerakan lateral (lateral movement), sampai akhirnya terdeteksi dan dimitigasi?"
- *Follow-up:* "Berapa lama rentang waktu dari akses awal sampai akhirnya terdeteksi (dwell time)?"
-  *Opsionaljika narasumber punya diagram:* "Apakah Bapak/Ibu berkenan share screen untuk menunjukkan ilustrasi/diagram kronologinya, atau cukup dijelaskan secara verbal saja?"

### Segmen 2 — Bagian C: Analisis Dampak

**1. Dampak Operasional**
- "Berapa lama sistem mengalami downtime atau gangguan total akibat insiden ini?"
- "Bagaimana alur kerja harian tim dan layanan ke klien terdampak selama periode tersebut?"

**2. Dampak Finansial**
- "Apakah ada kerugian finansial langsung — misalnya biaya pemulihan vendor, uang tebusan (jika relevan), atau denda regulasi?"
- "Bagaimana estimasi kerugian tidak langsung, seperti penurunan produktivitas atau potensi pendapatan yang hilang selama sistem belum normal?"

**3. Dampak Reputasi & Hukum**
- "Bagaimana dampak insiden terhadap tingkat kepercayaan pelanggan atau mitra bisnis?"
- "Apakah ada tuntutan hukum atau tantangan kepatuhan (compliance) yang dihadapi pasca-insiden, dan bagaimana strategi komunikasi PR saat krisis tersebut?"

### Segmen 3 — Bagian D: Respons & Pemulihan

**1. Tindakan Respons Awal (Containment)**
- "Begitu indikasi serangan terkonfirmasi, langkah mitigasi darurat apa yang pertama diambil tim untuk mengisolasi serangan agar tidak menyebar?"

**2. Langkah Pemberantasan (Eradication)**
- "Setelah berhasil dilokalisasi, bagaimana proses eliminasi akar penyebabnya — patching massal, revoke akun, atau pembersihan malware menyeluruh?"

**3. Langkah Pemulihan (Recovery)**
- "Bagaimana proses pemulihan sistem sampai kembali normal? Apakah mengandalkan backup, dan berapa lama proses restore-nya?"

**4. Tindakan Pasca-Insiden**
- "Evaluasi internal atau perbaikan apa yang langsung diterapkan perusahaan/klien setelah insiden ini untuk memperkuat pertahanan ke depan?"
- *Pertanyaan penutup segmen ini:* "Dari sudut pandang Bapak/Ibu sebagai praktisi, apa pelajaran terbesar (lesson learned) dari kasus ini yang menurut Bapak/Ibu paling penting untuk dihindari organisasi lain?"

---

## E. Dokumen & Bukti yang Wajib Diminta (Versi Zoom)

**1. Bukti Legitimasi Perusahaan**
- Link/screenshot website resmi (defenxor.com) dan profil LinkedIn perusahaan/narasumber.
- Screenshot tampilan Zoom call yang menampilkan nama narasumber dan tim (sebagai pengganti foto bersama tatap muka).

**2. Bukti Pelaksanaan Wawancara (untuk Lampiran A)**
- **File rekaman Zoom** (cloud/local recording) — pastikan diunduh & dibackup setelah sesi selesai, jangan hanya mengandalkan cloud yang bisa expired.
- Catatan ringkasan tertulis dari notetaker.
- Screenshot sesi Zoom (menunjukkan tanggal/waktu pada perangkat, peserta yang hadir).
- Bukti komunikasi penjadwalan (screenshot email/WA undangan Zoom & konfirmasi jadwal).

**3. Materi Pendukung Teknis**
- Laporan insiden yang telah dianonimkan.
- Diagram jaringan yang telah disanitasi.
- Dokumen post-mortem/ringkasan investigasi yang boleh dipublikasikan secara akademik.
- Contoh IoC yang sudah dianonimkan, jika versi aslinya tidak bisa dibagikan.

> Script permintaan: *"Terakhir, untuk melengkapi laporan kami, apakah kami diperkenankan mendapatkan dokumen pendukung seperti laporan yang sudah dianonimkan, diagram jaringan yang sudah disanitasi, atau ringkasan post-mortem? Bisa dikirimkan melalui chat Zoom ini atau email kami setelah sesi selesai. Tentu kami pahami bila ada bagian yang tidak bisa dibagikan karena alasan kerahasiaan klien."*

---

## F. Do's and Don'ts — Khusus Wawancara Online

**Do's**
- Join 10–15 menit lebih awal untuk memastikan koneksi, mic, dan kamera berfungsi normal.
- Gunakan nama tampilan (display name) yang jelas dan profesional di Zoom, beserta foto profil yang sopan jika kamera dimatikan sewaktu-waktu.
- Nyalakan kamera sepanjang sesi (kecuali ada gangguan teknis) untuk menjaga kesan profesional dan membangun rapport.
- **Mute mic saat tidak berbicara**, terutama anggota yang berada di tempat dengan latar suara bising.
- Beri sedikit jeda sebelum menjawab/bertanya untuk mengantisipasi delay/lag video call.
- Minta izin secara eksplisit sebelum menyalakan fitur Record, dan informasikan saat recording dimulai/berhenti.
- Gunakan fitur **chat Zoom** untuk mengirim daftar pertanyaan cadangan, link dokumen, atau menerima file dari narasumber tanpa memotong pembicaraan.
- Tetap berpakaian rapi dan profesional walau dari rumah/kos.
- Pastikan background rapi/netral atau gunakan virtual background yang sopan.
- Validasi kembali fakta-fakta kunci sebelum sesi ditutup.
- Segera **download & backup rekaman** begitu sesi selesai (jangan menunda, terutama jika memakai cloud recording dengan masa retensi terbatas).

**Don'ts**
- Jangan memulai recording sebelum mendapat izin verbal dari narasumber.
- Jangan membiarkan koneksi tim sendiri tidak stabil — uji dulu sebelum sesi dimulai.
- Jangan berbicara bersamaan/memotong saat narasumber masih menjelaskan, terutama karena delay audio bisa membuat percakapan bertumpuk.
- Jangan memaksa narasumber membuka data yang sudah dinyatakan rahasia.
- Jangan multitasking terlihat di kamera (membuka aplikasi lain, terganggu HP) saat narasumber sedang berbicara.
- Jangan menyebarluaskan link rekaman/recording di luar keperluan tugas akademik.
- Jangan mengarang atau menambah-nambahi data yang tidak disampaikan narasumber.
- Jangan share screen dokumen internal tim yang belum tertata rapi (tutup tab/file yang tidak relevan sebelum share screen).

---

## G. Script Penutup (Closing) — Versi Zoom

"*opsional* Sejauh ini, izinkan kami merangkum kembali secara singkat: [Moderator merekap 2–3 poin kunci dari jawaban narasumber]. Apakah ada yang ingin Bapak/Ibu tambahkan atau koreksi dari apa yang sudah kami sampaikan?

*wajib* Kami sangat menghargai waktu dan keterbukaan Bapak hari ini. Seluruh informasi ini akan sangat membantu kami dalam menyusun Laporan Investigasi Insiden untuk tugas akhir mata kuliah kami. Jika nanti ada dokumen pendukung yang masih perlu disusulkan, bolehkah kami menghubungi melalui email/WhatsApp yang sama sebelum meeting ini berakhir?

Sekali lagi terima kasih banyak atas waktu dan kesempatannya, Bapak Madani. Kami akan menghentikan rekaman sekarang. Semoga harinya lancar."

*(Dokumentator menghentikan recording, mencatat jam selesai wawancara, dan langsung mengunduh file rekaman sebelum meninggalkan Zoom.)*

---

## H. Checklist Pasca-Wawancara (Persiapan Lampiran A) — Versi Zoom

- [ ] Detail wawancara tercatat: tanggal, jam mulai-selesai, durasi, nama & jabatan narasumber, platform "Zoom Meeting".
- [ ] **File rekaman Zoom sudah diunduh** dari cloud/local dan dibackup ke 2 tempat (drive tim + penyimpanan pribadi).
- [ ] Transkrip wawancara (verbatim atau ringkasan terstruktur) sudah disusun, bisa dibantu dari fitur transcript otomatis Zoom (perlu diperiksa ulang akurasinya).
- [ ] Screenshot sesi Zoom (menunjukkan peserta & waktu) sudah dikumpulkan sebagai pengganti foto dokumentasi.
- [ ] Dokumen pendukung yang dikirim via chat Zoom/email sudah disimpan & dicatat sumbernya.
- [ ] Bukti legitimasi perusahaan (link website, profil resmi) sudah disertakan.
- [ ] Email/chat ucapan terima kasih & follow-up sudah dikirim — bisa dijadikan bukti tambahan pelaksanaan wawancara.

---

Struktur dan substansi pertanyaan tetap konsisten dengan versi tatap muka, sehingga hasil wawancara ini bisa langsung dipetakan ke bagian Analisis Teknis, Analisis Dampak, Analisis Respons & Pemulihan, serta Lampiran A pada laporan akhir.
