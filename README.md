# Advance Programming C
**Syauqi Armanaya Syaki** </br>
**2206829010** </br>

# Module 5

## Jmeter Report and Test Results

### Endpoint `/all-student`
* Before Optimization (JMeter GUI):
  ![WhatsApp Image 2024-03-12 at 23 19 18_d6f1f5c4](https://github.com/syauqiarman/exercise-profiling/assets/113775175/1f71e14c-2d24-4a42-8465-cecb6c4c9052)
* After Optimization (JMeter GUI):
  ![WhatsApp Image 2024-03-13 at 15 58 54_8782658c](https://github.com/syauqiarman/exercise-profiling/assets/113775175/fbdd7305-dd09-4740-861d-5752b4f5c121)
* Before Optimization (JMeter CLI):
  ![WhatsApp Image 2024-03-13 at 00 04 50_4f726be5](https://github.com/syauqiarman/exercise-profiling/assets/113775175/6bce69c9-62a7-46c7-8299-77ef28e99341)
* After Optimization (JMeter CLI):
  ![WhatsApp Image 2024-03-13 at 16 16 10_359fcca7](https://github.com/syauqiarman/exercise-profiling/assets/113775175/95c60f5d-c17d-45ad-9e33-41f60e93eb27)

### Endpoint `/all-student-name`
* Before Optimization (JMeter GUI):
  ![WhatsApp Image 2024-03-12 at 23 35 48_d1ffc9a8](https://github.com/syauqiarman/exercise-profiling/assets/113775175/d053b9cd-043f-4af9-8520-482d5cfc135c)
* After Optimization (JMeter GUI):
  ![WhatsApp Image 2024-03-13 at 16 01 51_aedb65ba](https://github.com/syauqiarman/exercise-profiling/assets/113775175/52830142-acfa-4eff-ac00-cde1c0ef105b)
* Before Optimization (JMeter CLI):
  ![WhatsApp Image 2024-03-13 at 00 05 28_7883f8f4](https://github.com/syauqiarman/exercise-profiling/assets/113775175/9308b802-87f6-40e4-ba8e-67a5b1fee0f7)
* After Optimization (JMeter CLI):
  ![WhatsApp Image 2024-03-13 at 16 16 57_9d603a4a](https://github.com/syauqiarman/exercise-profiling/assets/113775175/a25eb378-d799-48c4-b64b-0e1c9466e62d)

### Endpoint `/highest-gpa`
* Before Optimization (JMeter GUI):
  ![WhatsApp Image 2024-03-12 at 23 40 46_8959333b](https://github.com/syauqiarman/exercise-profiling/assets/113775175/72bb5def-77b0-49ee-afb7-616aa060b791)
* After Optimization (JMeter GUI):
  ![WhatsApp Image 2024-03-13 at 19 18 43_92292905](https://github.com/syauqiarman/exercise-profiling/assets/113775175/da7d9ee9-3532-408d-8327-947bd9b0e4d6)
* Before Optimization (JMeter CLI):
  ![WhatsApp Image 2024-03-13 at 00 06 00_3ef92a3e](https://github.com/syauqiarman/exercise-profiling/assets/113775175/a527d370-2c96-4ec8-88c3-aa21a05f145f)
* After Optimization (JMeter CLI):
  ![WhatsApp Image 2024-03-13 at 16 17 36_02084998](https://github.com/syauqiarman/exercise-profiling/assets/113775175/97fcedfa-6ef1-434a-a345-a0838ab94b54)

### Kesimpulan
Terjadi peningkatan performa dan waktu eksekusi antara kode-kode awal yang memakan waktu lama dengan kode-kode baru setelah dilakukan pengoptimalan dengan profiling menggunakan Intellij Profiler dan performance testing menggunakan JMeter. Pengoptimalan ini berhasil dan dibuktikan dengan semakin cepatnya waktu eksekusi untuk melakukan respon.

## Reflection
1. JMeter digunakan untuk melakukan pengujian performa kode dengan cara membuat simulasi beban kerja yang tinggi, yakni dengan mengirim request ke endpoint yang ditentukan untuk diuji. Sedangkan, Intellij Profiler digunakan untuk melakukan profiling sebagai cara untuk mengetahui informasi yang lebih rinci mengenai bagian-bagian yang menyebabkan performa menjadi buruk, sehingga akan sangat membantu untuk mengoptimalkan kode.
2. Melalui profiling, bottleneck dan weak points yang menyebabkan performa buruk akan dengan mudah teridentifikasi. Informasi yang dapat didapatkan dapat berupa runtime, memory allocation, CPU usage, garbage collection activity, dan thread concurrency. Dengan informasi ini, saya bisa memfokuskan diri untuk melakukan pengoptimalan terhadap komponen atau kode yang memperlambat performa.
3. Menurut saya, Intellij Profiler efektif untuk melakukan analisis terhadap performa suatu program, khususnya dalam menemukan bottleneck, seperti dalam method `getAllStudentsWithCourse` yang memakan waktu banyak saat dieksekusi. Dengan informasi yang tersedia, saya bisa melakukan optimasi terhadap method yang paling berpengaruh terhadap buruknya performa program, sehingga program akan menjadi lebih optimal lagi.
4. Tantangan besar yang saya hadapi dalam melakukan pengujian performa dan profiling ada saat memahami hasil dari pemeriksaannya yang kompleks, sehingga sulit untuk menentukan mana yang menjadi penghambat utama performa suatu program. Untuk mengatasinya, saya mempelajari lebih dalam mengenai cara memahami hasil analisis yang tersedia dan lebih teliti dalam memaknai hasil tersebut.
5. Menggunakan Intellij Profiler sangat bermanfaat bagi saya, karena dengan Intellij Profiler yang tersedia dalam IDE Intellij IDEA, saya tidak perlu menggunakan third party apps lain untuk melakukan profiling. Selain itu proses profiling disini juga dapat menunjukkan secara langsung masalah atau kode yang menyebabkan buruknya performa, sehingga saya tidak perlu memeriksa dan mengoptimalkan satu-satu secara manual.
6. Sejauh ini, saya belum mengalami hasil yang tidak konsisten antara performance testing dan profiling. namun, jika saya mengalaminya, maka saya akan mencoba untuk mengecek konfigurasi yang ada pada JMeter dan memeriksa kembali hasil profiling Intellij Profiler. Bisa juga dengan menghindari benchmark performance test saat pertama dilakukan, karena bisa saja JVM atau JIT compilernya belum berjalan optimal. Jika masih terdapat kendala, maka bisa mancari permasalahan melalui internet, bertanya kepada teman, kakak asdos, atau dosen.
7. Setelah menganalisis hasil performance testing dan profiling, pertama saya melakukan perbandingan terhadap durasi yang diperlukan oleh program untuk merespon permintaan menggunakan JMeter. Jika terasa lambat, saya akan memanfaatkan profiler untuk mengenali bagian kode yang memperlambat proses sehingga performa menjadi buruk, lalu solusi yang saya lakukan berikutnya adalah dengan refactoring terhadap kode tersebut agar lebih optimal. Berikutnya saya lakukan performance testing dan profiling lagi untuk memeriksa peningkatan yang terjadi. Untuk memastikan bahwa refactoring atau modifikasi yang dilakukan pada kode tetap menghasilkan hasil yang sama dan tidak mengubah fungsionalitas program, saya melakukan pemeriksaan menyeluruh untuk memastikan bahwa outputnya konsisten dengan sebelum perubahan dilakukan. Selain itu, untuk memastikan optimalisasi yang dilakukan tidak mengubah fungsionalitas program, juga bisa dilakukan dengan membuat unit test seperti minggu-minggu sebelumnya.