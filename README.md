## Understanding how it works

![Result of the execution](image.png)

Ini terjadi karena spawner menyimpan task tersebut dan hanya akan di eksekusi ketika command `execute.run()` dijalankan. Sehingga karena `println!("Hannan's Komputer: hey hey");` dijalankan sebelum `execute.run()`, maka pada console muncul `Hannan's Komputer: hey hey` terlebih dahulu sebelum task yang di spawn dengan spawner.