<h3 align="center">SISTEM INFORMASI GEOGRAFI</h3>
<h3 align="center">
'OVERLAY'
</h3>


<p align="center">
  <img src="https://github.com/nadiaaaAR/Geographic-Information-System/blob/master/img/overlay.jpg">
</p>


**1. Latar Belakang**<br>
Overlay adalah objek di peta yang terikat dengan koordinat garis lintang/garis bujur, sehingga ikut bergerak bila Anda menyeret atau memperbesar/memperkecil tampilan peta. Untuk informasi tentang tipe overlay yang telah didefinisikan, lihat Menggambar pada peta Google Maps JavaScript API menyediakan kelas OverlayView untuk membuat overlay custom Anda sendiri. OverlayView adalah kelas dasar yang menyediakan beberapa metode yang harus Anda implementasikan saat membuat overlay sendiri. Kelas ini juga menyediakan beberapa metode yang memungkinkannya menerjemahkan koordinat layar dan lokasi pada peta. 
OpenLayers membuatnya mudah untuk menempatkan peta dinamis di halaman web. Hal ini dapat menampilkan ubin peta dan spidol diambil dari sumber manapun. OpenLayers telah dikembangkan untuk memajukan penggunaan informasi geografis dari segala jenis. Ini benar-benar gratis, Open Source JavaScript, dirilis di bawah BSD License 2-klausul (juga dikenal sebagai FreeBSD).

**2. Pembahasan**<br>

**a.	Pengertian Overlay**
<p>Overlay adalah objek di peta yang terikat dengan koordinat garis lintang/garis bujur, sehingga ikut bergerak bila Anda menyeret atau memperbesar/memperkecil tampilan peta. Overlay merupakan proses penempatan grafis suatu peta diatas grafis peta lainnya agar menghasilkan gabungan kedua peta yang memiliki informasi atribut dari kedua peta tersebut. Teknik overlay dalam sistem informasi geografis ada 2 yaitu gabungan (union) dan irisan (intersect). Untuk informasi tentang tipe overlay yang telah didefinisikan, lihat Menggambar pada peta Google Maps JavaScript API menyediakan kelas OverlayView untuk membuat overlay custom Anda sendiri</p><br>

**b.	Pengertian Marker**
<p>Marker atau penanda genetic merupakan penciri individu yang dilihat oleh mata atau terdeteksi dengan alat tertentu yang menunjukkan genotype suatu individu. Di dalam sebuah peta atau maps, marker adalah suatu tanda yang menjelaskan atau memberitahukan suatu tempat atau wilayah agar user mengetahui lokasi yang dimaksud</p><br>

**c.	Pengertian OpenLayers**
<p>Open Layer adalah library javascript murni untuk menampilkan data peta di berbagai browser, tanpa server side dependencies. Open Layer mengimplementasikan javascript API untuk membangun rich web-based geographic application yang mirip dengan Google Maps dan MSN Virtual Earth APIS</p><br>

**d.	Menambahkan overlay**
Inilah langkah yang diperlukan untuk membuat overlay :<br>

<p>1.	Atur prototype objek overlay custom Anda ke instance baru google.maps.OverlayView(). Akibatnya, ini akan menjadi subkelas dari kelas overlay.</p>
<p>2.	Buat konstruktor untuk overlay custom Anda, dan atur parameter inisialisasi.</p>
<p>3.	Implementasikan metode onAdd() dalam prototipe Anda, dan lekatkan overlay ke peta. OverlayView.onAdd() akan dipanggil bila peta siap untuk overlay yang akan dilekatkan.</p>
<p>4.	Implementasikan metode draw() dalam prototipe Anda, dan tangani tampilan visual objek Anda. OverlayView.draw() akan dipanggil bila objek pertama kali ditampilkan.</p>
<p>5.	Anda juga harus mengimplementasikan metode onRemove() untuk membersihkan setiap elemen yang Anda tambahkan dalam overlay.</p>


**e.	Memulai Overlay**
<p>Bila overlay telah dibuat untuk pertama kali dan siap ditampilkan, kita perlu melekatkannya ke peta melalui DOM browser. API menunjukkan bahwa overlay telah ditambahkan ke peta dengan memanggil metode onAdd()overlay. Untuk menangani metode ini, kita buat <//div//> **(tanpa //)** untuk menyimpan gambar, tambahkan sebuah elemen <//img//> **(tanpa //) **, lekatkan ke <//div//>, kemudian lekatkan overlay ke salah satu panel peta. Panel adalah simpul dalam struktur hierarki DOM.</p>
Panel, tipe MapPanes, menetapkan urutan tumpukan untuk layer berbeda pada peta. Panel berikut tersedia, dan disebutkan sesuai urutan tumpukannya dari bawah ke atas:<p>
<p>1.	mapPane adalah panel terendah dan berada di atas petak. Ini mungkin tidak menerima kejadian DOM. (Panel 0).</p>
<p>2.	overlayLayer berisi polyline, poligon, overlay bumi dan overlay layer petak. Ini mungkin tidak menerima kejadian DOM. (Panel 1).</p>
<p>3.	overlayShadow berisi bayangan marker. Ini mungkin tidak menerima kejadian DOM. (Panel 2).</p>
<p>4.	overlayImage berisi gambar latar depan marker. (Panel 3).</p>
<p>5.	floatShadow berisi bayangan jendela informasi. Panel ini berada di atas overlayImage, sehingga marker bisa berada dalam bayangan jendela informasi. (Panel 4).</p>
<p>6.	overlayMouseTarget berisi elemen yang menerima kejadian mouse DOM, seperti target transparan untuk marker. Panel ini berada di atas floatShadow, sehingga marker yang berada dalam bayangan jendela informasi bisa diklik. (Panel 5).</p>
<p>7.	floatPane berisi jendela informasi. Panel ini berada di atas semua overlay peta. (Panel 6).</p></p>


<div class="content">
<!DOCTYPE html>
<html>
  <head>
    <title>Overlay</title>
    <link rel="stylesheet" href="https://openlayers.org/en/v3.20.1/css/ol.css" type="text/css">
    he line below is only needed for old environments like Internet Explorer and Android 4.x 
    <script src="https://cdn.polyfill.io/v2/polyfill.min.js?features=requestAnimationFrame,Element.prototype.classList,URL"></script>
    <script src="https://openlayers.org/en/v3.20.1/build/ol.js"></script>
    <script src="https://code.jquery.com/jquery-2.2.3.min.js"></script>
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css">
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js"></script>
    <style>
      #marker {
        width: 30px;
        height: 30px;
        border: 7px solid #088;
        border-radius: 60px;
        background-color: #0000CD;
        opacity: 3.0;

      }
      #bandung {
        text-decoration: none;
        color: #FF0000;
        font-size: 11pt;
        font-weight: bold;
      }
      #marker1 {
        width: 30px;
        height: 30px;
        border: 7px solid #088;
        border-radius: 60px;
        background-color: #0000CD;
        opacity: 3.0;
      }
      #bulukumba {
        text-decoration: none;
        color: #FF0000;
        font-size: 11pt;
        font-weight: bold;
      }

.popover-content {
        min-width: 180px;
      }
    </style>
  </head>
  <body>
    <div id="map" class="map"></div>
    <div style="display: none;">
      Clickable label for Vienna 
      <a class="overlay" id="bandung" target="_blank" href="https://id.wikipedia.org/wiki/Kota_Bandung">Bandung</a>
      <div id="marker" title="Marker"></div>
      Clickable label for Vienna 
      <a class="overlay" id”bulukumba" target="_blank" href="https://id.wikipedia.org/wiki/bulukumba">Bulukumba</a>
      <div id="marker1" title="Marker"></div>
      Popup 
      <div id="popup" title="Welcome to My Maps"></div>
    </div>
    <script>

      var map = new ol.Map({
        layers: [
          new ol.layer.Tile({
            source: new ol.source.XYZ({
              url: 'https://map.vas.web.id/wmts/agm/webmercator/{z}/{x}/{y}.png'
            })
          })
        ],
        target: 'map',
        view: new ol.View({
          center: ol.proj.transform([118.015776, -2.6000285], 'EPSG:4326', 'EPSG:3857'),
          zoom: 5
        })
      });

      var pos = ol.proj.fromLonLat([107.609810,-6.914744]);

      // Vienna marker
      var marker = new ol.Overlay({
        position: pos,
        positioning: 'center-center',
        element: document.getElementById('marker'),
        stopEvent: false
      });
      map.addOverlay(marker);

// Vienna label
      var bandung = new ol.Overlay({
        position: pos,
        element: document.getElementById('bandung')
      });
      map.addOverlay(bandung);

      var pos1 = ol.proj.fromLonLat([105.3794937,-6.4457721]);

      // Vienna marker
      var marker1 = new ol.Overlay({
        position: pos1,
        positioning: 'center-center',
        element: document.getElementById('marker1'),
        stopEvent: false
      });
      map.addOverlay(marker1);

      // Vienna label
      var bulukumba = new ol.Overlay({
        position: pos1,
        element: document.getElementById('bulukumba')
      });
      map.addOverlay(bulukumba);

      // Popup showing the position the user clicked
      var popup = new ol.Overlay({
        element: document.getElementById('popup')
      });
      map.addOverlay(popup);

      map.on('click', function(evt) {
        var element = popup.getElement();
        var coordinate = evt.coordinate;
        var hdms = ol.coordinate.toStringHDMS(ol.proj.transform(
            coordinate, 'EPSG:3857', 'EPSG:4326'));

        $(element).popover('destroy');
        popup.setPosition(coordinate);
        // the keys are quoted to prevent renaming in ADVANCED mode.
        $(element).popover({
          'placement': 'top',
          'animation': false,
          'html': true,
          'content': '<p>The location you clicked was:</p><code>' + hdms + '</code>'
        });
        $(element).popover('show');
      });
    </script>
  </body>
</html> 
</div>


<br><br>
**Hasil Praktikum :**

<p align="center">
  <img src="https://github.com/nadiaaaAR/Geographic-Information-System/blob/master/img/map.PNG">
</p>

**3. Penutup**

**a. Kesimpulan**
Overlay merupakan proses penempatan grafis suatu peta diatas grafis peta lainnya agar menghasilkan gabungan kedua peta yang memiliki informasi atribut dari kedua peta tersebut. Teknik overlay dalam sistem informasi geografis ada 2 yaitu gabungan (union) dan irisan (intersect).


**a. Kesimpulan**
Selanjutnya untuk mendalami materi Overlay  dengan membaca sumber-sumber yang tersedia di buku maupun internet , dan melakukan praktikum mandiri.

**Link Github** 	            :  https://github.com/nadiaaaAR/Geographic-Information-System<br>

**Referensi**	                :  http://openlayers.org/two/<br>

**Scan Plagiarisme**          : <br>
   
a. searchenginereport     :   https://drive.google.com/open?id=0B831iVXSuoJcd2NlUEtiMWdYTlk <br>
        
                       
b. smallseotools	      :   https://drive.google.com/open?id=0B831iVXSuoJcTlVKa1ZWTkRTU2s<br>

                      

> - Fullname 				 : Nadia Ayu Lestari Arifin
> - Nickname 				 : Nadia
> - NPM		 				 : 1144002
> - Class	 				 : D4 TI 3C
> - Department  		     : Informatics Engineering
> - Collage					 : Politeknik Pos Indonesia


