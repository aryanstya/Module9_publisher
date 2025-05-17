**a. How much data your publisher program will send to the message broker in one run?**

Pada satu kali eksekusi, program publisher akan mengirimkan sejumlah data sesuai dengan jumlah pesan dan ukuran masing-masing pesan yang telah ditentukan dalam program. Misalnya, jika program dikonfigurasi untuk mengirim 100 pesan masing-masing sebesar 1KB, maka total data yang dikirim adalah sekitar 100KB. Jumlah ini dapat bervariasi tergantung pada konfigurasi program dan isi pesannya.

**b. The URL of: amqp://guest:guest@localhost:5672 is the same as in the subscriber program, what does it mean?**


Penggunaan URL amqp://guest:guest@localhost:5672 baik di program publisher maupun subscriber berarti keduanya terkoneksi ke message broker yang sama. Rinciannya sebagai berikut:
guest (pertama): Username untuk autentikasi.
guest (kedua): Password untuk pengguna tersebut.
localhost: Menunjukkan bahwa broker berjalan di mesin lokal.
5672: Port default untuk protokol AMQP.

URL yang digunakan pada kedua program, baik publisher maupun subscriber, menunjukkan bahwa keduanya terhubung ke instance RabbitMQ yang sama sebagai message broker. Bagian pertama guest adalah nama pengguna (username), sedangkan guest kedua adalah kata sandinya (password) yang digunakan untuk proses autentikasi. localhost menunjukkan bahwa koneksi dilakukan ke broker yang berjalan di mesin lokal, dan 5672 adalah port standar yang digunakan oleh RabbitMQ untuk koneksi AMQP. Dengan konfigurasi ini, publisher dan subscriber dipastikan saling berkomunikasi melalui broker yang sama.

- Running RabbitMQ as message broker
![Screenshot 2025-05-17 185219](https://github.com/user-attachments/assets/26734b53-e47c-4a27-9aaf-a468fc96eab2)
