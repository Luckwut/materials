---
tags:
  - X
tanggal: 2024-09-24
cssclasses:
  - center-images
---
___
# Library
- Kumpulan kode/fitur yang sudah ditulis oleh orang lain yang kita bisa gunakan.
- Fungsinya untuk menghemat waktu, daripada menulis kode yang panjang untuk menggerakkan servo, menggunakan sensor, dan lain-lain. Kita bisa gunakan kode yang sudah ditulis oleh orang lain.
- **Cara Instalasi Library di Arduino IDE**
	- Buka Arduino IDE
	- Pergi ke **Sketch** → **Include Library** → **Manage Libraries**.
	- Cari/Search library yang ingin di-Install, contohnya 'Servo'.
	- Klik **Install**
- **Cara menggunakan Library**
	- Setelah Instalasi selesai. Cukup tambahkan `#include <NamaLibrary.h>` di kode. Contohnya:
		```c
		#include <Servo.h>
		```
___
# Servo
- Sebuah jenis Motor (bukan kendaraan) yang kita bisa program atau kontrol perputarannya.
- Servo motor biasanya bisa memutar dari 0° hingga 180°. Namun, ada Servo motor yang bisa memutar sampai 360°.
- Digunakan dalam projek seperti robotika, untuk mengatur lengan/persendian robot.
- Modul Servo terdiri dari:
	- Motor DC/Motor Servo
	- Control Circuit
	- Gearbox
- Cara kerja:
	- Servo menggunakan pin [[Pulse Width Modulation (PWM)]]
	- Posisi Servo/Perputaran Servo ditentukan oleh 'lebar' sinyal HIGH dari PWM.
- Contoh Kode:
```c
#include <Servo.h>

Servo myServo;  // Membuat objek/variabel servo

void setup() {
  myServo.attach(9);  // Servo dikoneksikan di pin 9
}

void loop() {
  myServo.write(90);  // Putar servo 90 derajat
  delay(1000);        // Tunggu 1 detik
  myServo.write(0);   // Putar kembali servo ke 0 derajat
  delay(1000);        // Tunggu 1 detik
}
```
- Pin dalam servo:
![[Screenshot 2024-09-30 073825.png]]