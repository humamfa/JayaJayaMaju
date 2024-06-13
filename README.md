# Proyek Pertama: Menyelesaikan Permasalahan Perusahaan Jaya Jaya Maju

## Business Understanding

Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000 dan telah memiliki lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. 

### Permasalahan Bisnis

Walaupun telah menjadi menjadi perusahaan yang cukup besar, Jaya Jaya Maju masih cukup kesulitan dalam mengelola karyawan. Hal ini berimbas tingginya _attrition rate_ (rasio jumlah karyawan yang keluar dengan total karyawan keseluruhan) hingga lebih dari 10%. Mengidentifikasi penyebab karyawan melakukan atrisi perlu dilakukan secepat mungkin. _Attrition rate_ yang tinggi dapat menciptakan lingkungan kerja yang tidak stabil dan mengganggu _working culture_ di perusahaan.

### Cakupan Proyek

- Mengidentifikasi penyebab tingginya attrition rate di perusahaan Jaya Jaya Maju.
- Membuat business dashboard.
- Membuat model machine learning berdasarkan dataset karyawan Jaya Jaya Maju untuk memprediksi kemungkinan karyawan melakukan attrition.

### Persiapan

Sumber data: Jaya Jaya Maju (https://github.com/dicodingacademy/dicoding_dataset/blob/main/employee/employee_data.csv)

Setup environment Dashboard:

```
docker pull metabase/metabase:v0.46.4
docker run -p 3000:3000 --name metabase metabase/metabase
```

Login Metabase:
```
Username: root@mail.com
Password: root123
```

Setup environment Python - Anaconda:
```
conda create --name decision-tree python=3.9
conda activate decision-tree
pip install -r requirements.txt
```

Setup environment Python - Terminal:
```
mkdir decision_tree
cd decision_tree
pipenv install
pipenv shell
pip install -r requirements.txt
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
- Karekteristik umum karyawan yang melakukan attrition adalah melakukan overtime, berusia 18-22 tahun, monthly income di bawah $2056, 

### Rekomendasi Action Items (Optional)

Berikan beberapa rekomendasi action items yang harus dilakukan perusahaan guna menyelesaikan permasalahan atau mencapai target mereka.

- Jaya Jaya Maju perlu memperhatikan komitmen overtime karyawan. Perusahaan perlu menghindari terjadinya overtime, mengingat standard hour yang ditetapkan perusahaan adalah 80 jam. Apabila diperlukan, total jam overtime sebaiknya dibatasi 3 jam dalam satu hari dan 14 belas jam dalam satu minggu (merujuk UU 13/2003 pasal 78).
- Jaya Jaya Maju perlu memperhatikan umur karyawan, baik karyawan aktif maupun calon karyawan yang akan direkrut ke depannya, terutama karyawan yang berada pada jarak umur 18-22 tahun. Perusahaan perlu mengutamakan untuk merekrut karyawan di usia 23 tahun ke atas untuk mengurangi kemungkinan karyawan melakukan attrition.

## Model Machine Learning

Prediksi attrition karyawan dapat dilakukan dengan menggunakan script Python (Jaya_Jaya_Maju.py). Untuk memasukkan data karyawan:
```
print(model.predict([[...]]))
```
Data karyawan dapat diisi pada bagian kosong dengan format berikut:
```
['Age', 'DailyRate', 'DistanceFromHome', 'Education', 'EnvironmentSatisfaction', 'HourlyRate', 'JobInvolvement', 'JobLevel', 'JobSatisfaction', 'MonthlyIncome', 'MonthlyRate', 'NumCompaniesWorked', 'PercentSalaryHike', 'PerformanceRating', 'RelationshipSatisfaction', 'StockOptionLevel', 'TotalWorkingYears', 'TrainingTimesLastYear', 'WorkLifeBalance', 'YearsAtCompany', 'YearsInCurrentRole', 'YearsSinceLastPromotion', 'YearsWithCurrManager', 'BusinessTravel_num', 'Department_num', 'EducationField_num', 'Gender_num', 'JobRole_num', 'MaritalStatus_num', 'OverTime_num']
```
Contoh:

```
print(model.predict([[19,111,1000,2,4,555,1,4,4,1000,1111,6,55,4,3,2,11,6,3,4,3,1,2,1,1,3,0,1,1,0]]))
### Output: [0]
```

Run script Python:
```
python jaya_jaya_maju.py
```

Nilai output yang dihasilkan adalah 0 (karyawan diprediksi tidak keluar dari perusahaan) atau 1 (karyawan diprediksi keluar dari perusahaan).
