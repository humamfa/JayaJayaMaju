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

## Model Machine Learning

Prediksi attrition karyawan dapat dilakukan dengan menggunakan script Python (Jaya_Jaya_Maju.py). Untuk memasukkan data karyawan, gunakan baris paling bawah:
```
print(clf.predict([[...]]))
```
Data karyawan dapat diisi pada bagian kosong dengan format berikut:
```
['Age', 'DailyRate', 'DistanceFromHome', 'Education', 'EnvironmentSatisfaction', 'HourlyRate', 'JobInvolvement', 'JobLevel', 'JobSatisfaction', 'MonthlyIncome', 'MonthlyRate', 'NumCompaniesWorked', 'PercentSalaryHike', 'PerformanceRating', 'RelationshipSatisfaction', 'StockOptionLevel', 'TotalWorkingYears', 'TrainingTimesLastYear', 'WorkLifeBalance', 'YearsAtCompany', 'YearsInCurrentRole', 'YearsSinceLastPromotion', 'YearsWithCurrManager', 'BusinessTravel_num', 'Department_num', 'EducationField_num', 'Gender_num', 'JobRole_num', 'MaritalStatus_num', 'OverTime_num']
```
Contoh:

![image](https://github.com/humamfa/JayaJayaMaju/assets/152384891/c5e7ec91-9609-459e-9b83-dfa9512d0307)

Nilai output yang dihasilkan adalah 0 (karyawan diprediksi tidak keluar dari perusahaan) dan 1 (karyawan diprediksi keluar dari perusahaan.
