## 2.1 Original code of broadcast chat

![Simulation running one server and three clients](image.png)

**Server**
Server dijalankan dan mendengarkan koneksi di port 2000, lalu server menerima tiga koneksi baru dari alamat lokal dengan port yang berbeda. Server menampilkan message yang dikirim oleh client secara real-time.

**Client**
Client dijalankan dan terhubung dengan server dan menerima welcome message. Message yang dikirim baik dari client1, client2, maupun client3 akan diterima dari masing-masing client juga.

## 2.2 Modifying the websocker port

Ya, di file `server.rs` juga menggunakan websocket protocol. Websocket protocol didefinisikan di dalam `tokio::spawn`, tepatnya di `let (_req, ws_stream) = ServerBuilder::new().accept(socket).await?;`. Baris tersebut adalah proses websocket handshake. Handshake itu sendiri adalah proses negosiasi di antara dua device atau sistem yang akan menerapkan aturan dalam berkomunikasi dan memvalidasi sinyal untuk memastikan jalur komunikasi aman dan kedua device tersebut dalam kondisi siap. Fungsi dari websocket handshake  adalah mengubah/ menerapkan koneksi jaringan biasa (TCP) menjadi koneksi dua arah yang interaktif (websocket).