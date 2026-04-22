# Bank Customer Churn Prediction: Multi-Model Comparison 🏦📊

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Blue?style=for-the-badge)

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk memprediksi kemungkinan nasabah bank akan berhenti berlangganan (**Churn**) menggunakan berbagai algoritma *Machine Learning*. Dengan mengidentifikasi nasabah yang berisiko churn, manajemen bank dapat mengambil tindakan preventif untuk mempertahankan nasabah tersebut.

### Gambar 1 : Grafik Distribusi Nasabah
<img width="1388" height="989" alt="image" src="https://github.com/user-attachments/assets/d5fc3c3b-0712-4492-aa58-f76b9b292897" />

## 📊 Dataset Overview
Dataset yang digunakan mencakup informasi nasabah seperti:
- **Credit Score**, **Age**, **Tenure**, **Balance**.
- **Geography** (Prancis, Jerman, Spanyol).
- **Gender** dan variabel demografis lainnya.
- **Target Variable**: `Exited` (1 = Churn, 0 = Stay).

## 🛠️ Langkah Pengerjaan
1. **Data Cleaning**: Menghapus kolom yang tidak berpengaruh pada model (`RowNumber`, `CustomerId`, `Surname`).
2. **Preprocessing**: 
   - Mengubah data kategori menjadi numerik menggunakan `LabelEncoder` dan `One-Hot Encoding`.
   - Normalisasi fitur menggunakan `StandardScaler`.
3. **Modeling**: Melakukan komparasi performa antara 5 algoritma berbeda:
   - K-Nearest Neighbors (KNN)
   - Decision Tree
   - Random Forest
   - Support Vector Machine (SVM)
   - Naive Bayes
  
### Gambar 2 : Correlation Heatmap
<img width="1016" height="936" alt="image" src="https://github.com/user-attachments/assets/40bffdb8-6a0c-42ac-a41a-9ac998dd6e69" />

## 📈 Perbandingan Performa Model
Berdasarkan hasil pengujian pada dataset, berikut adalah metrik performa masing-masing model:

| Model | Akurasi | Precision | Recall | F1-Score |
| :--- | :---: | :---: | :---: | :---: |
| **Random Forest** | **86.75%** | **76.89%** | 44.22% | **56.16%** |
| **SVM** | 86.40% | 82.78% | 31.81% | 45.96% |
| **KNN** | 84.15% | 71.07% | 31.55% | 43.71% |
| **Naive Bayes** | 82.95% | 70.81% | 27.23% | 39.33% |
| **Decision Tree** | 78.95% | 48.37% | **53.18%** | 50.66% |

### Gambar 3 : Grafik perbandingan antar Model Machine Learning
<img width="1191" height="590" alt="image" src="https://github.com/user-attachments/assets/e47860f3-a4ed-4c1e-bbdb-b383910f5750" />

### 💡 Kesimpulan Utama
- **Random Forest** terpilih sebagai model terbaik secara keseluruhan dengan akurasi **86.75%** dan F1-Score yang paling stabil.
  ### Gambar 4 : Grafik model terbaik (Random Forest)
  <img width="450" height="393" alt="image" src="https://github.com/user-attachments/assets/afd6f71d-44ea-4531-af73-798ff5607736" />

- **SVM** memiliki tingkat **Precision tertinggi (82.78%)**, sangat efektif jika perusahaan ingin meminimalkan kesalahan dalam memprediksi nasabah yang sebenarnya tidak churn.
- **Decision Tree** unggul dalam hal **Recall**, artinya paling baik dalam menangkap jumlah nasabah yang benar-benar akan churn, meskipun akurasinya lebih rendah.

## 🚀 Cara Menjalankan Proyek
1. Clone repositori ini:
   ```bash
   git clone [https://github.com/SamudraDinoNcus/customer-churn-prediction.git](https://github.com/SamudraDinoNcus/customer-churn-prediction.git)
2. Pastikan library terinstall:
   pip install pandas numpy seaborn matplotlib scikit-learn
3. Buka file Customer_Churn_Analysis.ipynb di Google Colab atau Jupyter Notebook.


- Author: [Samudra Dino]
- E-mail: [samudrarisdiyanto5@gmail.com]
