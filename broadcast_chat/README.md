## 2.1 Original code of broadcast chat

![Simulation running one server and three clients](image.png)

**Server**
Server dijalankan dan mendengarkan koneksi di port 2000, lalu server menerima tiga koneksi baru dari alamat lokal dengan port yang berbeda. Server menampilkan message yang dikirim oleh client secara real-time.

**Client**
Client dijalankan dan terhubung dengan server dan menerima welcome message. Message yang dikirim baik dari client1, client2, maupun client3 akan diterima dari masing-masing client juga.

