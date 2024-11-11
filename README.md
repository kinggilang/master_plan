-------------------------------
Nama: Gilang Bagus Tri Pambudi
-
Nim: 362358302148
-
Kelas: 2A TRPL
-
-------------------------------
PRAKTIKUM STATE 1
-
-------------------------------
1. Penjelasan Langkah 4 pada Praktikum
Pada langkah ini, file data_layer.dart dibuat untuk menggabungkan ekspor dari model plan.dart dan task.dart. Tujuan dari langkah ini adalah untuk mempermudah dan merapikan proses impor, karena hanya dengan mengimpor satu file data_layer.dart, semua model yang dibutuhkan dapat diakses. Pendekatan ini membuat kode lebih efisien, mudah dipelihara, dan lebih mudah dibaca.

2. Alasan Penggunaan Variabel dan Konstanta Plan pada Langkah 6
Pada langkah 6, variabel plan diperlukan untuk menyimpan data rencana yang mencakup daftar tugas dalam aplikasi. Variabel ini digunakan untuk memanipulasi dan memperbarui informasi rencana, seperti menambahkan tugas baru atau mengubah status tugas. Dibuat sebagai konstanta karena pada saat pembuatan objek Plan, nilai-nilai default seperti nama dan daftar tugas ditetapkan melalui konstruktor. Penggunaan konstanta memastikan bahwa nilai awal objek tidak dapat diubah setelah objek dibuat, yang membantu menjaga integritas data dan mencegah perubahan yang tidak diinginkan

Hasil
-
![Screenshot 2024-11-11 100635](https://github.com/user-attachments/assets/78383d95-99a0-40e7-b229-a80901c4a0d5)
-
3. Kegunaan Metode pada Langkah 11 dan 13 dalam Siklus Hidup State
- Pada Langkah 11 dan Langkah 13, dua metode penting dalam siklus hidup StatefulWidget digunakan, yaitu initState() dan dispose().
-initState() (Langkah 11): Metode ini dipanggil satu kali ketika State pertama kali dibuat. Di sini, kita menginisialisasi variabel seperti scrollController dan menambahkan listener untuk menangani peristiwa scroll. initState() memastikan bahwa pengaturan awal untuk scrollController dilakukan sebelum widget ditampilkan.
-dispose() (Langkah 13): Metode ini dipanggil ketika State widget tidak lagi digunakan, biasanya saat widget dihapus dari widget tree. Di sini, kita membersihkan scrollController dengan memanggil dispose() untuk mencegah kebocoran memori dan melepaskan sumber daya yang digunakan oleh controller.
-------------------------------
PRAKTIKUM STATE 2
-------------------------------
- Pada langkah 1, InheritedWidget adalah widget yang memungkinkan data diteruskan ke widget anak tanpa perlu meneruskannya secara manual. InheritedNotifier adalah subclass dari InheritedWidget yang lebih spesifik digunakan untuk menangani perubahan data, dengan menghubungkan ValueNotifier untuk mengelola state yang berubah. Ini memungkinkan widget yang bergantung padanya untuk memperbarui UI secara otomatis saat data berubah, sehingga pengelolaan state menjadi lebih efisien dan mudah.

- Tujuan dari metode di langkah 3 adalah untuk mempermudah perhitungan dan penampilan status progres dari tugas yang ada pada Plan. Dengan menambahkan dua metode ini, kita dapat dengan mudah menampilkan jumlah tugas yang selesai dan progres keseluruhan tanpa harus menghitungnya berulang-ulang di tempat lain dalam kode. Hal ini membuat logika aplikasi menjadi lebih terstruktur dan efisien.

![Screenshot 2024-11-11 104155](https://github.com/user-attachments/assets/83947b1f-907b-4804-8d4e-5439503f1ffa)


-------------------------------
PRAKTIKUM STATE 3
-------------------------------

Diagram tersebut menggambarkan alur navigasi dan struktur widget dalam aplikasi Flutter.

![ss 1](https://github.com/user-attachments/assets/b5a48ee4-c3be-45b3-b6d0-1bf94b7c9d52)

- Diagram Kiri
1. MaterialApp: Merupakan root widget dari aplikasi Flutter.
2. PlanProvider: Widget yang menyediakan data atau state yang diperlukan oleh widget di bawahnya.
3. PlanCreatorScreen: Layar yang digunakan untuk membuat sebuah rencana.
4. Column: Widget yang mengatur tata letak widget anaknya dalam bentuk kolom vertikal.
5. TextField: Widget untuk input teks.
6. Expanded: Widget yang memperluas widget anaknya untuk mengisi ruang yang tersedia.
7. ListView: Widget untuk menampilkan daftar item dalam bentuk scrollable.

- Diagram Kanan
1. MaterialApp: Tetap sebagai root widget dari aplikasi.
2. PlanScreen: Layar baru yang muncul setelah navigasi dilakukan.
3. Scaffold: Widget yang menyediakan struktur dasar visual untuk material design.
4. Column: Sama seperti sebelumnya, mengatur tata letak widget anaknya dalam bentuk kolom vertikal.
5. Expanded: Tetap digunakan untuk memperluas widget anaknya.
6. SafeArea: Widget yang memastikan bahwa widget anaknya tidak terpotong oleh area yang tidak aman (seperti notch atau status bar).
7. ListView: Tetap digunakan untuk menampilkan daftar item.
8. Text: Widget untuk menampilkan teks.

