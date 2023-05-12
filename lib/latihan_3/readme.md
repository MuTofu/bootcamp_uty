## Latihan 3

Pada pelatihan 3 ini akan membahas tentang widget lanjutan dari materi sebelumnya.
Untuk latihan 3 akan membahas tentang row, column, list view, stack, Navigation (In line code)

Jump to

- [Row](https://github.com/dikynugraha1111/bootcamp_uty/tree/master/lib/latihan_3#Row)
- [List View](https://github.com/dikynugraha1111/bootcamp_uty/tree/master/lib/latihan_3#List-View)
- [Stack](https://github.com/dikynugraha1111/bootcamp_uty/tree/master/lib/latihan_3#Stack)
- [Navigation](https://github.com/dikynugraha1111/bootcamp_uty/tree/master/lib/latihan_3#Navigation)

### Row

Widget ini sama hal nya dengan Column, namun jika Column berdirektori horizontal atau atas ke bawah, maka Row berdirektori utama vertikal atau kiri ke kanan.</br>
![row-direction](../../asset/raw/row_direction.png)</br>

### List View

Cara penggunaan ListView ini mirip dengan Column atau Row di mana Anda memasukkan widget yang ingin disusun sebagai children dari ListView.
Hanya saja untuk widget List View sendiri anda bisa melakukan kustomisasi lebih detail dan banyak lagi, seperti menambahkan separator pada setiap item list view, direction dari list view, generate list view dari item, dan masih banyak lagi.
Disini kita akan membahas 2 macam list view, yaitu List View secara secara default (ListView) dan juga List View yang itemnya di generate dari list data tertentu (ListView.builder atau ListView.generate)

### Stack

Stack widget memungkinkan kita untuk menampilkan beberapa lapis widget ke layar. Stack widget juga merupakan multiple children widget yang artinya memiliki properti children sehingga dapat menampung lebih dr satu widget. Urutan dari lapisan widget pada stack dari bawah ke atas, jadi widget yang pertama di dalam stack akan berada di posisi paling bawah dan begitu juga sebaliknya, widget yang terakhir di stack widget akan berada di posisi paling atas stack.</br>
![stack-pict](../../asset/raw/stack_pict.png)</br>

```
        body: Stack(
          children: <Widget>[
            Container(
              color: Colors.green,
            ),
            Container(
              color: Colors.red,
              height: 400.0,
              width: 300.0,
            ),
            Container(
              color: Colors.deepPurple,
              height: 200.0,
              width: 200.0,
            ),
          ],
        ),
```

![stack-sample](../../asset/raw/stack_sample.png)</br>

### Navigation

Widget Navigator bekerja seperti tumpukan layar (stack), ia menggunakan prinsip LIFO (Last-In, First-Out).Ada cukup banyak method yang bisa kita gunakan pada widget navigator salah satunya adalah method Navigator.push(), Navigator.pop(), dan Navigator.pushAndReplacement().

- Navigator.push(), Metode push digunakan untuk menambahkan rute lain ke atas tumpukan screen (stack) saat ini. Halaman baru ditampilkan di atas halaman sebelumnya. Ini seperti kita ingin berpindah dari halaman 1 ke halaman lainnya
- Navigator.pop(), Metode pop menghapus rute paling atas dari tumpukan. Ini menampilkan halaman sebelumnya kepada pengguna. Skenerio simpel nya adalah seperti kita ingin kembali dari halam sekarang ke halaman sebelumnya (Back).
- Navigator.pushAndReplacement(), method ini digunakan untuk menghapus rute saat ini dan diganti dengan rute lain ke atas tumpukan screen (stack). Skenerio simpel nya adalah, ketika kita di halaman 1 dan ingin ke halaman 2, tetapi ketika kita berpindah ke halaman 2, kita juga ingin menghapus/membuang halaman 1.
