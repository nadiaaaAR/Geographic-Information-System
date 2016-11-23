<h3 align="center">SISTEM INFORMASI GEOGRAFIS</h3>
<h3 align="center">
"WRITE, EDIT, READ dan DELETE Data Geospasial - Pertemuan 6 GISE"
</h3>


<p align="center">
  <img src="https://github.com/nadiaaaAR/Geographic-Information-System/blob/master/img/enam.jpg">
</p>


**1. Latar Belakang**

Data terdiri dari pengamatan kita membuat dari melihat dunia nyata. Data spasial terdiri pengamatan dengan lokasi. Data spasial mengidentifikasi fitur dan posisi di permukaan bumi. Data spasial adalah bagaimana kita menempatkan pengamatan kami di peta. Semua perangkat lunak GIS telah dirancang untuk menangani data spasial. Data spasial (juga disebut data geospasial) adalah bagaimana informasi geografis ditangkap dalam GIS.  
Vektor dan data raster dua jenis data utama yang digunakan dalam GIS. Kedua vektor dan data raster memiliki sistem referensi spasial. Ini adalah lintang dan bujur yang menentukan posisi di Bumi. Kita tahu dua model data utama spasial vektor dan raster data. Tapi apa perbedaan antara raster dan vektor data? Kapan sebaiknya Data ditampilkan sebagai raster atau vektor? Mari kita menjelajahi jenis data spasial secara lebih rinci.


**2. Pembahasan**


**Write Point**

w = shapeType
w.field (‘Kota’,’C’,’30’)
w.field (‘Jakarta’,’Rima’)
w.record (‘Jakarta’,’Rima’)
w.point (10,10,0,0)
w.save(‘kota.shp’)
exit()


**Edit Point**

e = shapefile.Editor(shapefile= ”shapefiles/test/point.shp”)
e.point(0,0,10,2)
e.record(“Appended”,”Point”)
e.save(‘shapefiles/test/point’)

**Read Point**

sf = shape
f.records()
sf.record(0)
sf.record(1)
sf.shapes()[0].point


**Delete Record**
e.delete(1)

----------------------------------------------------------
     Python
  Import shapefile
  Sf = shapefile.writer(shapeType=1)
  Sf = field(‘NAMA’,’C’,’40’)
  Sf = field(‘PEMILIK’,’C’,’’40’)
  Sf = record(‘Warung Nasi’,’Asep Dinamo’)
  Sf = point(10.10)
  Sf.save(‘warteg.shp’)
  Exit().

Script Edit:
  Python
  Import shapefile
  Sf = sahefile.Editor(‘war.shp’)
  Sf = point(16,10,0,0)
  Sf = record(‘Padang’)
  Sf = save()
  Sf = save(‘war.shp’)
  A= shapefile.Reader(‘war,shp’)
  A = records()
  A.shapes().Points
  A.shapes()[0]
  A.shapes()[0] Points
[[10.0,10,0]]

     
Script Delete:
  Sf.Delete(0)
  A.shapes()[0].Points
[[10,0,10,0]]
  Sf = Point(16,10,0,0)
  Sf = record(‘Padang’)
  Sf = save(‘war.shp’)

Vektor data tidak terdiri dari grid piksel. Sebaliknya, grafik vektor terdiri dari simpul dan jalur. Tiga jenis simbol dasar untuk data vektor adalah titik, garis dan poligon (area). Sejak waktu subuh, peta telah menggunakan simbol untuk mewakili fitur dunia nyata. Dalam terminologi GIS, fitur dunia nyata disebut entitas spasial.



**3. Penutup**

**Kesimpulan**

Jenis data spasial memberikan informasi bahwa komputer membutuhkan untuk merekonstruksi data spasial dalam bentuk digital. Penambahan data geospasial kita bisa menggunakan attribute yang tersedia dalam parameter writer yang sudah ada yaitu, .shapefile point, .shapefile polygon, .shapefile polyline.

**Saran**

Selanjutnya untuk mendalami materi retrieve data geospasial dengan membaca sumber-sumber yang tersedia di buku maupun internet , dan melakukan praktikum mandiri

-------

**Link Github**               :  https://github.com/nadiaaaAR/Geographic-Information-System<br>

**Referensi**                 : https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm<br>

**Scan Plagiarisme**          : <br>
   
a. searchenginereport   :   https://drive.google.com/open?id=0B831iVXSuoJcRVA0SjBOQ0VWakE<br>
        
b. smallseotools        :   https://drive.google.com/open?id=0B831iVXSuoJcNkRCVDJlZzVtNzQ <br>

   
-------

> - Fullname         : Nadia Ayu Lestari Arifin
> - Nickname         : Nadia
> - NPM              : 1144002
> - Class            : D4 TI 3C
> - Department       : Informatics Engineering
> - Collage          : Politeknik Pos Indonesia





