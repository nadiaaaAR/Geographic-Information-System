<h3 align="center">SISTEM INFORMASI GEOGRAFI</h3>
<h3 align="center">
“Web Service Geospasal & Open Geospatial Consortium"
</h3>


<p align="center">
  <img src="https://github.com/nadiaaaAR/Geographic-Information-System/blob/master/img/ogc.png">
</p>


**1. Latar Belakang**
 The Open Geospatial Consortium, Inc (OGC) adalah sebuah konsorsium industri internasional dari 368 perusahaan, instansi pemerintah dan universitas yang berpartisipasi dalam proses konsensus untuk mengembangkan spesifikasi antarmuka yang tersedia untuk umum. OpenGIS® Spesifikasi mendukung solusi interoperable yang" geo-aktifkan "Web, nirkabel dan layanan berbasis lokasi, dan arus utama IT. spesifikasi memberdayakan pengembang teknologi untuk membuat informasi dan layanan spasial yang kompleks dapat diakses dan berguna dengan semua jenis aplikasi.
Open source adalah konsep perangkat lunak yang memungkinkan kode sumber terbuka dan bebas untuk mendistribusikan dan memodifikasi. MAGIC menggunakan database PostgreSQL dan PostGIS lapisan spasial dalam alat pemetaan online dan menciptakan data geospasial yang memenuhi OGC standards.Data dibuat dalam MAGIC dapat diakses di Open Source GIS software.Other open source aplikasi GIS termasuk plugin GDAL raster, Quantum GIS, Rumput dan banyak lainnya.
Dengan mengembangkan layanan pemetaan web dan layanan file web menggunakan standar OGC pengguna akan dapat mengambil data online MAGIC dan digunakan dalam dalam berbagai aplikasi GIS. Misalnya, pengguna akan dapat melihat 1934 foto udara dari providedthrough MAGIC ini layanan pemetaan web dalam program seperti Google Earth, ArcMap atau di Quantum GIS.

**2. Pembahasan**

Web Service geospasial (GWS) membantu pengguna menemukan, akses, dan kadang-kadang memanipulasi data yang menarik di web dinamis dari jaringan terdistribusi. GWS dirancang untuk mengumpulkan data sekali dan memperbarui atau mengeditnya secara real time. Banyak pengguna GIS tidak mengikuti pengembangan alat dan standar yang memfasilitasi penciptaan dinamis GWS untuk mengakses data geospasial dan produk. Namun non-ahli sudah penggelaran GWS dibangun untuk SUN (Fischer 2009). Artikel ini berusaha untuk menjelaskan secara singkat layanan web pilih geospasial dan untuk memperkenalkan pembaca untuk pilihan demonstrasi dan alat-alat yang memungkinkan GWS interoperabilitas. Ini menggambarkan alat dan sumber daya yang berguna bagi mereka yang ingin membangun layanan geospasial mereka sendiri. Implementasi GWS, baik untuk geovisualizations, analisis spasial, ponsel, atau opsi geogrid, yang ditingkatkan oleh kolaborasi dengan konsorsium regional dan global (misalnya, Konsorsium Geospasial Terbuka (OGC), Open Source Geospatial Foundation (OSGeo), Open Grid Forum (OGF )), lembaga nasional, dan industri. OGC bekerja sama dengan spektrum yang luas dari pengguna. Banyak alat yang digunakan untuk menyediakan fungsionalitas GWS digambarkan sebagai adalah geoportals bahwa infrastruktur layanan data spasial (SDI) inisiatif, dan masyarakat ilmu ilmiah dan sosial.<br>

**a.	Geospasial Web Services Menurut Jenis**
untuk referensi dan implementasi sesuai standar OGC. implementasi referensi yang berfungsi penuh, dan orang-orang terhadap yang lain dievaluasi. Implementasi compliant standar berkaitan dengan perangkat lunak server-side, dan dianggap berfungsi penuh sebagai diuji. pelaksanaannya dapat dipertimbangkan, tetapi tidak dijamin, untuk beroperasi dengan produk standar OGC dilaksanakan dengan baik lainnya.<br>


**1.	WEB MAP SERVICE (WMS)**
WMS menyediakan pengguna dengan sarana untuk melayani peta georeferensi tersedia dari server GIS melalui web. Server menggunakan implementasi WMS 1,0 menghasilkan peta, menjawab pertanyaan dasar, dan berkomunikasi fungsi mereka ke program lain melalui GetMap, GetFeatureInfo dan GetCapabilities interface. Melalui antarmuka GetFeatureInfo, pengguna dapat mengambil atribut Info yang berkaitan dengan fitur dipetakan. WMS diimplementasikan di lebih dari 280 produk. Jika pengguna meminta peta dengan kotak yang sama melompat-lompat, sistem referensi spasial, dan ukuran output, mereka dapat menghasilkan peta komposit dibangun dari sumber yang terletak di jaringan WMS didistribusikan. Di mana pengamatan bumi diminta, model metadata WMS diperlukan. Ketika permintaan peta besar atau sering terbuat dari server, peta caching mungkin lambat. Untuk mengatasi masalah kinerja, gambar pra-diberikan, atau ubin, dapat digunakan (seperti pada Google Maps) untuk mempercepat pengambilan permintaan WMS yang berkaitan dengan observasi Bumi.
Ada dua implementasi referensi dari WMS, versi 1.1.1, implementasi referensi resmi, dan 1.3, pelaksanaan kandidat. Sebuah implementasi referensi, sesuai dengan spesifikasi OGC, adalah salah satu yang pengembang lain mengevaluasi implementasi mereka. Setidaknya lima puluh produk yang sesuai dengan WMS 1.1.1 dan sembilan belas dengan WMS v. 1.3.0.<br>

**2.	Web Coverage Service (WCS)**
WCS, raster standar pelayanan OGC ini, mengambil "coverage" atau informasi geospasial yang berkaitan dengan fenomena multidimensi pada titik-titik dalam ruang yang berbeda-beda di wilayah geografis. Setiap WCS menyediakan akses ke informasi "cakupan grid" sederhana atau melalui tiga operasi: GetCapabilities, DescribeCoverage, dan GetCoverage. Informasi (tersedia data dan metadata), meskipun tidak ditampilkan oleh WCS, dapat digambarkan oleh WMS, digunakan dalam multi-nilai pertanggungan, atau digunakan dalam model ilmiah. fungsinya memfasilitasi subsetting, scaling, proyeksi ulang, dan encoding format grid data. Ketika permintaan operasi yang dibuat menggunakan XML mereka mungkin dikemas dalam amplop SOAP. The diantisipasi WCS 2.0 akan bergantung pada model cakupan GML. WCS ekstensi termasuk WCPS (dijelaskan di bawah) dan WCS-T. WCS-T adalah operasi layanan transaksional yang dapat menambah, mengubah, atau menghapus coverage jaringan dari server WCS sambil memberikan metadata cakupan diperbarui (http://www.opengeospatial.org/standards/wcs).<br>


**3.	Web Coverage Processing Service (WCPS)**
WCPS adalah perpanjangan dari WCS v. 1.1.2 dan didasarkan pada WCPS bahasa standar antarmuka (http://www.opengeospatial.org/standards/wcps).The permintaan izin pengolahan bahasa protokol-independen "coverage" atau informasi geospasial digital multi-dimensi yang bervariasi secara spasial dan / atau temporal. Hal ini memungkinkan, ekstraksi, pengolahan, dan fungsi analisis yang berkaitan dengan sensor, gambar dan data statistik yang diwakili oleh pertanggungan. Hal ini diduga menjembatani WCS dan WPS. Sejak WCS terbatas coverage segiempat, data multi-dimensi tersedia di titik-titik grid. Interpolasi dapat memberikan data antara titik-titik grid. Petascope (http://www.petascope.org) adalah implementasi referensi dari WCPS.<br>

**4.	Web Features Services (WFS)**
The WFS antarmuka memungkinkan pengguna untuk mengakses dan memanipulasi informasi fitur geospasial dari sumber jaringan terdistribusi. operasi dasar termasuk GetCapabilities, DescribeFeatureType dan operasi GetFeature. operasi yang lebih kompleks yang tersedia melalui antarmuka layanan WFS-T dijelaskan di bawah.
Intergraph: GeoMedia
http://www.intergraph.com/sgi/products/productFamily.aspx?family=10&country
Intergraph adalah GIS dan rekayasa perangkat lunak terkemuka. GeoMedia WebMap profesional 5.01 memberikan OGC Server compliant WFS v. 1.0.0. dan mengimplementasikan WFS-T 1.0.0. GeoMedia ini 6.1.5 "SDI Pro" versi mendukung Layanan Gazetteer, sebuah WFS transaksional, dan WFS aman (Sonea 2008). GeoMedia membaca banyak format data tanpa terjemahan, dan WFS yang mampu menangkap fitur yang diubah melalui clien tipis.<br>


**5.	Web Features Service Transcational (WFS-T)**
Interface WFS-T mengizinkan pengguna untuk membuat (insert), menghapus, memperbarui dan mengunci contoh fitur, dan mengambil atau fitur query. Interface yang ditulis dalam XML, sementara GML digunakan untuk menggambarkan fitur dalam antarmuka. Sehingga transaksi dapat disimpan dengan benar dalam datastore (misalnya, SQL RDBMS), semantik transaksi diterapkan.<br>


**6.	Web Processing Service (WPS)**
WPS tampaknya menawarkan pengguna kemampuan terbatas untuk membangun dan memfasilitasi penerbitan alat geoprocessing untuk vektor dan raster data. Implementasi dapat dianggap middleware. Berikut proses-proses berhubungan dengan perhitungan, algoritma atau model yang melibatkan data georeferensi. Dalam penerbitan, mengikat informasi dan metadata yang dibuat tersedia untuk memfasilitasi penemuan dan akses. Untuk interoperabilitas, standar untuk profil aplikasi untuk setiap proses yang ditawarkan. Pengguna menemukan layanan WPS mungkin input data dan melaksanakan proses tanpa mengetahui tentang profil antarmuka atau aplikasi. WPS memberikan untuk kedua platform netral dan platform-spesifik spesifikasi. WPS menggunakan DescribeProcess dan Jalankan operasi untuk encoding permintaan dan tanggapan, embedding data dan metadata, referensi input dan output, dan meminta penyimpanan output. Pembangunan alur kerja berulang mungkin dengan WPS melalui orkestrasi rantai layanan, menyebut urutan layanan web, atau melalui rantai layanan yang sederhana. Apalagi WPS kompatibel dengan WSDL dan SOAP, dan dapat menambahkan sertifikat keamanan. Keuntungan lebih dari spesifikasi WSDL / SOAP saat ini termasuk kemampuannya untuk menentukan penyimpanan output, fasilitasi pelayanan chaining, dan fleksibilitas untuk digunakan oleh SISA atau SOAP arsitektur.<br>


**7.	Open GIS Location Service (OpenLS)**
OpenLS merupakan standar antarmuka yang terdiri dari satu set layanan dasar dan lebih kompleks. Layanan inti antara lain layanan direktori, layanan gateway, layanan lokasi utilitas (untuk geocode dan membalikkan geokode,), layanan presentasi, dan layanan rute. Layanan direktori membantu pelanggan mengakses tempat terdekat atau khusus. Layanan gerbang mengambil lokasi dari terminal mobile (perangkat). Lebih layanan yang kompleks antara lain layanan navigasi dan layanan pelacakan. Layanan navigasi adalah layanan rute ditingkatkan dan jaringan dapat diakses. Layanan pelacakan melacak sekelompok objek yang bergerak.<br>

**3. Penutup**

**a. Kesimpulan**

Web Service geospasial (GWS) membantu pengguna menemukan, akses, dan kadang-kadang memanipulasi data yang menarik di web dinamis dari jaringan terdistribusi. GWS dirancang untuk mengumpulkan data sekali dan memperbarui atau mengeditnya secara real time.

*b. Saran**

Selanjutnya untuk mendalami materi Web Service Geospasal & Open Geospatial Consortium dengan membaca sumber-sumber yang tersedia di buku maupun internet, dan melakukan praktikum mandiri.

-------

**Link Github** 	            :  https://github.com/nadiaaaAR/Geographic-Information-System<br>

**Referensi**	                :  http://magic.lib.uconn.edu/help/help_OGC.html<br>

**Scan Plagiarisme**          : <br>
   
a. searchenginereport     :   https://drive.google.com/open?id=0B831iVXSuoJcd2NlUEtiMWdYTlk <br>
        
                       
b. smallseotools	      :   https://drive.google.com/open?id=0B831iVXSuoJcTlVKa1ZWTkRTU2s<br>

                      
-------

> - Fullname 				 : Nadia Ayu Lestari Arifin
> - Nickname 				 : Nadia
> - NPM		 				 : 1144002
> - Class	 				 : D4 TI 3C
> - Department  		     : Informatics Engineering
> - Collage					 : Politeknik Pos Indonesia


