<h3 align="center">SISTEM INFORMASI GEOGRAFI</h3>
<h3 align="center">
“KONFIGURASI MAP PROXY”
</h3>


<p align="center">
  <img src="https://github.com/nadiaaaAR/Geographic-Information-System/blob/master/img/mapproxy.jpg">
</p>


**1. Latar Belakang**
 MAP PROXY ,berfungsi untuk menampung hasil gambar dari mapserver agar konsumsi komputasi bisa direduksi.


**2. Pembahasan**

**a.	Pengertian MapProxy**

MapProxy (mapproxy.org) adalah open source ubin geospasial proxy yang mendukung proyeksi ulang. Awalnya dikembangkan oleh Omniscale Mapproxy adalah server proxy python untuk gambar geospasial. Hal ini dapat membaca data dari WMS, ubin, mapserver dan mapnik, dan cache dan melayani data bahwa sebagai WMS, WMTS, TMS dan KML. Hal ini juga dapat melakukan reprojections antara berbagai sistem koordinat referensi

**b.	Install MapProxy**

<p>-          Ketikkan “#install python-pip dan python-dev”
<p>-          Lalu “#pip install mapproxy”
<p>-          Setelah itu ketikkan “#install Vwsqi”
<p>-          Tunggu hingga proses selesai.


**c.	Konfigurasi MapProxy**
Ada dua file konfigurasi yang digunakan oleh MapProxy.

mappproxy.yaml

Ini adalah konfigurasi utama MapProxy. Ini mengkonfigurasi semua aspek server: Yang server harus dimulai, di mana berasal data dari, apa yang harus di-cache.

seed.yaml

File ini adalah konfigurasi untuk alat mapproxy-benih. Lihat penyemaian dokumentasi untuk informasi lebih lanjut.

Konfigurasi ini menggunakan format YAML. Wikipedia berisi pengenalan yang baik untuk YAML. Konfigurasi MapProxy dikelompokkan menjadi beberapa bagian, masing-masing mengkonfigurasi aspek yang berbeda dari MapProxy. Ini adalah bagian berikut:<br>

<p>•	GLOBALS: Internal dari MapProxy dan nilai-nilai default yang digunakan dalam bagian konfigurasi lainnya.
<p>•	Layanan: Layanan MapProxy penawaran, misalnya WMS atau TMS.
<p>•	sumber: Tentukan mana MapProxy dapat mengambil data baru.
<p>•	cache: Konfigurasi cache internal.
<p>•	lapisan: Konfigurasi lapisan yang MapProxy menawarkan. Setiap lapisan dapat terdiri dari beberapa sumber dan cache.
<p>•	grid: Tentukan grid yang menggunakan MapProxy untuk menyelaraskan gambar cache.<br>
Urutan bagian tidak penting, sehingga Anda dapat mengatur dengan cara Anda. <br>

Untuk membuat satu set baru file konfigurasi untuk MapProxy panggilan:<br>

mapproxy-util create -t base-config mymapproxy

Ini akan membuat direktori mymapproxy dengan contoh konfigurasi minimal (mapproxy.yaml dan seed.yaml) dan dua file konfigurasi contoh lengkap (full_example.yaml dan full_seed_example.yaml).

Lihat dokumentasi konfigurasi untuk informasi lebih lanjut. Dengan konfigurasi default data cache akan ditempatkan di subdirektori cache_data.

**Untuk memulai server tes:**

cd mymapproxy
mapproxy-util serve-develop mapproxy.yaml

Sudah ada lapisan tes dikonfigurasi yang mendapatkan data dari Omniscale OpenStreetMap WMS. Jangan ragu untuk menggunakan layanan ini untuk pengujian. 
MapProxy dilengkapi dengan layanan demo yang berisi daftar WMS semua dikonfigurasi dan lapisan TMS. Anda dapat mengakses layanan yang di http: // localhost: 8080 / demo /.



**3. Penutup**

**a. Kesimpulan**

MAP PROXY ,berfungsi untuk menampung hasil gambar dari mapserver agar konsumsi komputasi bisa direduksi, mappproxy.yaml Ini adalah konfigurasi utama MapProxy. Ini mengkonfigurasi semua aspek server: Yang server harus dimulai, di mana berasal data dari, apa yang harus di-cache.

*b. Saran**

Selanjutnya untuk mendalami materi Konfigurasi Map Proxy dengan membaca sumber-sumber yang tersedia di buku maupun internet, dan melakukan praktikum mandiri.

-------

**Link Github** 	            :  https://github.com/nadiaaaAR/Geographic-Information-System<br>

**Referensi**	                :  https://mapproxy.org/docs/nightly/configuration.html <br>

**Scan Plagiarisme**          : <br>
   
a. searchenginereport     :    https://drive.google.com/open?id=0B831iVXSuoJccUhTSVRWanZaUzA<br>
        
                       
b. smallseotools	      :   https://drive.google.com/open?id=0B831iVXSuoJceV9yYlUyVGVHd3c<br>

                      
-------

> - Fullname 				 : Nadia Ayu Lestari Arifin
> - Nickname 				 : Nadia
> - NPM		 				 : 1144002
> - Class	 				 : D4 TI 3C
> - Department  		     : Informatics Engineering
> - Collage					 : Politeknik Pos Indonesia


