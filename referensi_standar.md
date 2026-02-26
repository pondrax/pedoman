# Referensi Pemetaan Pemenuhan Standar Keamanan (KED, KEI, KEF)
## Pedoman Sistem Manajemen Keamanan Informasi Pemerintah Kota Mojokerto

Tabel ini menyediakan pemetaan rinci antara Instrumen Pemeriksaan Keamanan SPBE (72 Kontrol) dengan instruksi teknis yang terdapat dalam Pedoman SMKI.

| NO | Fungsi Keamanan | Standar Teknis (Audit) | Pemenuhan Desain (**KED**) | Pemenuhan Implementasi (**KEI**) | Pemenuhan Efektivitas (**KEF**) |
| :-- | :--- | :--- | :--- | :--- | :--- |
| **1** | **Autentikasi** | **1. Manajemen Kata Sandi** | **Bab 5.7.2**: Ketentuan panjang, kompleksitas, & usia sandi. | **Bab 4.4.4**: Bukti rekaman konfigurasi proses autentikasi. | **Bab 6.1.1**: Indikator % penggunaan password kuat ≥90%. |
| | | **2. Verifikasi Sisi Server** | **Bab 5.6.1 (2)**: Verifikasi wajib dilakukan di sisi server. | **Bab 5.6.1 (3)**: Hasil uji *Manual Code Review* autentikasi. | **Bab 5.10.4**: Laporan insiden nihil bypass autentikasi. |
| | | **3. Kompleksitas & Masa Berlaku** | **Bab 5.7.2 (Tabel)**: Rincian teknis parameter sandi. | **Bab 5.7.2**: Dokumen standar kebijakan autentikasi PD. | **Bab 5.2.4**: Laporan kepatuhan sandi berkala. |
| | | **4. Batas Kesalahan Login** | **Bab 5.7.2 (Tabel)**: Pengaturan *Lockout* (5-20 percobaan). | **Bab 5.9.2.2**: Log sistem yang mencatat kejadian lockout. | **Bab 5.9.2.2**: Alerting otomatis saat brute-force terdeteksi. |
| | | **5. Pemulihan Kata Sandi** | **Bab 5.6.1 (2)**: Penggunaan OTP/Email/Telepon & Logging. | **Bab 4.4.4**: Screenshot alur reset/recovery password. | **Bab 5.10.4**: Nihil kompromi akun via reset password. |
| | | **6. Rahasia Simpan (Hash)** | **Bab 5.8.1 (1)**: Kredensial wajib dienkripsi/hash aman. | **Bab 5.6.1 (3)**: Audit algoritma hash (BCrypt/Argon2). | **Bab 5.8.5**: Tidak ada plaintext password di DB. |
| | | **7. Jalur Komunikasi Port 443** | **Bab 5.6.1**: Penegakan HTTPS/TLS 1.2+ global. | **Bab 5.8.1 (3)**: Verifikasi sertifikat SSL/TLS aktif. | **Bab 5.11**: Status pengujian sniffing (Traffic terenkripsi). |
| **2** | **Manajemen Sesi** | **8. Pengendali Sesi** | **Bab 5.6.1 (2)**: Penggunaan session handler framework. | **Bab 4.4.4**: Bukti konfigurasi session management. | **Bab 5.6.1**: Nihil kerentanan *Session Fixation*. |
| | | **9. Framework Handler** | **Bab 5.6.1 (2)**: Menggunakan handler standar framework. | **Bab 5.6.1 (3)**: Review kode dependensi session. | **Bab 5.10.4**: Keandalan sesi saat traffic tinggi. |
| | | **10. Token Sesi Acak** | **Bab 5.6.1 (2)**: Token wajib memenuhi algoritma acak CSPRNG. | **Bab 4.4.4**: Sampel token sesi terenkripsi/acak. | **Bab 5.6.1**: Hasil uji *Token Predictability* (Nihil). |
| | | **11. Timeout Otomatis** | **Bab 5.7.2 (Tabel)**: Timeout 5-15 menit sesuai kategori. | **Bab 5.9.2.2**: Log sesi berakhir saat masa idle terpenuhi. | **Bab 6.1.1**: KPI keamanan sesi dan ketersediaan. |
| | | **12. Validasi Session ID** | **Bab 5.6.1 (2)**: Validasi ID sesi di setiap request server. | **Bab 5.6.1 (3)**: Review kode validasi interseptor sesi. | **Bab 5.10.4**: Nihil serangan *Session Hijacking*. |
| | | **13. Atribut Cookie (Flag)** | **Bab 5.6.1 (2)**: Wajib flag *Secure, HttpOnly, SameSite*. | **Bab 4.4.4**: Bukti Header Set-Cookie pada browser. | **Bab 5.6.1**: Rating A pada securityheaders.com. |
| | | **14. Deteksi Duplikasi Sesi** | **Bab 5.6.1 (2)**: Deteksi login ganda dari lokasi berbeda. | **Bab 5.9.2.2**: Laporan notifikasi ke user via email/app. | **Bab 5.10.4**: Penurunan angka pembajakan akun aktif. |
| **3** | **Kontrol Akses** | **15. Otorisasi (RBAC)** | **Bab 5.7.1**: Aturan hak akses & Bab 5.6.1 (RBAC/ABAC). | **Bab 4.4.4**: Matriks Role-Based Access Control aplikasi. | **Bab 6.2.1**: Hasil audit akses periodik (6 bulan). |
| | | **16. Serangan Otomatis** | **Bab 5.6.1 (2)**: Anti-bot, Captcha, dan Rate Limiting. | **Bab 5.5.5**: Konfigurasi WAF dan Rate Limiter aktif. | **Bab 5.6.3**: Pengurangan traffic malicious otomatis. |
| | | **17. Panel Admin Khusus** | **Bab 5.6.1 (2)**: Akses & tampilan admin wajib tersedia. | **Bab 4.4.1**: Daftar admin pengelola sistem informasi. | **Bab 5.7.2**: Akses remote admin wajib via VPN. |
| | | **18. Verifikasi Token API** | **Bab 5.6.3 (4)**: Token harus atomik dan sekali pakai (one-time). | **Bab 5.6.3 (5)**: Log akses API (mTLS/Token). | **Bab 5.6.3 (4)**: Nihil kerentanan *Race Condition* pada token. |
| **4** | **Validasi Input** | **19. Validasi Sisi Server** | **Bab 5.6.1 (2)**: Validasi semua parameter di sisi server. | **Bab 5.6.1 (3)**: Hasil scan SAST tingkat kepatuhan kode. | **Bab 4.2.2**: Laporan Pentest status *"Fail to Inject"*. |
| | | **20. Penolakan Input Cacat** | **Bab 5.6.1 (2)**: Mekanisme filter & penolakan data kotor. | **Bab 5.9.2.1**: Log penolakan request tidak valid (400/422). | **Bab 5.10.4**: Nihil serangan *Buffer Overflow*. |
| | | **21. Pendekatan Whitelist** | **Bab 5.6.1 (2)**: Validasi berdasarkan daftar yang diizinkan. | **Bab 5.6.1 (3)**: Review fungsi sanitasi input di kode. | **Bab 5.2.4**: Minimnya anomali data di Database. |
| | | **22. Filter Data Untrusted** | **Bab 5.6.1 (2)**: Filter terhadap sumber data eksternal. | **Bab 5.6.3**: Laporan integrasi data yang tersanitasi. | **Bab 5.10.4**: Nihil dampak serangan dari data third-party. |
| | | **23. Kode Dinamis (Eval)** | **Bab 5.6.1 (2)**: Larangan fitur dinamis berbahaya (eval/exec). | **Bab 5.6.1 (3)**: Scanning kode sumber terhadap fungsi eval. | **Bab 5.10.4**: Nihil insiden *In-Memory Code Execution*. |
| | | **24. Proteksi XSS** | **Bab 5.6.1 (2)**: Output encoding (HTML/JS) & Content Security Policy. | **Bab 4.4.4**: Bukti header CSP diaktifkan secara ketat. | **Bab 5.6.1**: Verifikasi CSP Rating A. |
| | | **25. Injeksi Basis Data** | **Bab 5.6.1 (2)**: *Parameterized Queries / Prepared Stmt*. | **Bab 5.6.1 (3)**: Audit kode pada layer Database Access. | **Bab 5.10.4**: Nihil kebocoran data via SQL Injection. |
| **5** | **Kriptografi** | **26. Standar Algoritma** | **Bab 5.8.1**: Minimal 256-bit symmetric, 2048-bit asymmetric. | **Bab 5.8.1**: Rekaman algoritma kriptografi yang aktif. | **Bab 5.2.4**: Kepatuhan terhadap Kep. BSSN 443/2024. |
| | | **27. Autentikasi Enkripsi** | **Bab 5.8.2**: Penggunaan Hash untuk verifikasi integritas. | **Bab 4.2.4**: Bukti tanda tangan digital pada dokumen. | **Bab 5.8.6**: Validasi integritas dokumen via BSrE. |
| | | **28. Manajemen Kunci** | **Bab 5.8.1 (4)**: Rotasi 90 hari, Storage di HSM/KMS. | **Bab 4.4.4**: Log rotasi kunci kriptografi otomatis. | **Bab 5.8.1**: Rahasia kunci privat tetap terjaga 100%. |
| | | **29. Generator Angka Acak** | **Bab 5.6.1 (2)**: Generator angka acak kriptografi (CSPRNG). | **Bab 5.6.1 (3)**: Review fungsi random pada aplikasi. | **Bab 5.6.1**: Ketahanan terhadap serangan prediksi nilai. |
| **6** | **Kesalahan & Log** | **30. Konten Pesan Error** | **Bab 5.9.2.1**: Pesan generik tanpa info teknis (Pemerintah Kota). | **Bab 4.4.4**: Screenshot pesan error UI aplikasi. | **Bab 5.10.4**: Nihil kebocoran info versi via error page. |
| | | **31. Pola Penanganan Eror** | **Bab 5.9.2.1**: Try-Catch-Finally & Fuzzing pada fase testing. | **Bab 5.6.1 (3)**: Bukti kode penangkapan exception komprehensif. | **Bab 5.6.1**: Ketahanan sistem terhadap input cacat masif. |
| | | **32. Masking Info Log** | **Bab 5.9.2.2**: Larangan mencatat password/token di log. | **Bab 5.9.2.2 (2)**: Log SIEM yang menunjukkan sensor data. | **Bab 5.8.5**: Kepatuhan Privasi (Privacy by Design). |
| | | **33. Cakupan Log Investigasi** | **Bab 5.9.2.2 (1)**: Subjek, Objek, IP, Waktu, Hasil. | **Bab 5.9.2.2 (2)**: Dashboard SIEM/Log Management. | **Bab 6.1.1**: Keberhasilan audit forensik 100%. |
| | | **34. Pelindungan Log** | **Bab 5.9.2.2 (2)**: Log terpusat & Read-only access bagi admin. | **Bab 5.5.3**: Konfigurasi server log dengan hak akses ketat. | **Bab 5.9.2.2**: Log tidak dapat dimanipulasi oleh intruder. |
| | | **35. Enkripsi Log (Injeksi)** | **Bab 5.9.2.2**: Enkripsi & Sanitasi/Encoding input log pengguna. | **Bab 4.4.4**: Bukti enkripsi pada file arsip log. | **Bab 5.9.2.2**: Nihil kerentanan *Log Injection*. |
| | | **36. Sinkronisasi Waktu** | **Bab 5.9.2.2 (1)**: Wajib menggunakan NTP Server. | **Bab 5.5.3**: Bukti sinkronisasi waktu pada OS/Perangkat. | **Bab 5.9.2.2**: Urutan kronologis log akurat antar sistem. |
| **7** | **Proteksi Data** | **37. Salinan Info Dikecualikan** | **Bab 5.8.4**: Kebijakan retensi dan backup data terbatas. | **Bab 5.11**: Jadwal backup berkala dan laporan status. | **Bab 5.11**: Data dapat dipulihkan 100% pasca insiden. |
| | | **38. Simpan Sementara Aman** | **Bab 5.6.1 (2)**: Hapus data sensitif dari memori pasca guna. | **Bab 5.6.1 (3)**: Audit kode manajemen memori (Clean memory). | **Bab 5.10.4**: Nihil kebocoran data via *Memory Dump*. |
| | | **39. Penghapusan Data** | **Bab 5.6.1 (2)**: Otorisasi & Audit Trail pertukaran data. | **Bab 5.8.4 (3)**: Berita Acara Pemusnahan Data. | **Bab 5.6.1**: Akuntabilitas siklus hidup data 100%. |
| | | **40. Keamanan Penyimpanan** | **Bab 5.8.1 (2)**: *Transparent Data Encryption* (TDE/LUKS). | **Bab 5.5.3**: Dokumen enkripsi disk di pusat data. | **Bab 5.10.4**: Data DB tetap aman meski media dicuri. |
| | | **41. Eksport & Hapus User** | **Bab 5.8.5 (4)**: Hak Portabilitas & Hak Penghapusan data. | **Bab 4.4.4**: Log permintaan penghapusan data pengguna. | **Bab 5.8.5**: Kepatuhan terhadap UU Pelindungan Data Pribadi. |
| | | **42. Bersih Memori** | **Bab 5.6.1 (2)**: Pembersihan memori aplikasi otomatis. | **Bab 5.6.1 (3)**: Verifikasi kode pembersihan variabel sensitif. | **Bab 5.10.4**: Nihil residu password di RAM. |
| **8** | **Komunikasi** | **43. Komunikasi Terenkripsi** | **Bab 5.6.1**: Hostname Enforcement & Tolak akses via IP. | **Bab 5.8.1 (3)**: Implementasi mTLS untuk antar sistem. | **Bab 5.6.1**: Seluruh traffic wajib melalui hostname SSL resmi. |
| | | **44. Koneksi Masuk/Keluar** | **Bab 5.5.5**: Filter firewall & gateway enkripsi global. | **Bab 5.5.5**: Ruleset WAF/Firewall yang membatasi akses. | **Bab 4.2.3**: Hasil scan port tidak menunjukkan kebocoran. |
| | | **45. Jenis Algoritma Komunikasi** | **Bab 5.8.1 (3)**: TLS 1.2/1.3 wajib, TLS 1.1 dilarang. | **Bab 5.8.1 (3)**: Hasil scan SSLLabs rating Grade A. | **Bab 5.2.4**: Tidak ada penggunaan cipher lemah (NULL/RC4). |
| | | **46. Sertifikat Elektronik** | **Bab 5.8.6**: Penggunaan layanan sertifikat BSrE-BSSN. | **Bab 5.8.6 (3)**: Dokumen registrasi sertifikat pegawai. | **Bab 5.8.6 (4)**: Validitas tanda tangan 100% saat verifikasi. |
| **9** | **Kode Berbahaya** | **47. Analisis Kode (SAST)** | **Bab 5.6.1 (3)**: Penggunaan tools SAST (SonarQube/Deepsource). | **Bab 5.6.1 (3)**: Laporan scan kerentanan kode sumber. | **Bab 4.2.3**: Penurunan jumlah temuan celah keamanan aplikasi. |
| | | **48. Pustaka Pihak Ketiga** | **Bab 5.6.1 (3)**: Software Composition Analysis (SCA). | **Bab 5.9.4**: Daftar pustaka yang telah diaudit kerentanannya. | **Bab 5.6.1**: Nihil penggunaan library dengan celah kritis (CVE). |
| | | **49. Izin Fitur & Privasi** | **Bab 5.6.1 (2)**: Mekanisme kelola izin (Akses data/lokasi/sensor). | **Bab 4.4.4**: Bukti persetujuan izin (consent) oleh pengguna. | **Bab 5.10.4**: Nihil pelanggaran akses sensor tanpa izin. |
| | | **50. Integritas Software** | **Bab 5.8.2**: Hash verifikasi & File Integrity Monitoring (FIM). | **Bab 5.5.3**: Dokumen konfigurasi monitor integritas file. | **Bab 5.10.4**: Nihil modifikasi kode ilegal di server produksi. |
| | | **51. Fitur Pembaruan** | **Bab 5.6.1 (4)**: Verifikasi Digital Signature pada paket update. | **Bab 5.9.1**: Log pembaruan sistem yang ditandatangani. | **Bab 5.6.1**: Keamanan supply chain dan integritas update. |
| **10** | **Logika Bisnis** | **52. Alur Langkah Realistis** | **Bab 5.6.1 (2)**: Memastikan urutan langkah logika benar. | **Bab 4.4.4**: Dokumen *Workflow Business Logic* aplikasi. | **Bab 5.10.4**: Nihil serangan *Business Logic Bypass*. |
| | | **53. Validasi Logika Bisnis** | **Bab 5.6.1 (2)**: Validasi terhadap risiko (limit/kuota). | **Bab 5.6.1 (3)**: Hasil pengujian manual terhadap anomali logika. | **Bab 5.10.4**: Nihil manipulasi nilai antar langkah alur bisnis. |
| | | **54. Monitoring Pengujian** | **Bab 5.9.2.2**: Aktivitas pengujian tercatat di SIEM. | **Bab 5.5.5**: Log WAF/Firewall yang menjaring aktivitas testing. | **Bab 5.9.2.2**: Ketersediaan data investigasi pasca pengujian. |
| | | **55. Anti Otomatisasi** | **Bab 5.6.1 (2)**: Rate limiting & Anti-bot sbg filter masif request. | **Bab 5.5.5**: Konfigurasi WAF anti-DDoS aktif. | **Bab 5.6.3**: Ketahanan terhadap serangan bot masif. |
| | | **56. Notifikasi Peringatan** | **Bab 5.9.2.2 (2)**: Mekanisme Alerting Real-time (Alerting). | **Bab 4.4.4**: Screenshot dasbor peringatan serangan aktif. | **Bab 5.9.2.2**: Kecepatan respon terhadap anomali serangan. |
| **11** | **Keamanan File** | **57. Kuota Unggah** | **Bab 5.6.1 (2)**: Batas kuota file (PDF 10MB, JPG 2MB). | **Bab 4.4.4**: Bukti penolakan file saat melampaui kuota. | **Bab 5.9.1**: Stabilitas storage terjaga 100%. |
| | | **58. Validasi Tipe Konten** | **Bab 5.6.1 (2)**: Cek *Magic Number* & MIME-Type server side. | **Bab 5.6.1 (3)**: Review kode fungsi pengecekan tipe file. | **Bab 5.10.4**: Nihil file berbahaya (.php/.exe) terunggah. |
| | | **59. Sanitasi Metadata** | **Bab 5.6.1 (2)**: Penghapusan metadata file pasca unggah. | **Bab 5.6.1 (3)**: Bukti hilangnya EXIF/Metadata pada file unduhan. | **Bab 5.8.5**: Pelindungan privasi informasi dalam file. |
| | | **60. Scan Antivirus File** | **Bab 5.6.1 (2)**: Pengecekan antivirus pada file yang diunggah. | **Bab 4.4.4**: Log antivir scanner saat proses intake file. | **Bab 4.2.1**: Dari direktori penyimpanan bersih dari virus. |
| | | **61. Unduhan Aman** | **Bab 5.6.1 (2)**: Penegakan tipe file & Larangan script pada download. | **Bab 4.4.4**: Bukti header Content-Type yang sesuai pada file. | **Bab 5.10.4**: Nihil serangan *Cross-Site Scripting* via unduhan. |
| **12** | **API & Integrasi** | **62. Konfigurasi Layanan Web** | **Bab 5.6.3**: Standar integrasi REST API Kota Mojokerto. | **Bab 5.6.1 (3)**: Laporan audit hardening server web. | **Bab 5.6.3**: API hanya dapat diakses oleh client terdaftar. |
| | | **63. Info Celah API** | **Bab 5.6.3 (4)**: Larangan info sensitif pada URI/URL (Query String). | **Bab 4.4.4**: Hasil test request API (Status 200/400). | **Bab 5.10.4**: Nihil info bocor di URI atau body request. |
| | | **64. Otorisasi API (Level 3)** | **Bab 5.6.3 (2)**: Otorisasi wajib sesuai role dan akses (mTLS). | **Bab 5.6.3 (5)**: Log akses antar sistem ber-token. | **Bab 5.10.4**: Nihil akses ilegal ke data privat API. |
| | | **65. Metode HTTP API** | **Bab 5.6.3 (4)**: Pembatasan metode HTTP (Allow GET, POST). | **Bab 5.9.1**: Hasil intercept penolakan metode TRACE/OPTIONS. | **Bab 5.6.3**: Penurunan celah serangan berbasis metode HTTP. |
| | | **66. Validasi Skema API** | **Bab 5.6.3 (4)**: Mekanisme Validasi Skema (Schema Validation). | **Bab 5.6.1 (3)**: Dokumen spesifikasi skema API PD. | **Bab 5.10.4**: Nihil input malformasi yang diterima oleh API. |
| | | **67. Anti-Otomatisasi API** | **Bab 5.6.3 (4)**: Pembatasan jumlah request per klien (Rate Limit). | **Bab 5.5.5**: Konfigurasi API Gateway dengan limit aktif. | **Bab 5.6.3**: API tetap responsif meskipun di bawah serangan. |
| **13** | **Konfigurasi** | **68. Hardening Server** | **Bab 5.5.3**: Hardening sebelum masuk jaringan produksi. | **Bab 5.5.3**: Laporan *Baseline Security Audit* server. | **Bab 4.2.3**: Hasil VA menunjukkan status *Hardened*. |
| | | **69. Dokumentasi Dependensi** | **Bab 5.9.3**: Mekanisme pencatatan perubahan & dependensi. | **Bab 4.4.4**: Inventaris library & konfigurasi dependensi. | **Bab 5.6.1 (3)**: Laporan Software Composition Analysis (SCA). |
| | | **70. Hapus Fitur Tak Perlu** | **Bab 5.6.1 (2)**: Hapus dokumentasi, sampel, & konfigurasi sisa. | **Bab 5.9.1**: Bukti penghapusan akun guest/test default. | **Bab 5.5.3**: Tidak ada port terbuka yang tidak terdaftar. |
| | | **71. Integritas Aset (SRI)** | **Bab 5.6.1 (2)**: Header integrity pada file eksternal/download. | **Bab 4.4.4**: Bukti hash pada link unduhan sistem. | **Bab 5.9.3**: Aset tetap orisinial meski diakses publik. |
| | | **72. Respon Aman (Header)** | **Bab 5.6.1 (2)**: Masking header sensitif (Server/X-Powered-By). | **Bab 4.4.4**: Screenshot header respon HTTP dari server. | **Bab 5.6.1 (2)**: Hasil intercept tidak menunjukkan info teknis. |

---

### **Catatan Penggunaan Rekaman Bukti (KEI):**
Seluruh sub-poin implementasi (**KEI**) di atas mewajibkan instansi untuk menyimpan:
1.  **Log Sistem**: Mencatat aktivitas teknis secara otomatis.
2.  **Screenshot Konfigurasi**: Membuktikan fitur keamanan telah diaktifkan.
3.  **Berita Acara / Laporan**: Membuktikan proses manual (seperti Pentest, Hardening, Pemusnahan) telah dilaksanakan.

Dokumen ini disusun sebagai panduan teknis bagi Auditor dalam melakukan verifikasi lapangan terhadap Pedoman SMKI Kota Mojokerto.
