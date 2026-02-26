
STANDAR TEKNIS DAN PROSEDUR KEAMANAN
APLIKASI BERBASIS WEB

Petunjuk Teknis, Penjelasan dan Pengujian setiap fungsi kontrol keamanan
Standar Teknis Dan Prosedur Keamanan Aplikasi berbasis Web merupakan
prosedur yang dapat dilakukan oleh Auditor Keamanan SPBE Keamanan untuk
mendapatkan bukti data dukung pengujian kontrol keamanan.

A. Kontrol Keamanan pada area Standar Teknis dan Prosedur Keamanan
Kontrol  Keamanan  pada  area  Standar  Teknis  dan  Prosedur  Keamanan
Aplikasi Berbasis Web berjumlah 72 kontrol keamanan yang terdiri dari 13
fungsi diuraikan sebagai berikut :

1.  Fungsi : Pasal 27 ayat (1) tentang Autentikasi (Kontrol 1-7);

2.  Fungsi : Pasal 27 ayat (2) tentang Manajemen Sesi (Kontrol 8-14);

3.  Fungsi : Pasal 27 ayat (3) tentang Kontrol Akses (Kontrol 15-18);

4.  Fungsi : Pasal 27 ayat (4) tentang Validasi Input (Kontrol 19-25);

5.  Fungsi : Pasal 27 ayat (5) tentang Kriptografi pada Verifikasi Statis
(Kontrol 26-29);

6.  Fungsi : Pasal 27 ayat (6) tentang Penanganan Error dan Pencatatan
Log (Kontrol 30-36);

7.  Fungsi : Pasal 27 ayat (7) tentang Proteksi Data (Kontrol 37-42);

8.  Fungsi : Pasal 27 ayat (8) tentang Keamanan Komunikasi (Kontrol 43-

46);

9.  Fungsi : Pasal 27 ayat (9) tentang Pengendalian Kode Berbahaya
(Kontrol 47-51);

10. Fungsi : Pasal 27 ayat (10) tentang Logika Bisnis (Kontrol 52-56);

11. Fungsi : Pasal 27 ayat (11) tentang File (Kontrol 57-61);

12. Fungsi : Pasal 27 ayat (12) tentang Keamanan Application programming
interface dan Web Service (Kontrol 62-67); dan

13. Fungsi : Pasal 27 ayat (13) tentang Keamanan Konfigurasi (Kontrol 68-

72).

K1.  Menggunakan manajemen kata sandi untuk proses autentikasi


Deskripsi/
Tujuan

Memastikan penerapan manajemen kata sandi
yang memadai dalam rangka proses autentikasi
yang efektif.


- 58 -


Referensi
Kontrol
Keamanan

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 1 poin a

● OWASP ASVS v.4.0.3 – 2

● WSTG-ATHN-02

● CWE-521

K2.  Menerapkan verifikasi kata sandi pada sisi server


Deskripsi/
Tujuan

Referensi
Kontrol
Keamanan

Memastikan bahwa tidak ada penggunaan kata
sandi yang masuk dalam kategori lemah (baik itu
lemah karena sering digunakan ataupun lemah
dikarenakan bersifat default dari suatu produk).

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 1 poin b

● OWASP ASVS v.4.0.3 – 2.2.1

● WSTG-ATHN-02

● CAPEC-16

● CWE-307

● CWE-1392

● CWE-1393

● CAPEC-70

K3.  Mengatur jumlah karakter, kombinasi jenis karakter, dan masa berlaku
dari kata sandi


Deskripsi/
Tujuan
Referensi
Kontrol
Keamanan

Mengatur  jumlah  karakter,  kombinasi  jenis
karakter, dan masa berlaku dari kata sandi.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 1 poin c

● OWASP ASVS v.4.0.3 – 2.1.1; 2.1.2; 2.1.4

● WSTG-ATHN-02

● CAPEC-16

● CWE-521

● CWE-1392

● CWE-1393

● CAPEC-70

K4.  Mengatur jumlah maksimum kesalahan dalam pemasukan kata sandi


Deskripsi/
Tujuan
Referensi
Kontrol
Keamanan

Melindungi sistem dari percobaan menebak kata
sandi dan akses ilegal ke dalam sistem.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 1 poin d

● OWASP ASVS v.4.0.3 – 2.2.1

● WSTG-ATHN-03

● CWE-307

● CWE-654

K5.  Mengatur mekanisme pemulihan kata sandi


- 59 -


Deskripsi/
Tujuan

Referensi
Kontrol
Keamanan

Memastikan   bahwa   terdapat   mekanisme
pemulihan  kata  sandi  yang  memadai  pada
aplikasi.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 1 poin e

● OWASP ASVS v.4.0.3 – 2.1.5; 2.1.6; 2.5.3

● WSTG-ATHN-09

● CAPEC-50

● CWE-620

● CWE-640

K6.  Menjaga kerahasiaan kata sandi yang disimpan melalui mekanisme
kriptografi.


Deskripsi/
Tujuan

Referensi
Kontrol
Keamanan

Memastikan  kerahasiaan  kata  sandi  yang
disimpan  dalam  keadaan  terenkripsi  dan
memitigasi  risiko  pengungkapan  kata  sandi
dalam keadaan terbaca dengan jelas (Clear text).

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 1 poin f

● OWASP ASVS v.4.0.3 – 2.4.1

● WSTG-ATHN-02

● CWE-916

K7.  Menggunakan  jalur  komunikasi  yang  diamankan  untuk  proses
autentikasi


Deskripsi/
Tujuan

Referensi
Kontrol
Keamanan

Memastikan  bahwa  jalur  komunikasi  yang
digunakan oleh aplikasi telah sesuai dengan
common practice dan standar keamanan yang
menjadi rujukan secara internasional.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 1 poin g

● OWASP ASVS v.4.0.3 – 2.7.4

● WSTG-CRYP-01

● WSTG-CRYP-03

● CWE-295

● CWE-311

● CWE-523

● CAPEC-217

K8.  Menggunakan pengendali sesi untuk proses manajemen sesi


Deskripsi/
Tujuan

Referensi
Kontrol
Keamanan

Memastikan aplikasi memiliki pengendali sesi
yang memiliki fungsi untuk membatasi suatu
peran dari pengguna.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 2 poin a

● OWASP ASVS v.4.0.3 – 3


- 60 -

● WSTG-SESS-01

● WSTG-SESS-02

● WSTG-SESS-03

● CWE-598

K9.  Menggunakan pengendali sesi yang disediakan oleh kerangka kerja
aplikasi


Deskripsi/
Tujuan
Referensi
Kontrol
Keamanan

Memastikan penerapan sesi pada aplikasi untuk
autentikasi berkelanjutan.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 2 poin b

● WSTG-SESS-01

K10. Mengatur pembuatan dan keacakan token sesi yang dihasilkan oleh
pengendali sesi


Deskripsi/
Tujuan
Referensi
Kontrol
Keamanan

Memastikan pembuatan dan keacakan token
sesi yang dibuat.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 2 poin c

● OWASP ASVS v.4.0.3 – 3.2.1; 3.2.4

● WSTG-SESS-01

● CWE-384

● CWE-331

K11. Mengatur kondisi dan jangka waktu habis sesi


Deskripsi/
Tujuan

Referensi
Kontrol
Keamanan

Memastikan  terdapatnya  mekanisme  log  out
otomatis, manajemen batas waktu, kadaluarsa,
serta   penghancuran   sesi   dalam   rangka
memitigasi penggunaan     berulang nilai sesi
yang sama pada kondisi idle di rentang waktu
tertentu.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 2 poin d

● OWASP ASVS v.4.0.3 – 3.3.1; 3.3.2

● WSTG-SESS-07

● CWE-613

K12. Validasi dan pencantuman session id


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan bahwa setiap sesi yang terbentuk
memiliki keunikan session ID tersendiri

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 2 poin e

● OWASP ASVS v.4.0.3 – 3.4.1; 3.4.2; 3.4.3;

3.4.4

● WSTG-SESS-01

● WSTG-SESS-02


- 61 -

● WSTG-SESS-03

● CWE-614

● CWE-1004

● CWE-16

K13. Pelindungan  terhadap  lokasi  dan  pengiriman  token  untuk  sesi
terautentikasi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  pengiriman  token  hanya
dilakukan pada jalur yang aman dan dengan
atribut yang sesuai best practice.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 2 poin f

● OWASP ASVS v.4.0.3 – 3.2.3

● WSTG-SESS-02

● WSTG-SESS-03

● CWE-539

K14. Pelindungan terhadap duplikasi dan mekanisme persetujuan pengguna


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan aplikasi melakukan pembangkitan
session baru saat pengguna login kembali.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 2 poin g

● OWASP ASVS v.4.0.3 – 3.2.1

● CWE-384

K15. Menetapkan otorisasi pengguna untuk membatasi kontrol akses


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  supaya  setiap  peran  (role)  dari
pengguna berjalan sesuai dengan yang telah
ditentukan (baik dari eksekusi Create, Read,
Update, maupun Delete).

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 3 poin a

● OWASP ASVS v.4.0.3 – 4.1.3

● CAPEC-180

● CWE-284

● CWE-285

● WSTG-ATHZ-03

● WSTG-ATHZ-04

K16. Mengatur peringatan terhadap bahaya serangan otomatis apabila terjadi
akses yang bersamaan atau akses yang terus-menerus pada fungsi


Deskripsi/
Tujuan

Mencegah terjadinya serangan secara otomatis
yang dapat membuat seorang penyerang untuk
dapat meraih akses ke dalam suatu aplikasi,
melakukan pengambilan data secara masif dan


- 62 -


Referensi Kontrol
Keamanan

otomatis, atau bahkan membuat suatu sistem
menjadi down.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 3 poin b

● OWASP ASVS v.4.0.3 – 4.2.2

● WSTG-ERRH-01

● CAPEC-112

● CAPEC-125

● CWE-352

● CWE-400

● CWE-770

● CWE-799

K17. Mengatur antarmuka pada sisi administrator


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  suatu  aplikasi  memiliki
pengaturan pada sisi administrator yang dapat
digunakan untuk memperkuat keamanan akses
terhadap sisi administrator itu sendiri.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 3 poin c

● WSTG-CONF-05

● CWE-419

K18. Mengatur verifikasi kebenaran token ketika mengakses data dan
informasi yang dikecualikan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan bahwa suatu data dan informasi
hanya  dapat  diakses  oleh  pengguna  yang
legitimate.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 3 poin d

● OWASP ASVS v.4.0.3 – 4.3.3

● CWE-732

K19. Menerapkan fungsi validasi input pada sisi server


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Melakukan   sanitasi   terhadap   input   yang
dilakukan  pengguna  dalam  rangka  mitigasi
serangan seperti XSS, SQLi, dan lain-lain

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 4 poin a

● OWASP ASVS v.4.0.3 – 5.1.3

● WSTG-INPV-01

● WSTG-INPV-02

● CWE-20

K20. Menerapkan mekanisme penolakan input jika terjadi kesalahan validasi


Deskripsi/
Tujuan

Untuk melakukan pemeriksaan terhadap input
yang  dilakukan  pengguna  ,  dalam  rangka


- 63 -


Referensi Kontrol
Keamanan

mitigasi format data yang tidak sesuai, dan telah
ditetapkan oleh aplikasi

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 4 poin b

● OWASP ASVS v.4.0.3 – 5.1.5

● CWE-601

K21. Melakukan validasi positif pada seluruh input


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Untuk melakukan penyaringan terhadap input
yang dilakukan pengguna melalui mekanisme
mendefinisikan  daftar  putih  (white  listing),
terhadap   tag  atau  atribut  html  yang
diperbolehkan pada aplikasi.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 4 poin c

● OWASP ASVS v.4.0.3 – 5.1.3

● CWE-20

K22. Melakukan filter terhadap data yang tidak dipercaya


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Melakukan penyaringan terhadap input yang
diberikan pengguna, melalui entry point seperti
form yang di-submit, atau parameter pada url.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 4 poin e

● OWASP ASVS v.4.0.3 – 5.1; 5.2

● WSTG-INPV-04

● CWE-94

● CWE-95

● CWE-116

● CWE-138

● CWE-147

● CWE-159

● CWE-918

K23. Menggunakan fitur kode dinamis


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Menemukenali  penggunaan  dari  fitur  kode
dinamis pada aplikasi dalam rangka melakukan
proses encoding atau atau mengganti dengan
karakter unicode terhadap inputan penggunaan
yang  tidak  sesuai  dengan  aturan  yang
ditetapkan.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 4 poin f

● OWASP ASVS v.4.0.3 – 5.2.4; 5.3

● CWE-95

K24. Melakukan pelindungan terhadap akses yang mengandung konten skrip


- 64 -


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Melindungi aplikasi dari inputan pengguna yang
mengandung skrip, ataupun percobaan serangan
melalui entry point (seperti form yang di-submit,
atau parameter pada url, textfield pada fitur
pencarian, dan lain - lain).

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 4 poin g

● OWASP ASVS v.4.0.3 – 5.1; 5.2.7; 5.2.8

● WSTG-INPV-01

● WSTG-INPV-02

● WSTG-INPV-03

● CWE-94

● CWE-159

K25. Melakukan pelindungan dari serangan injeksi basis data


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Mengidentifikasi potensi injeksi pada aplikasi,
guna memitigasi potensi serangan seperti SQLi,
terganggunya  kerahasiaan  data  seperti
kebocoran  data, akses yang tidak sah ke data
yang bersifat sensitif atau terganggunya aspek
integritas data ataupun ketersediaannya.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 4 poin h

● OWASP ASVS v.4.0.3 – 5.1; 5.3.4; 5.3.5

● WSTG-INPV-05

● CWE-89

K26. Menggunakan  algoritma  kriptografi,  modul  kriptografi,  protokol
kriptografi, dan kunci kriptografi sesuai dengan ketentuan peraturan
perundang-undangan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  aplikasi  telah  didesain
dengan identifikasi dan implementasi penerapan
kriptografi dalam arsitektur aplikasinya guna
melindungi aset data sesuai dengan kebutuhan
dan klasifikasi informasinya untuk memberikan
jaminan keamanan aspek kerahasiaan, keaslian,
keutuhan,    kenirsangkalan,    dan/atau
ketersediaan. Desain kontrol yang dapat menjadi
rujukan umumnya berupa kebijakan password,
arsitektur aplikasi, arsitektur database, ataupun
saluran komunikasi yang digunakan, baik itu
data  at rest dan data in transit.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 5 poin a

● OWASP ASVS v.4.0.3 – 6.1; 6.2.3

● CWE-311

● CWE-326


- 65 -

K27. Melakukan autentikasi data yang dienkripsi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan   bahwa   aplikasi   memenuhi
persyaratan  seluruh  modul  kriptografi  yang
digunakan  telah  diimplementasikan  dengan
benar  untuk  menjamin  data  yang  dienkripsi
adalah asli dan utuh sehingga dapat dilakukan
verifikasi atau validasi

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 5 poin b

● OWASP ASVS v.4.0.3 – 6.2.7

● CWE-326

K28. Menerapkan manajemen kunci kriptografi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan        bahwa        aplikasi
mengimplementasikan   manajemen   kunci
kriptografi  yang  aman  dari  seluruh  tahapan
siklus hidup kunci kriptografi

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 5 poin c

● OWASP ASVS v.4.0.3 – 6.4.1

● CWE-798

K29. Membuat angka acak yang menggunakan generator angka acak
kriptografi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan       bahwa       aplikasi
mengimplementasikan  pembangkitan  angka
acak kriptografi yang aman dalam setiap modul
aplikasi yang membutuhkan angka acak seperti
token, initialization vector, seed, ataupun master
key

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 5 poin d

● OWASP ASVS v.4.0.3 – 6.3.1

● CWE-338

K30. Mengatur konten pesan yang ditampilkan ketika terjadi kesalahan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  Aplikasi  hanya  akan
menampilkan pesan bersifat umum yang muncul
ketika terjadi eror

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 6 poin a

● OWASP ASVS v.4.0.3 – 7.4.1

● CWE-210


- 66 -

K31. Menggunakan metode penanganan eror untuk mencegah kesalahan
terprediksi dan tidak terduga serta menangani seluruh pengecualian
yang  tidak ditangani


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan bahwa Aplikasi memiliki metode
untuk  menangani  error  untuk  mencegah
kesalahan terprediksi dan tidak terduga

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 6 poin b

● OWASP ASVS v.4.0.3 – 7.4.1

● CWE-210

K32. Tidak mencantumkan informasi yang dikecualikan dalam pencatatan
log


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan    bahwa    Aplikasi    tidak
mencantumkan  informasi  yang  dikecualikan
dalam pencatatan log, dan hanya mencatat log
keamanan yang relevan dengan insiden seperti
autentikasi berhasil dan gagal, kegagalan akses
kontrol, kegagalan validasi input.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 6 poin c

● OWASP ASVS v.4.0.3 – 7.1.1; 7.1.2; 7.1.3

● CWE-532

● CWE-778

K33. Mengatur  cakupan  log  yang  dicatat  untuk  mendukung  upaya
penyelidikan ketika terjadi insiden


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  Aplikasi  telah  mengatur
cakupan log yang dicatat untuk mendukung
upaya penyelidikan ketika terjadi insiden

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 6 poin d

K34. Mengatur pelindungan log aplikasi dari akses dan modifikasi yang tidak
sah


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  aplikasi  telah  mengatur
pelindungan  log  aplikasi  dari  akses  dan
modifikasi yang tidak sah

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 6 poin e

● OWASP ASVS v.4.0.3 – 7.3.3

● CWE-200

K35. Melakukan enkripsi pada data yang disimpan untuk mencegah injeksi
log


- 67 -


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan bahwa semua komponen log harus
mendapatkan pengamanan, dengan cara enkripsi
pada  data  sebelum  dicatat  pada  log,  yang
berguna sebagai pencegahan injeksi log

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 6 poin f

● OWASP ASVS v.4.0.3 – 7.3.1

● CWE-117

K36. Melakukan sinkronisasi sumber waktu sesuai dengan zona waktu dan
waktu yang benar


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan bahwa sumber waktu pada Aplikasi
telah disinkronisasi dengan waktu dan zona
waktu yang tepat, dan disarankan menggunakan
UTC untuk memudahkan analisis forensik pasca
insiden

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 6 poin g

● OWASP ASVS v.4.0.3 – 7.3.4

K37. Melakukan  identifikasi  dan  penyimpanan  salinan  informasi  yang
dikecualikan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan   bahwa   seluruh   data   yang
teridentifikasi dibuat dan diproses oleh aplikasi
harus dipastikan terletak sesuai direktori yang
ditetapkan.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 7 poin a

● OWASP ASVS v.4.0.3 – 8.3.4

● CWE-200

K38. Melakukan pelindungan dari akses yang tidak sah terhadap informasi
yang dikecualikan yang disimpan sementara dalam aplikasi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  informasi  sensitif  yang
disimpan sementara dalam aplikasi diterapkan
perlindungan dari akses yang tidak sah

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 7 poin b

● OWASP ASVS v.4.0.3 – 8.3.6

● CWE-226

K39. Melakukan  pertukaran,  penghapusan,  dan  audit  informasi  yang
dikecualikan


Deskripsi/
Tujuan

Memastikan  bahwa  pada  Aplikasi  terdapat
mekanisme pertukaran, penghapusan, dan audit
informasi yang dikecualikan


- 68 -


Referensi Kontrol
Keamanan

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 7 poin c

● OWASP ASVS v.4.0.3 – 8.3.5

● CWE-532

K40. Memastikan data disimpan dengan aman


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan data disimpan dengan aman dan
backup data dilakukan secara aman

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 7 poin e

● OWASP ASVS v.4.0.3 – 8.3.7

● CWE-327

K41. Menentukan metode untuk menghapus dan mengekspor data sesuai
permintaan pengguna


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan terdapat metode untuk menghapus
dan  mengekspor  data  sesuai  permintaan
pengguna

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 7 poin f

● OWASP ASVS v.4.0.3 – 8.3.2

● CWE-212

K42. Membersihkan memori setelah tidak diperlukan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  dilakukan  pembersihan
memori setelah tidak diperlukan

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 7 poin g

● OWASP ASVS v.4.0.3 – 8.3.6

● CWE-226

K43. Menggunakan komunikasi terenkripsi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan   bahwa   aplikasi   memenuhi
persyaratan menggunakan TLS dengan enkripsi
yang   kuat dan terbaru, serta dikonfigurasi untuk
menonaktifkan  penggunaan  algoritma  yang
lemah,    telah usang, atau telah diketahui tidak
aman.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 8 poin a

● OWASP ASVS v.4.0.3 – 9.1.1

● CWE-319

K44. Mengatur koneksi masuk dan keluar yang aman dan terenkripsi dari
sisi pengguna


- 69 -


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan        bahwa       aplikasi
mengimplementasikan   setiap   konektivitas
transaksi elektronik yang dikirimkan pengguna
selalu melalui jaringan yang terenkripsi, serta
mereviu  konfigurasi  dari  sisi  klien  untuk
memastikan implementasi TLS 1.2 atau yang
terbaru telah terverifikasi.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 8 poin b

● OWASP ASVS v.4.0.3 – 9.2.2

● CWE-319

K45. Mengatur jenis algoritma yang digunakan dan alat pengujiannya


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  hanya  versi  protokol  TLS
terbaru  yang  diaktifkan,  serta  memastikan
terdapat  pengaturan  alat  pengujian  TLS  yang
akan digunakan oleh pemilik Aplikasi

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 8 poin c

● OWASP ASVS v.4.0.3 – 9.1.2; 9.1.3

● CWE-326

K46. Mengatur aktivasi dan konfigurasi sertifikat elektronik yang diterbitkan
oleh penyelenggara sertifikasi elektronik


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan terdapat pengaturan mekanisme
dan waktu aktivasi dan konfigurasi sertifikat TLS
yang dipakai pada aplikasi

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 8 poin d

● OWASP ASVS v.4.0.3 – 9.1.2; 9.1.3

● CWE-295

K47. Menggunakan analisis kode dalam kontrol kode berbahaya


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan bahwa terdapat tools analisis kode
yang dapat mendeteksi kode yang berpotensi
malicious

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 9 poin a

● OWASP ASVS v.4.0.3 – 10.1.1

● CWE-749

K48.  Memastikan kode sumber aplikasi dan pustaka tidak mengandung kode
berbahaya dan fungsionalitas lain yang tidak diinginkan


Deskripsi/
Tujuan

Memastikan  bahwa  kode  sumber  dan  library
pihak ketiga pada aplikasi, tidak mengandung
kode berbahaya serta tidak memiliki kemampuan


- 70 -


Referensi Kontrol
Keamanan

untuk mengumpulkan data. Jika memang harus
menggunakan  data  maka  harus  meminta
persetujuan dari user.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 9 poin b

● OWASP ASVS v.4.0.3 – 10.2.1

● CWE-359

K49. Mengatur izin terkait fitur atau sensor terkait privasi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan aplikasi tidak akan meminta izin
kepada   fitur   atau   akses   yang   tidak
diperlukan/berlebihan  kepada  sensor  seperti
kamera, microphone dan lokasi.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 9 poin c

● OWASP ASVS v.4.0.3 – 10.2.2

● CWE-272

K50. Mengatur pelindungan integritas


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  aplikasi  menggunakan
perlindungan integritas, seperti kode integritas
signature atau subresource.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 9 poin d

● OWASP ASVS v.4.0.3 – 10.3.2

● CWE-353

K51. Mengatur mekanisme fitur pembaruan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  bahwa  aplikasi  yang  memiliki
mekanisme  pembaruan  otomatis  klien  atau
server,  pembaruan  harus  diperoleh  melalui
saluran aman dan ditandatangani secara digital

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 9 poin e

● OWASP ASVS v.4.0.3 – 10.3.1

● CWE-16

K52. Memproses alur logika bisnis dalam urutan langkah dan waktu yang
realistis


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan aplikasi hanya akan memproses
aksi yang sesuai dengan logika bisnis dalam
urutan langkah dan waktu yang realistis

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 10 poin a

● OWASP ASVS v.4.0.3 – 11.1.1; 11.1.2

● CWE-841

● CWE-799


- 71 -

K53. Memastikan logika bisnis memiliki batasan dan validasi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan aplikasi mampu memvalidasi bahwa
aksi sesuai dengan logika bisnis

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 10 poin b

● OWASP ASVS v.4.0.3 – 11.1.5

● CWE-841

K54. Memonitor aktivitas yang tidak biasa


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Aplikasi  mampu  melakukan  pemantauan
terhadap  aktivitas  anomali  atau  yang  tidak
sesuai dengan logika bisnis

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 10 poin c

● OWASP ASVS v.4.0.3 – 11.1.7

● CWE-754

K55. Membantu dalam kontrol anti otomatisasi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Aplikasi memiliki kontol anti-otomatisasi untuk
melindungi dari permintaan akses berlebihan,
seperti serangan eksfiltrasi data secara masif dan
DDOS

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 10 poin d

● OWASP ASVS v.4.0.3 – 11.1.4

● CWE-770

K56. Memberikan peringatan ketika terjadi serangan otomatis atau aktivitas
yang tidak biasa


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Aplikasi mampu memberikan peringatan yang
dapat  dikonfigurasi  ketika  terdeteksinya
serangan otomatis atau aktivitas yang tidak biasa

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 10 poin f

● OWASP ASVS v.4.0.3 – 11.1.8

● CWE-390

K57. Mengatur jumlah file untuk setiap pengguna dan kuota ukuran file yang
diunggah


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Aplikasi mengatur file dan kuota ukuran file yang
diunggah  untuk  memastikan  bahwa  satu
pengguna  tidak  dapat  mengisi  penyimpanan
dengan banyak file, atau file yang terlalu besar.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 11 poin a

● OWASP ASVS v.4.0.3 – 12.1.3


- 72 -

● CWE-770

K58. Melakukan validasi file sesuai dengan tipe konten yang diharapkan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan file yang diunggah pada aplikasi
dilakukan  validasi  sesuai  dengan  metadata
untuk  mencegah  adanya  fungsi  yang  tidak
diinginkan.

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 11 poin b

● OWASP ASVS v.4.0.3 – 12.3

● CWE-22

● CWE-73

● CWE-78

● CWE-98

● CWE-641

● CWE-829

K59. Melakukan pelindungan terhadap metadata input dan metadata file


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  aplikasi  memiliki  mekanisme
pelindungan  terhadap  metadata  input  dan
metadata  file

● Peraturan Badan Siber dan Sandi Negara No.
4 Tahun 2021 pasal 27 ayat 11 poin c

● OWASP ASVS v.4.0.3 – 12.3.1; 12.3.2; 12.3.3

● CWE-22

● CWE-73

● CWE-98

K60. Melakukan pemindaian file yang diperoleh dari sumber yang tidak
dipercaya


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan setiap file yang didapatkan dari
sumber  yang  tidak  dipercaya  dilakukan
pemindaian  untuk  mencegah  adanya  konten
berbahaya (malicious content) pada aplikasi

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 11
poin  d

● OWASP ASVS v.4.0.3 – 12.4.2

● CWE-509

K61. Melakukan konfigurasi server untuk mengunduh file sesuai ekstensi
yang ditentukan


Deskripsi/
Tujuan

Memastikan terdapat konfigurasi pada server
yang  mengatur  proses  unduh  file  untuk
memastikan aplikasi hanya menyajikan file


- 73 -


Referensi Kontrol
Keamanan

tertentu guna mencegah kebocoran informasi
dan kode sumber yang tidak disengaja.

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 11
poin  e

● OWASP ASVS v.4.0.3 – 12.5.1

● CWE-552

K62. Melakukan konfigurasi layanan web


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan bahwa layanan web (Web Service)
pada aplikasi telah dikonfigurasikan dengan
baik.

● Perban Peraturan Badan Siber dan Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 12
poin  a

● OWASP ASVS v.4.0.3 – 13

K63. Memverifikasi uniform resource identifier Application programming
interface tidak menampilkan informasi yang berpotensi sebagai celah
keamanan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan bahwa tahap verifikasi pada Uniform
Resource Identifier (URI) Application programming
interface  tidak  menampilkan  informasi  yang
berpotensi sebagai celah keamanan.

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 12
poin  b

● OWASP ASVS v.4.0.3 – 13.1.1

● CWE-116

K64. Membuat keputusan otorisasi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan   otorisasi   pada   Application
programming interface berjalan dan terkontrol
dengan baik

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 12
poin  c

● OWASP ASVS v.4.0.3 – 13.1.4

● CWE-285

K65. Menampilkan metode RESTful hypertext transfer protocol apabila input
pengguna dinyatakan valid


Deskripsi/
Tujuan

Memastikan restful http valid berjalan dan dapat
mencegah    pengguna    normal    untuk
menggunakan  fitur  DELETE  atau  PUT  pada


- 74 -


Referensi Kontrol
Keamanan

Application programming interface dan resource
yang terlindungi

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 12
poin  d

● OWASP ASVS v.4.0.3 – 13.2.1

● CWE-650

K66. Menggunakan validasi skema dan verifikasi sebelum menerima input


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan validasi skema XSD berjalan pada
dokumen  XML  yang  ada  pada  Application
programming interface, dan memverifikasi input
pada kode sumber

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 12
poin  e

● OWASP ASVS v.4.0.3 – 13.3.1

● CWE-20

K67. Menerapkan kontrol anti otomatisasi


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan  Aplikasi  memiliki  kontrol  anti-
automasi sebagai langkah pengamanan dari
serangan exfiltrasi data yang masif, DDOS, dan
file uploads

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 12
poin  g

● OWASP ASVS v.4.0.3 – 11.1.4

● CWE-770

K68. Mengonfigurasi server sesuai rekomendasi server aplikasi dan kerangka
kerja aplikasi yang digunakan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan   konfigurasi   server   sesuai
rekomendasi server aplikasi dan kerangka kerja
aplikasi yang digunakan

● Perban Peraturan Badan Siber dan Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 13
poin  a

● OWASP ASVS v.4.0.3 – 14.1.3

● CWE-16

K69. Mendokumentasi, menyalin konfigurasi, dan semua dependensi


Deskripsi/
Tujuan

Memastikan       aplikasi       memiliki
konfigurasi/terdapat     mekanisme     dari
pemilik/pengelola      aplikasi      untuk
mendokumentasikan, menyalin konfigurasi, dan


- 75 -


Referensi Kontrol
Keamanan

semua  dependensi,  dan  memanfaatkan  hasil
dokumentasi untuk keperluan kritikal.

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 13
poin  b

● OWASP ASVS v.4.0.3 – 14.1.4

K70. Menghapus fitur, dokumentasi, sampel, dan konfigurasi yang tidak
diperlukan


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan       aplikasi       memiliki
konfigurasi/terdapat     mekanisme     dari
pemilik/pengelola  aplikasi  agar  semua  fitur,
dokumentasi, contoh aplikasi, dan konfigurasi
yang tidak diperlukan telah dihapus.

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 13
poin  c

● OWASP ASVS v.4.0.3 – 14.2.2

● CWE-1002

K71. Memvalidasi integritas aset jika aset aplikasi diakses secara eksternal


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan   terdapat   konfigurasi   atau
mekanisme  pada  aplikasi  terkait  validasi
integritas aset jika aset aplikasi diakses secara
eksternal

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 13
poin  d

● OWASP ASVS v.4.0.3 – 14.2.3

● CWE-829

K72. Menggunakan respons aplikasi dan konten yang aman


Deskripsi/
Tujuan

Referensi Kontrol
Keamanan

Memastikan HTTP Header atau komponen lain
pada aplikasi yang muncul saat respons tidak
boleh   memperlihatkan   adanya   informasi
mendetail mengenai versi komponen sistem yang
digunakan

● Perban  Peraturan  Badan  Siber  dan  Sandi
Negara No. 4 Tahun 2021 pasal 27 ayat 13
poin  e

● OWASP ASVS v.4.0.3 – 14.3.3

● CWE-200