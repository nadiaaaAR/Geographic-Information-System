<h3 align="center">SISTEM INFORMASI GEOGRAFIS</h3>
<h3 align="center">
"RETRIVE DATA GEOSPASIAL"
</h3>


<p align="center">
  <img src="https://github.com/nadiaaaAR/Geographic-Information-System/blob/master/img/consult_3.jpg">
</p>


**1. Latar Belakang**

Data terdiri dari pengamatan kita membuat dari melihat dunia nyata. Data spasial terdiri pengamatan dengan lokasi. Data spasial mengidentifikasi fitur dan posisi di permukaan bumi. Data spasial adalah bagaimana kita menempatkan pengamatan kami di peta. Semua perangkat lunak GIS telah dirancang untuk menangani data spasial. Data spasial (juga disebut data geospasial) adalah bagaimana informasi geografis ditangkap dalam GIS.  



**2. Pembahasan**

**a. Pengertian *

Retrive Data Geospasial adalah salah satu cara untuk mengambil data geometri dan Database data geospasial, dimana data tersebut merupakan data vector yang merupakan salah satu jenis dari data geospasial, karena data vector merupakan data yang  berbentuk shape, jadi data tersebut dapat digunakan untuk retrieve di python, shapefile atau SHP sendiri merupakan data yang menyimpan data geometri didalamnya, yaitu :<br>
1.  Bbox : koordinat batas view di peta, biasanya berbentuk persegi panjang di peta, bbox merupak boundary box yaitu koordinat titik 4.<br>
2.  Shape Type<br>
- Point      : koordinat titik (1 titik/koordinat) bernomer standar 1 dari ESRI<br> 
- PolyLine : koordinat titik-titik yang membentuk garis tapi tidak membentuk area bernomer standar 3 dari ESRI.<br>
- Polygon   : koordinat membentuk area bernomer standar 5 dari ESRI.<br>



**b. Operasi Pengambilan data dengan Python **

Membaca Jumlah data Geometri :<br>
**>> import shapefile** <br>
**>>sf = shapefile.Reader(“namafile.shp”<br>
**>>sf.shapes()**<br>
**>>a = sf.shapes()**<br>
**>>len(a)**<br>

Membaca Jumlah data Geometri :<br>
**>> import shapefile**<br>
**>>sf.records()**<br>
**>>sf.records(n)**<br>


**3. Penutup**

**Kesimpulan**

Retrive Data Geospasial adalah salah satu cara untuk mengambil data geometri dan Database data geospasial, dimana data tersebut merupakan data vector yang merupakan salah satu jenis dari data geospasial.

**Saran**

Selanjutnya untuk mendalami materi retrieve data geospasial dengan membaca sumber-sumber yang tersedia di buku maupun internet , dan melakukan praktikum mandiri

-------

**Link Github**               :  https://github.com/nadiaaaAR/Geographic-Information-System<br>

**Referensi**                 :  http://researchguides.library.yorku.ca/content.php?pid=245987&sid=2176375<br>

**Scan Plagiarisme**          : <br>
   
a. searchenginereport   :   https://drive.google.com/open?id=0B831iVXSuoJceF9ERU5OdFZCR0U <br>
        
b. smallseotools        :   https://drive.google.com/open?id=0B831iVXSuoJcUFpDWTF6WEFSQnM <br>

  
-------

> - Fullname         : Nadia Ayu Lestari Arifin
> - Nickname         : Nadia
> - NPM              : 1144002
> - Class            : D4 TI 3C
> - Department       : Informatics Engineering
> - Collage          : Politeknik Pos Indonesia





