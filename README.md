
# UAS II3160 - Mengembangkan Layanan Microservice (Tugas 3)
## Mealy: Diet Meal Planner
Microservice ini dikembangkan dalam rangka memenuhi UAS II3160 Teknologi Sistem Terintegrasi, lebih tepatnya Tugas 3 - Integrasi Layanan 
Nama Pembuat Layanan Integrasi: Favian Rafi Laftiyanto / 18223036
Nama Rekan Sekelompok yang Dimanfaatkan API-nya: Ahmad Evander Ruizhi Xavier / 18223064

### A. Deskripsi
Mealy adalah aplikasi Diet Meal Planner yang dirancang untuk membantu pengguna menentukan pilihan makanan sehat berdasarkan profil kesehatan personal. Aplikasi ini menghitung kebutuhan nutrisi harian (BMR, BMI, dan Calorie Needs) serta memberikan rekomendasi makanan yang telah difilter sesuai dengan batasan medis tertentu. Layanan dapat diakses pada: https://19623238-favian.github.io/mealy/ 

Layanan ini dikembangkan dengan memanfaatkan 2 buah API yang telah dibuat pada Tugas sebelumnya (Tugas 2). Berikut adalah API yang dimanfaatkan pada layanan ini:
- [API Healthy Grocery]https://github.com/19623238-Favian/API-Healthy-Grocery : https://api.cirro.my.id/api/recommendation/food
  - Digunakan untuk menentukan BMI, BMR, dan kebutuhan nutrisi pengguna
- [API Nutrient]https://github.com/evanderruizhi2/nutrition-serviceAPI.git : https://evanrzh.theokaitou.my.id/api/nutrition/constraints
  - Digunakan untuk menentukan rekomendasi makanan sehat bagi pengguna dan juga untuk mencari kandungan nutrisi suatu makanan

### B. Fitur Utama
- **Personalized Health Calculator**: Menghitung BMI (Body Mass Index) dan BMR (Basal Metabolic Rate) secara otomatis berdasarkan usia, berat badan, tinggi badan, dan tingkat aktivitas.
- **Medical Condition Filtering**: Memberikan batasan nutrisi khusus (seperti batas gula, natrium, atau lemak) bagi pengguna dengan kondisi medis seperti Diabetes, Hipertensi, dan Penyakit Jantung.
- **Healthy Food Recommendations**: Menampilkan 5 + 10 menu makanan terbaik dengan skor kesehatan tertinggi yang paling sesuai dengan kebutuhan pengguna.
- **Search & Sort Nutrition**: Fitur pencarian database makanan yang dilengkapi dengan fungsi pengurutan (*sorting*) berdasarkan kandungan nutrisi (Kalori, Protein, Karbohidrat, dll).

### C. Technology Stack yang Digunakan
- **Frontend**: HTML5, Tailwind CSS, JavaScript (Vanilla JS).
- **Icons**: Font Awesome 6.0.
- **API Backend**: 
  - `https://evanrzh.theokaitou.my.id/api` (Nutrition Constraints)
  - `https://api.cirro.my.id` (Food Recommendation)
- **Deployment**: GitHub Pages

### D. Cara Kerja Aplikasi
1. **Input Data**: Pengguna memasukkan data fisik dan memilih riwayat kondisi medis.
2. **Analisis Nutrisi**: Aplikasi mengirim data ke API untuk mendapatkan kalkulasi batasan nutrisi (Constraints).
3. **Pencocokan Data**: Algoritma aplikasi memfilter database makanan yang ada di API untuk mencari menu yang tidak melanggar batasan nutrisi pengguna.
4. **Scoring**: Makanan diurutkan berdasarkan skor kesehatan untuk memberikan rekomendasi yang paling optimal.

### Screenshot Website
#### Main Page

#### Food Recommendations Example

#### Food Nutritions Search