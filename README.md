Nama  :Reza Kurniawan

Kelas TI.22.A1

nim   : 312210436

*Exception Handling*

    ◉ Exception (eksepsi) merupakan suatu kesalahan (error) yang terjadi saat proses eksekusi program sedang berjalan, kesalahan ini akan menyebabkan program berakhir dengan tidak normal.
    
*Handling*

    ◉ Penanganan file adalah bagian penting dari aplikasi apa pun.
*Assertion*

    ◉ Assertion(pernyataan) adalah kewajaran program yang kamu bisa aktif/nonaktifkan ketika kamu selesai menjalankan program.

*The Assert Statement*

    ◉ Saat menemukan pernyataan, Python mengevaluasi ekspresi yang menyertainya, yang mana semoga benar. Jika ekspresi salah, Python memunculkan pengecualian AssertionError.

Sintaks untuk pernyataan yaitu :

assert Expression[, Arguments]

Jika pernyataan gagal, Python menggunakan ArgumentExpression ArgumentExpression sebagai argumen argumen untuk AssertionError AssertionError. Pengecualian AssertionError Pengecualian AssertionError dapat ditangkap dan ditangani ditangani seperti pengecualian lainnya menggunakan try- kecuali pernyataan, tetapi jika dibiarkan, mereka akan menghentikan program dan menghasilkan backtrace.

Contoh
    
    ◉ Berikut adalah fungsi fungsi yang mengubah suhu dari derajat Kelvin menjadi derajat Fahrenheit.Karena nol derajat Kelvin dingin, fungsi fungsi menyimpannya jika melihat negatif negatif suhu.
    ◉ Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:
    
![Screenshot_20221220_234735](https://user-images.githubusercontent.com/115677959/208728799-74737582-87f3-4c23-bd54-2420b1bfc317.png)

*Menangani Pengecualian*

Jika Anda memiliki beberapa kode mencurigakan yang mungkin mengeluarkan pengecualian, Anda dapat mempertahankan program Anda letakkan kode yang mencurigakan di *try: blok. Setelah coba: blok, sertakan pernyataan sertakan *except: statemen, diikuti oleh blok kode yang menangani masalah seanggun mungkin.

Contoh

    ◉ Contoh-contoh ini membuka file, menulis konten file, dan keluar dengan aman karena ada tidak masalah

    ◉ Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:
    
![Screenshot_20221220_235256](https://user-images.githubusercontent.com/115677959/208729217-9766d8a4-8344-430c-a228-55f040729509.png)
    
    ◉ Contoh ini mencoba membuka file yang Anda tidak memiliki izin menulis, sehingga membuat file pengecualian

    ◉ Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:

![Screenshot_20221220_235521](https://user-images.githubusercontent.com/115677959/208730171-de53297d-38bf-480b-9c07-e68a770f2def.png)

*Fasal kecuali tanpa Pengecualian*

    ◉ Anda juga dapat menggunakan pernyataan exception tanpa exception yang didefinisikan sebagai berikut:
try: You do your operations here; ...................... except: If there is any exception, then execute this block. ...................... else: If there is no exception then execute this block.

Pernyataan coba-kecuali jenis ini menangkap semua pengecualian pengecualian yang terjadi. Menggunakan percobaan seperti try-expect pernyataan tidak dianggap sebagai praktik pemrograman yang baik, karena mereka menangkap semuanya pengecualian tetapi tidak membuat programmer mengidentifikasi kemungkinan penyebab masalah terjadi

*Klausa kecuali dengan Berbagai Pengecualian*

    ◉Anda juga dapat menggunakan pernyataan exception yang sama untuk menangani beberapa exception sebagai berikut:
try: You do your operations here; ...................... except(Exception1[, Exception2[,...ExceptionN]]]): If there is any exception from the given exception list, then execute this block. ...................... else: If there is no exception then execute this block.

*Klausa coba-akhirnya*

Contoh

    ◉ Jika Anda tidak memiliki izin untuk membuka file dalam mode tulis yang dapat ditulis, maka ini akan menghasilkan hasil berikut:
    
![Screenshot_20221220_235809](https://user-images.githubusercontent.com/115677959/208730901-15755bdf-9404-4794-a60b-89b8cdf33584.png)

    ◉ Contoh yang sama dapat ditulis lebih bersih sebagai berikut:
    
![Screenshot_20221221_000125](https://user-images.githubusercontent.com/115677959/208731113-f17a2181-50be-45ce-b911-8cee2fb388b3.png)

Ketika exception dilempar ke dalam blok try, eksekusi segera dilanjutkan ke akhir memblok. Setelah semua pernyataan di blok akhirnya dieksekusi, pengecualian dimunculkan lagi dan ditangani dalam pernyataan kecuali jika ada di lapisan berikutnya yang lebih tinggi dari percobaan-kecuali penyataan.

*Argumen Pengecualian*

Contoh

    ◉ Berikut adalah contoh untuk satu pengecualian
    ◉ Ketika kode di bawah dijalankan, menghasilkan hasil sebagai berikut:!
    
![Screenshot_20221221_000843](https://user-images.githubusercontent.com/115677959/208731542-8745c6cf-a7ad-441d-bad6-2c0fa97a1a19.png)
   
*Melempar Pengecualian*

Contoh

    ◉ Pengecualian dapat berupa string, kelas, atau objek. Sebagian besar pengecualian adalah pengecualian dari inti Python menimbulkan adalah kelas, dengan argumen=argumen yang merupakan turunan dari kelas. Mendefinisikan pengecualian barucukup mudah dan dapat dilakukan sebagai berikut:
    
![Screenshot_20221221_001244](https://user-images.githubusercontent.com/115677959/208732011-039e86a3-9c90-42e6-8a4c-e4e0ee056ea7.png)

*Pengecualian yang Ditetapkan Pengguna*
    
    ◉ Python juga memungkinkan Anda membuat pengecualian sendiri dengan menurunkan kelas-kelas dari yang standar pengecualian bawaan.
    ◉ Berikut adalah contoh-contoh yang terkait dengan RuntimeError. Di sini, kelas dibuat yang merupakan subkelas dari subkelas RuntimeError. Ini berguna saat Anda perlumenampilkan tampilan informasi yang lebih spesifik saat e pengecualian tertangkap.
    ◉ Di blok coba, pengecualian yang ditentukan pengguna dimunculkan dan ditangkap di blok kecuali. Itu variabel e digunakan untuk membuat instance dari kelas Networkerror.

![Screenshot_20221221_001620](https://user-images.githubusercontent.com/115677959/208732337-342a9f12-df09-405d-9e3f-eac50864fb37.png)
