# kitabisa-loadtesting
1.	Pastikan laptop/computer terinstall java jdk https://www.oracle.com/java/technologies/downloads/
2.	Lalu pastinya perlu Jmeter (Open Source) https://jmeter.apache.org/ 
3.	Jika sudah extract jmeter lalu kita buka aplikasinya yaitu melalui Jmeter folder -> bin -> klik ApacheJmeter.jar 
4.	Jika sudah terbuka seperti ini selanjutnya, open file **kitabisa.jmx** atau buat test script seperti dibawah : 
5.	Klik kanan dibagian testplan lalu pilih add -> Thread(user) -> Thread Group, nah didalam thread group ini terdapat beberapa settingan kaya Number of thread itu berapa itu yang akan akses lalu duration itu berapa lama itu satuannya detik yaa, jadi disini kita setting berapa user yang akan akses dan berapa lama mengaksesnya untuk same user on each teration itu seperti apakah user tersebut aksesnya barengan atau ga gt 
 
6.	Setelah kita beramsumsi user yang akan mengaksesnya selanjutnya klik kanan di thread group -> add -> sampler -> http request, nah untuk http request mirip seperti postman jika sudah ada terbiasa menggunakan postman, jadi untuk test rest api dari sisi backend gt, kitab isa menambahkan method request nya seperti get atau post, lalu bisa juga menambahkan url endpointnya, jika menggunakan method post biasanya kita kan perlu body request atau param ya? Nah disini jg bisa menambahkan. Nah jika perlu header untuk request nya kitab isa juga menambahkan klik kanan di http request -> add -> config element -> http header manager, nah untuk pengisian di http request ini disayangkan gw belum bisa ngasih contoh menggunakan method post dikarenakan perlu url endpoint yang valid, kecuali dipinjemin endpoint staging sama marketplace tersebut hehehe,
Atau next gw bakal searching lagi endpoint yang bisa digunakan sebagai contoh ya, sekalian mau bahas terkait Security Testing, dikarenakan gw masih ngeliat beberapa aplikasi endpoint nya masih telanjang haha bisa diliat dari inspect element di web nya atau debugging lewat mobile apps nya.

 
 
7.	Setelah kita selesai setting http request nya atau body request nya, selanjutnya kita perlu listener atau seperti penampung response request nya, nah disini ada beberapa pilihan listener nya, disesuaikan masing2 kebutuhan aja yaa, tp gw sih biasanya pake view result tree atau summary report aja, 
 
 

8.	Nah yang terakhir kita tinggal running deh, request nya, klik segitiga hijau buat running request, nanti tinggal liat report nya di listner dari request yang kita setting di http request dan setting user di thread group, nah ini adalah hasil dari 1000 user barengan akses ke page yang sama menyebabkan error
 
 

9.	Generate html, 
Caranya klik tools -> generate html report, lalu tampil beberapa settingan, result file = itu adalah listener yang kita save di field filename di listener –> view result tree jangan lupa di save ya, user.properties file = user. Properties dari folder jmeter -> bin dan out put directory itu adalah folder penampung untuk report nya pastikan foldernya baru dan kosong ya dan tinggal generate lalu tampil deh html report nya dari folder setelah generate report.
 
 
 
 
