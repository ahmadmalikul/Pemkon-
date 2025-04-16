# Pemkon-
# Sistem Safety Pengereman Motor

Proyek ini merupakan implementasi sistem ** safety pengereman untuk sepeda motor** berbasis mikrokontroler STM32. Sistem ini dirancang untuk meningkatkan keselamatan pengendara dengan mendeteksi objek di depan secara otomatis menggunakan sensor, dan mengaktifkan rem menggunakan solenoid actuator.

---

## Komponen Utama

- **STM32F446RE** – Mikrokontroler sebagai pusat kontrol dan pemrosesan logika.
- **Sensor Ultrasonik (HC-SR04)** – Mengukur jarak objek di depan kendaraan.
- **Sensor Infrared** – Mendeteksi objek pada jarak sangat dekat untuk verifikasi tambahan.
- **Solenoid Linear Actuator** – Menarik tuas rem saat kondisi bahaya terdeteksi.
- **MOSFET Driver** – Mengendalikan arus besar untuk aktuator tanpa menggunakan relay.
- **Power Supply** – Mengalirkan daya ke sistem (12V untuk solenoid, 3.3V/5V untuk mikrokontroler).

---

## ⚙️ Cara Kerja Sistem

1. **Sensor ultrasonik** memantau jarak kendaraan dengan objek di depan.
2. **Sensor infrared** memastikan ada objek secara fisik dalam zona aman.
3. **STM32F446RE** memproses data dari kedua sensor secara real-time.
4. Jika kondisi kritis terpenuhi (jarak terlalu dekat & objek terdeteksi), sistem:
   - Mengaktifkan **MOSFET** untuk mengalirkan daya ke **solenoid**.
   - **Solenoid** menarik tuas rem secara otomatis.
5. Sistem akan menonaktifkan solenoid jika kondisi kembali aman.

---
