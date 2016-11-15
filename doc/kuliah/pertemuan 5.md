<h3 align="center">SISTEM INFORMASI GEOGRAFIS</h3>
<h3 align="center">
"SHAPE-FILE"
</h3>


<p align="center">
  <img src="https://github.com/nadiaaaAR/Geographic-Information-System/blob/master/img/5.png">
</p>


**1. Latar Belakang**

Data terdiri dari pengamatan kita membuat dari melihat dunia nyata. Data spasial terdiri pengamatan dengan lokasi. Data spasial mengidentifikasi fitur dan posisi di permukaan bumi. Data spasial adalah bagaimana kita menempatkan pengamatan kami di peta. Semua perangkat lunak GIS telah dirancang untuk menangani data spasial. Data spasial (juga disebut data geospasial) adalah bagaimana informasi geografis ditangkap dalam GIS.  
Vektor dan data raster dua jenis data utama yang digunakan dalam GIS. Kedua vektor dan data raster memiliki sistem referensi spasial. Ini adalah lintang dan bujur yang menentukan posisi di Bumi. Kita tahu dua model data utama spasial vektor dan raster data. Tapi apa perbedaan antara raster dan vektor data? Kapan sebaiknya Data ditampilkan sebagai raster atau vektor? Mari kita menjelajahi jenis data spasial secara lebih rinci.


**2. Pembahasan**

**Menambahkan data geospasial :**

>>Import Shapefile
>>a = shapefile.writer()
	
**SHP file Geometri**
	
>>a.point(x,y)
>>a.poly([x,y],[x,y])

**DBF file Table**

>>a.field(‘namafolder’,’C’,’4’)
>>a.record(‘BDG’)

**Disimpan dengan Method**

>>a.save(‘file.shp’)

Menambahkan data :

1.	Poin<br>

>>a.poly([a,b], [c,d])

2.	Polygon<br>

>>a.field(‘kota’,’C’,’4’)

**Membuat Attribute :**
	
>>a.field(‘Kota’,’C’,’4’)
>>a.record(‘Bandung’)
	
**Menyimpan Shapefile :**

>>a.save(‘namafile’)

**Parameter Writer :**

-.Shapefile Poin

>>a.point(‘10’,’12’)

-.Shapefile Polygon
>>a.poly(ports = ([3.5], [5,5] , [5,7] ))

-.Shapefile Polyline	
>>a.ports([3.5], [5,5] , [3,5], shapetype.shapefile.polyline)




**3. Penutup**

**Kesimpulan**

Jenis data spasial memberikan informasi bahwa komputer membutuhkan untuk merekonstruksi data spasial dalam bentuk digital. Penambahan data geospasial kita bisa menggunakan attribute yang tersedia dalam parameter writer yang sudah ada yaitu, .shapefile point, .shapefile polygon, .shapefile polyline.

**Saran**

Selanjutnya untuk mendalami materi retrieve data geospasial dengan membaca sumber-sumber yang tersedia di buku maupun internet , dan melakukan praktikum mandiri

-------

**Link Github**               :  https://github.com/nadiaaaAR/Geographic-Information-System<br>

**Referensi**                 : https://doc.arcgis.com/en/arcgis-online/reference/shapefiles.htm<br>

**Scan Plagiarisme**          : <br>
   
a. searchenginereport   :   https://drive.google.com/open?id=0B831iVXSuoJcd3N1eXIzdms4ZzQ <br>
        
b. smallseotools        :   https://drive.google.com/open?id=0B831iVXSuoJcWmE3NTlIVGVwYVE <br>

  
-------

> - Fullname         : Nadia Ayu Lestari Arifin
> - Nickname         : Nadia
> - NPM              : 1144002
> - Class            : D4 TI 3C
> - Department       : Informatics Engineering
> - Collage          : Politeknik Pos Indonesia





