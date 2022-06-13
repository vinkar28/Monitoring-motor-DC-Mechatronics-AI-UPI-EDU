# Monitoring Arus, Daya, Tegangan dan Kecepatan Motor DC Menggunakan NodeMCU ESP8266 yang Terintegrasi Dengan Database MySQL

Repository ini merupakan dokumentasi projek UAS Kelompok 5 mata kuliah Sensor dan Tranduser.

Anggota Tim :
<li> Geralda Livia Nugraha (2100179) </li>
<li> Ramadhirra Azzahra Putri (2100188) </li>
<li> Vinka Reviansa (2101918) </li> 
<li> Muhammad Wildan Alfarizy (2106373) </li> 
<li> Muhammad Mizanulkhair (2107620) </li> 


## Latar Belakang

Teknologi yang berkembang saat ini sangat berdampak pada kehidupan manusia. Terlebih lagi dengan hadirnya transistor, IC, dan perangkat elektronika lainnya yang mampu menciptakan prosesor-prosesor kecil dengan kemampuan komputasi, performa, keandalan serta efisiensi yang tinggi. Hal ini tentu saja dapat dimanfaatkan untuk mempermudah kegiatan sehari-hari, mulai <i>troubleshooting</i> hingga memberi komando pada asisten virtual untuk mengetahui prediksi cuaca 5 jam yang akan datang.

Meski terkesan sederhana, banyak sekali aktivitas "harian" yang sebenarnya akan terasa berat apabila dilakukan secara manual dan terus-menerus. Mayoritas pabrik lebih memilih untuk menggunakan mesin otomatis guna melakukan operasi sederhana berbalut looping, seperti melipat atau memindahkan barang, bukan tanpa alasan, tetapi
karena ingin meminimalisir human error yang mungkin saja terjadi. Human error, dalam industri maupun tidak, dapat berdampak fatal dan berpotensi untuk mengancam keselamatan jiwa. Salah satu kegiatan yang rentan mengalami kejadian ini adalah menghitung, di mana miskalkulasi merupakan hal yang sering terjadi. Apabila disandingkan dengan aktivitas monoton lainnya, seperti mencatat dan memonitor, maka semakin tinggi pula kemungkinan terjadinya human error. Beberapa kesalahan
memang tidak mematikan atau dapat dikategorikan sebagai <i>harmless</i>, tetapi tentu saja tetap menghambat banyak hal seperti waktu, efisiensi, dan sebagainya.

Mari kita ambil contoh kasus yang sering ditemukan, yakni troubleshooting pada sebuah sistem yang mengalami malfungsi pada bagian motor DC-nya. Dikarenakan motor DC merupakan alat yang hadir pada kebanyakan perangkat elektronika, seharusnya proses troubleshooting ini mudah untuk dilakukan, kan? Meski kita tidak asing dengan presensi motor DC ini, untuk mencari akar permasalahan tentu kita harus melewati proses yang tidak begitu sederhana, seperti memonitor dan menghitung variabel-variabel yang jumlahnya lebih dari satu, seperti jumlah putaran per menit (rpm), tegangan yang berada pada sistem, dan sebagainya, baru setelah data itu diperoleh kita dapat melakukan analisis hingga sebuah kesimpulan diperoleh. Proses monitoring, pencatatan, dan percobaan tersebut memang dapat dilakukan dengan mudah dengan menggunakan multimeter lalu mencatat hasil yang didapatkan, namun hal ini cukup memakan waktu. Olek karena itu, dibutuhkan otomatisasi guna mempermudah proses troubleshooting ini,
di mana kita dapat melakukan perhitungan lalu memonitor hasilnya di mana saja, kapan saja, dan juga dapat meng-export data yang diperoleh untuk melakukan graphing
atau analisis lainnya.



## Solusi

Berdasarkan uraian latar belakang, solusi yang kami tawarkan untuk mengendalikan motor DC adalah dengan menggunakan sensor NodeMCU ESP8266, INA219, dan Speed LM393 yang terintegrasi pada database MySQL. Sistem hardware berfungsi untuk mengukur tegangan dan arus (Sensor INA219) dan mengukur kecepatan motor (Sensor LM393). Kemudian nilai yang dibaca oleh sensor akan diolah datanya pada NodeMCU ESP8266 setelah itu NodeMCU ESP8266 akan mengirim data ke database MySQL. 
Dengan adanya hal ini, diharapkan dapat mempermudah proses monitoring, pencatatan, dan pengolahan data pada motor DC.


## Analisis dan Diskusi Project

Monitoring motor DC adalah sebuah alat yang digunakan untuk monitoring arus, tegangan, daya, dan kecepatan motor secara otomatis.

### Alat dan Bahan

<li> Speed Sensor LM393 </li>
<li> INA 219 </li>
<li> Driver L298N </li>
<li> Node MCU ESP8266 </li>
<li> Motor DC </li>
<li> Potensiometer 5k </li>
<li> Breadboard </li>
<li> Baterai (Vsource) </li>
<li> Kabel Jumper </li>

## Mekanisme Kerja

> 1. Pertama NodeMCU ESP8266 akan menghubungkan jaringan ke Wi-Fi dan server lokal. Jika tidak terhubung maka akan dilakukan konektivitas ulang hingga NodeMCU terhubung, jika terhubung maka akan dilakukan langkah selanjutnya.
> 2. Selanjutnya NodeMCU akan mendeteksi apakah sensor INA219 dan LM393 sudah terhubung dengan baik dan akan inisialisasi pin sensor.
> 3. Selanjutnya Sensor INA219 akan membaca nilai tegangan dan arus serta sensor LM393 akan membaca nilai kecepatan.
> 4. Selanjutnya NodeMCU ESP8266 menerima data dari sensor dan mengolah data teersebut.
> 5. Selanjutnya NodeMCU ESP8266 mengirim data sensor ke database MySQL.
> 6. Langkah terakhir menampilkan data yang berupa nilai dari pembacaan sensor pada website.


## Kesimpulan

> Dari perancangan dan pengujian aplikasi monitoring yang telah dilakukan terhadap fitur-fitur pada sistem monitoring berbasis website, semua fitur dapat berjalan sebagaimana mestinya. Monitoring arus, tegangan, daya, dan kecepatan motor secara otomatis menggunakan sensor INA219 dan speed sensor LM393 yang kemudian mengirimkannya ke database Mysql. Data dikirim dari database ke web menggunakan software Visual Code dengan menggunakan PHP dan HTML sederhana.


## Lampiran

### Tampilan Sensor
https://user-images.githubusercontent.com/107344746/173241731-40c883b5-0394-4809-8d36-bd3ee288ca31.mp4

### Demo Sensor
https://user-images.githubusercontent.com/107428291/173409790-33fbf080-6f4b-4e69-808f-d37efeb7c691.mp4
### Tampilan Aplikasi Pada Smartphone
> <img alt="Tampilan Aplikasi Pada Smartphone" src="https://i.ibb.co/qFxbh3X/Screenshot-20220613-072457-Video-Player.jpg" width="70%" height="70%">

### Tampilan Database pada MySQL
> <img alt="Tampilan Database pada MySQL" src="https://i.ibb.co/YtfCtp1/Screenshot-219.jpg" width="70%" height="70%">

### Wiring Diagram
> <img alt="Wiring Diagram" src="https://i.postimg.cc/nLskN6dt/Whats-App-Image-2022-06-12-at-18-18-55.jpg" width="70%" height="70%">

### Review Paper
> + [Review Paper](https://drive.google.com/drive/folders/1_dpZ5RZMZVyhly4pX0sPtSiqoRcTCKQn?usp=sharing)

### Link Youtube
> + [YouTube](https://youtube.com/playlist?list=PLaxTMjqPY5Ctf2KR1V5fZoZbjmiYFc8d7)

### Link File PHP
> + [File PHP (.php)](https://www.dropbox.com/s/2hlqb13b483a4c5/php%20files.rar?dl=0)


## Referensi
 
> + https://www.nyebarilmu.com/apa-itu-module-nodemcu-esp8266/#:~:text=NodeMCU%C2%A0ESP8266%C2%A0merupakan%20modul%20turunan%20pengembangan%20dari%20modul%20platform%20IoT,yang%20membedakan%20yaitu%20dikhususkan%20untuk%20%E2%80%9CConnected%20to%20Internet%E2%80%9C.

> + https://kelasrobot.com/apa-itu-nodemcu-esp8266-bagaimana-cara-pakenya/

> + https://www.nn-digital.com/blog/2019/06/09/belajar-modul-ina219-sensor-arus-tegangan-daya-dengan-arduino/

> + https://siddix.blogspot.com/2019/02/pengertian-dan-cara-kerja-ic-komparator.html

> + https://www.mahirelektro.com/2020/02/tutorial-menggunakan-driver-motor-l298n-pada-Arduino.html
 
 
