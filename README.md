# Modul 5 : Real-Time Operating System (RTOS)

## 🎯 Tujuan Praktikum
Berikut adalah tujuan dari praktikum pada Modul 5:
1.	Praktikan mampu memahami prinsip kerja dari RTOS
2.	Praktikan mampu membuat produk sederhana dengan memanfaatkan Operating system

## 📄 Dasar Teori
Real- Time Operating System (biasa di sebut RTOS) adalah sebuah Operating System (OS) yang digunakan untuk memenuhi kebutuhan aplikasi secara Real Time pada Embedded Device yang memproses data secara langsung tanpa ada nya penundaan (Buffer). Real Time karena system ini hamper bekerja setiap saat dimana ia dibutuhkan saat itu juga. Salah satu kelebihan Operating System RTOS adalah kemampuan nya untuk melakukan kerja secara konsisten baik secara waktu yang ia butuhkan maupun secara task aplikasi yang mampu ia kerjakan.

Gambar berikut menunjukkan perbedaan antara non-RTOS dengan RTOS

<img width="1200" height="675" alt="nonrtosvsrtos" src="https://github.com/user-attachments/assets/91be9fab-73d2-4213-8d61-c3cd939dd357" />
<br>
RTOS sendiri terdiri dari 2 jenis yaitu, sistem soft RTOS dan sistem hard RTOS. Soft RTOS bisa dideskripsikan sebagai sistem yang hampir selalu menyelesaikan task dengan waktu yang telah ditentukan. Pada soft RTOS kemungkinan penyelesaian task melewati batas waktu pelaksanaan task masih bisa terjadi. Dan pada sistem soft RTOS, apabila terjadi kegagalan mencapai deadline dalam waktu yang telah ditentukan maka sistem akan mengalami efek yang tidak begitu berbahaya bagi sistem. Contohnya seperti penurunan performa sistem. Sedangkan hard RTOS merupakan system yang dipastikan selalu menyelesaikan task dalam waktu yang telah ditentukan. Dikatakan pasti selalu menyelesaikan task karena hard RTOS selalu menyelesaikan task sebelum deadline dan apabila terjadi kegagalan menyelesaikan task maka sistem akan mengalami efek berbahaya yang dapat merusak sistem secara keseluruhan.

Terdapat beberapa jenis RTOS, seperti SafeRTOS dan FreeRTOS. Jenis Operating System RTOS yang paling sering digunakan adalah FreeRTOS, karena jenis RTOS yang bersifat Open Source, gratis dan mudah digunakan.
Berikut adalah aktivitas yang dapat dilakukan dalam pengenalan Real-Time Operating System menggunakan library yang ada di Arduino yaitu FreeRTOS.

Berikut adalah percobaan awal yang dapat dilakukan dalam pengenalan Real-Time Operating System menggunakan library yang ada di Arduino yaitu FreeRTOS.

```cpp
#include <Arduino_FreeRTOS.h>

void setup() {
  // put your setup code here, to run once:

  Serial.begin(9600);
  xTaskCreate(One, "one", 128, NULL, 1, NULL);
  xTaskCreate(Two, "two", 128, NULL, 1, NULL);
}

void loop() {
  // put your main code here, to run repeatedly:

}

void One(void *pvParameters) {
  while(1) {
    Serial.println("One");
    delay(2000);
  }
}
void Two(void *pvParameters) {
  while(1) {
    Serial.println("Two");
    delay(1000);
  }
}
```

## 🚀 Tugas Pendahuluan

- Membuat semua program (source code) yang diperlukan untuk masing-masing percobaan (sertakan keterangan-keterangan penting pada source code menggunakan komentar); Jelaskan masing-masing baris atau bagian kode tersebut.
- Menyiapkan rangkaian hardware untuk percobaan (sudah dirangkai, sehingga saat percobaan langsung menjalankan program yang telah dibuat). Sertakan pada tugas pendahuluan dalam bentuk foto yang juga menampilkan wajah Anda. (Dilakukan untuk masing-masing percobaan; Sebelum praktikum, cukup siapkan untuk percobaan pertama saja jika space pada breadboard terbatas)

## ⚙️ Alat dan Bahan

Dalam percobaan sederhana ini, berikut alat dan bahan yang digunakan:

<div align="center">
<table border="1" cellpadding="10" cellspacing="0" width="100%">
  <tr>
    <th>Arduino</th>
    <th>Potensiometer</th>
    <th>Motor Servo</th>
    <th>LED</th>
  </tr>

  <tr align="center">
    <td>
      <img width="192" height="136,1" alt="arduino_uno" src="https://github.com/user-attachments/assets/3e61e208-bb23-42aa-bbef-0ac539279ce0" /><br>
    </td>
    <td>
      <img width="179,5" height="175,75" alt="image" src="https://github.com/user-attachments/assets/f44c78e5-fd37-47e0-a2f4-0a5af2b6c86a" />
    </td>
    <td>
      <img width="318" height="260" alt="image" src="https://github.com/user-attachments/assets/e54280b7-5fd3-4ce7-b4f8-41163ed3bed3" /><br>
    </td>
    <td>
      <img width="54" height="134" alt="RedLED_Fritzing" src="https://github.com/user-attachments/assets/80556570-c129-43fa-904b-39eac5677a2d" />
    </td>
  </tr>

  <tr align="center">
    <td>Arduino Uno, Leonardo, atau lainnya</td>
    <td>Potensiometer</td>
    <td>Motor Servo</td>
    <td>LED Merah</td>
  </tr>
</table>
</div>

## 💻 Percobaan

## 📚 Pertanyaan Praktikum

## 🧰 Mengakhiri Percobaan

Berikut hal yang perlu dilakukan setelah selesai praktikum:
- Sebelum keluar dari ruang praktikum, pastikan meja dalam keadaan rapi.
- Jangan lupa untuk mendokumentasikan dalam bentuk foto dan video serta diunggah lewat google drive dan sertakan tautan dokumentasi tersebut di Buku Catatan Praktikum.
- Pastikan asisten telah menandatangani catatan percobaan kali ini pada Buku Catatan Praktikum Anda. Catatan percobaan yang tidak ditandatangani oleh asisten tidak akan dinilai.
- Kumpulkan kode program tugas tambahan pada setiap percobaan dalam repository github dengan format name repository “Kelas(value)_Modul(value)_Nama_NIM”


<h2></h2>

<br>

![banner](https://github.com/user-attachments/assets/f1f03032-41c0-4121-94e3-df1d513b42e5)
