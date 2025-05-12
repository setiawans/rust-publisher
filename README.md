# Reflection
Steven Setiawan - 2306152260

> How much data your publisher program will send to the message broker in one run?

Program publisher akan mengirimkan data sebanyak 5 kali ke _message broker_ dalam sekali eksekusi, karena di dalam kode publisher, terdapat `publish_event` yang dijalankan sebanyak 5 kali.

> The url of: "**amqp://guest:guest@localhost:5672**" is the same as in the subscriber program, what does it mean?

URL **amqp://guest:guest@localhost:5672** yang sama pada program publisher dan subscriber menunjukkan bahwa kedua program tersebut menggunakan server RabbitMQ yang sama sebagai perantara komunikasi, di mana publisher mengirimkan pesan ke _queue_ dan subscriber mendengarkan/mengambil pesan dari _queue_ yang sama.

## Running RabbitMQ as Message Broker

![/running-RabbitMQ](./images/running-RabbitMQ.jpg)

## Sending and Processing Event

![/run-publisher](./images/run-publisher.jpg)

![/run-subscriber](./images/run-subscriber.jpg)

Kedua gambar tersebut menunjukkan proses komunikasi dengan memanfaatkan RabbitMQ, di mana gambar pertama memperlihatkan eksekusi program publisher yang mengirimkan 5 data pengguna ke _message broker_ dalam satu kali eksekusi, sementara gambar kedua menampilkan program subscriber yang berhasil menerima data-data tersebut dan memprosesnya dengan menampilkan informasi pengguna di _console_.