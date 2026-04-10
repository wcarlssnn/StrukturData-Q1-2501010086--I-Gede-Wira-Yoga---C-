📘 Quiz Struktur Data – Q1

👤 Identitas
	•	Nama: (Isi Nama Anda)
	•	NIM: (Isi NIM Anda)
	•	Kelas: (Isi Kelas Anda)

⸻

1. Karakteristik Memori dan Akses Data

Pada struktur array, elemen-elemen disimpan secara berurutan dalam memori (kontigu). Hal ini memungkinkan sistem untuk menghitung alamat suatu elemen secara langsung menggunakan indeks. Oleh karena itu, proses akses data dapat dilakukan dengan sangat cepat, yaitu dalam kompleksitas waktu O(1).

Berbeda dengan itu, pada singly linked list, elemen tidak disimpan secara bersebelahan di memori. Setiap node hanya memiliki referensi ke node berikutnya. Untuk mengakses elemen tertentu, perlu dilakukan penelusuran dari awal hingga mencapai posisi yang diinginkan. Inilah yang menyebabkan waktu akses menjadi O(n).

⸻

2. Analisis Efisiensi Operasi Manipulasi

Struktur linked list lebih efektif digunakan ketika sering terjadi operasi penyisipan dan penghapusan data, terutama di bagian tengah.

Pada array, proses insert atau delete mengharuskan pergeseran elemen lainnya agar tetap berurutan, sehingga membutuhkan waktu O(n).

Sebaliknya, pada linked list, proses tersebut cukup dengan mengubah pointer antar node tanpa perlu menggeser data. Jika posisi node sudah diketahui, maka operasi ini dapat dilakukan dalam waktu O(1).

Dengan demikian, linked list lebih cocok untuk kondisi di mana manipulasi data lebih dominan dibandingkan akses acak.

⸻

3. Konsep Doubly Linked List

Pada doubly linked list, setiap node memiliki tiga komponen utama:
	•	Data
	•	Pointer ke node berikutnya (next)
	•	Pointer ke node sebelumnya (prev)

Keberadaan pointer tambahan memungkinkan traversal dilakukan ke dua arah, yaitu maju dan mundur. Hal ini memberikan fleksibilitas lebih dalam pengolahan data, seperti mempermudah penghapusan node tertentu.

Namun, konsekuensinya adalah penggunaan memori menjadi lebih besar dibandingkan singly linked list, serta pengelolaannya sedikit lebih kompleks.

⸻

4. Mekanisme Circular Linked List

Circular linked list merupakan variasi dari linked list di mana node terakhir tidak menunjuk ke nilai null, melainkan kembali ke node pertama sehingga membentuk sebuah siklus.

Perbedaan utama dengan linked list biasa adalah tidak adanya akhir yang jelas dalam struktur ini. Traversal dapat dimulai dari node mana saja dan akan terus berputar.

Contoh penerapan dari struktur ini adalah pada sistem round robin scheduling, di mana setiap proses dieksekusi secara bergiliran dalam siklus berulang.

⸻

5. Array Dinamis di Python

Dalam Python, tipe data list sebenarnya diimplementasikan sebagai dynamic array.

Ketika kapasitas array sudah penuh dan dilakukan operasi append, Python akan:
	1.	Mengalokasikan memori baru dengan kapasitas lebih besar
	2.	Menyalin seluruh elemen dari array lama ke array baru
	3.	Menambahkan elemen baru ke dalamnya

Walaupun proses penyalinan ini membutuhkan waktu O(n), hal tersebut tidak terjadi setiap saat. Oleh karena itu, secara rata-rata (amortized), operasi append tetap dianggap memiliki kompleksitas O(1).
