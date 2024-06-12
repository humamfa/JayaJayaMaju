# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000 dan telah memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. 

### Permasalahan Bisnis

Walaupun telah menjadi menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan. Hal ini berimbas tingginya attrition rate (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%.

### Cakupan Proyek

Membuat business dashboard dan model machine learning berdasarkan dataset karyawan Jaya Jaya Maju.

### Persiapan

Sumber data: Jaya Jaya Maju (https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/main/employee/employee_data.csv)

Setup environment:
```
Username: root@mail.com
Password: root123
```

## Business Dashboard

Business Dashboard terdiri dari 2 jenis grafik.

Grafik pertama menempatkan attrition rate di sumbu y dan kategori karyawan di sumbu x. Contoh:
![image](https://github.com/humamfa/JayaJayaMaju/assets/152384891/ffdc3f85-f48c-4c8d-823c-74b81faae32b)
Grafik di atas menunjukkan karyawan yang tidak melakukan overtime memiliki attrition rate 11%.

Grafik kedua menempatkan attrition di sumbu x dan kategori karyawan di sumbu y. Contoh:
![image](https://github.com/humamfa/JayaJayaMaju/assets/152384891/fab92a03-1634-4618-b017-9309e88f8a38)
Grafik di atas menunjukkan bahwa karyawan yang keluar dari perusahaan (nilai attrition 1) memiliki rata-rata income bulanan sebesar $4.872,4

## Conclusion

- Karyawan yang melakukan overtime memiliki attrition rate hampir 3x (0,32) dibandingkan dengan karyawan yang tidak melakukan overtime (0,11).
- Karyawan yang berada pada jarak umur 18-22 tahun memiliki attrition rate minimal 0,5.

### Rekomendasi Action Items (Optional)

Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.

- Jaya Jaya Maju perlu memperhatikan komitmen overtime karyawan.
- Jaya Jaya Maju perlu memperhatikan umur karyawan, baik karyawan aktif maupun calon karyawan yang akan direkrut ke depannya, terutama karyawan yang berada pada jarak umur 18-22 tahun.
