1. How much data your publisher program will send to the message broker in one
   run? bisa kita lihat pada implementasi di main.rs terlihat 5 message yang akan dikirim ketika message broker berjalan atau dijalakan. lima data ini masing masing berupa user id dan username
2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
   program, what does it mean? sebetulnya ini pertanyaan yang sangat trivia. ya karena kita ingin membuka sebuah jalan komunikasi atua bisa dibilang juga dengan protokol. sebetulnya cara berpikirnya katakan kita tiadak tahu alamatnya akan diset dimana, nah saat di subscriber barulah kita menyamaakan dengan alamat yang kita set secara random di publisher. hanya saja karena meneur tutorial kita mengerjkaannya secara terbalik, maksudnya mengerjakan subscirber dulu baru publisher, maka kita samakan saja alamat di publisher kita, yang amana kita bermaksud agar publisher dan subsciber sama sama lempar lempaaran data di jalan yang sama.

![image](https://github.com/user-attachments/assets/c077376c-b8b3-47b8-935a-56588960be88)

![image](https://github.com/user-attachments/assets/adbfa7e7-191f-4431-b6dc-0d37626f7029)

![image](https://github.com/user-attachments/assets/6d4e4bfa-fdf8-4587-a619-ac290f5791d3)

![image](https://github.com/user-attachments/assets/2490e783-072d-49af-bede-0c58bfe155f8)


Pada grafik pemantauan RabbitMQ, terlihat ada dua lonjakan berwarna ungu dan tidak ada lonjakan berwarna kuning. Lonjakan ungu menunjukkan bahwa ada dua pesan yang berhasil dikirim ke konsumen dan sudah diterima (acknowledged). Artinya, subscriber sudah menerima dan memproses dua pesan tersebut.

Sementara itu, tidak adanya lonjakan kuning berarti kemungkinan besar tidak ada pesan baru yang dikirim ke antrean (queue) selama waktu yang ditampilkan di grafik, atau jumlahnya sangat sedikit sehingga tidak terlihat.
