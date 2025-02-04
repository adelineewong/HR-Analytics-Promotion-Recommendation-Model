**Prediksi Promosi Karyawan dengan Machine Learning**
=============================================================

📖 **Deskripsi Proyek**
------------------------
Perusahaan multinasional menghadapi tantangan efisiensi dalam proses promosi karyawan, khususnya untuk posisi manajer 
dan level di bawahnya. Proses manual saat ini tidak hanya memakan waktu tetapi juga mahal, dengan estimasi biaya 
$240 per karyawan. Proyek ini bertujuan mengembangkan model machine learning yang membantu tim HR 
menyaring kandidat potensial secara efisien, meminimalkan biaya evaluasi, dan memastikan fokus pada karyawan berpotensial tinggi.

**Problem Statement**
- **Efisiensi Waktu dan Biaya**: Proses manual yang memakan waktu dan biaya besar menjadi beban bagi tim HR.
- **Optimalisasi Seleksi**: Perusahaan memerlukan model berbasis data untuk memprediksi karyawan yang layak 
  dipromosikan secara akurat.

🎯 **Tujuan Proyek**
--------------------
1️⃣ **Mengidentifikasi Faktor-Faktor Utama** yang memengaruhi kelayakan promosi karyawan.

2️⃣ **Mengembangkan Model Prediksi yang Akurat** untuk membantu perusahaan menyaring kandidat promosi 
    dengan efisiensi tinggi dalam waktu dan biaya.

📊 **Pendekatan Analitik**
--------------------------
1️⃣ **Eksplorasi Data**:
   - Analisis statistik untuk memahami pola dan hubungan antara fitur demografis, performa, dan target promosi.

2️⃣ **Pengembangan Model**:
   - Model LightGBM digunakan untuk menangani ketidakseimbangan data dan memprioritaskan efisiensi prediksi.

3️⃣ **Evaluasi Model**:
   - **Precision**: Memastikan kandidat yang dipilih relevan, mengurangi False Positives.
   - **Recall**: Mengidentifikasi sebanyak mungkin kandidat layak promosi, mengurangi False Negatives.
   - **F-Beta Score (Beta = 0,3)**: Memprioritaskan Precision untuk mengurangi dampak biaya False Positives.

💼 **Implementasi Model**
-------------------------
Model ini digunakan pada checkpoint evaluasi promosi, misalnya pada periode triwulan atau tahunan. 
Rekomendasi model akan membantu tim HR memfokuskan sumber daya pada kandidat berpotensi, 
sehingga mempercepat proses seleksi dan menurunkan biaya evaluasi.

**Proses Implementasi**:

1️⃣ Tahap uji coba untuk memastikan akurasi model sebelum adopsi penuh.

2️⃣ Integrasi model ke sistem HR untuk mendukung analisis prediktif secara langsung.

3️⃣ Analisis dampak implementasi terhadap efisiensi waktu, biaya, dan kepuasan karyawan.
     
💡 **Insight dari Analisis EDA**
-------------------------------
1. **Hubungan Skor Pelatihan dan Promosi**:
   - Karyawan dengan skor pelatihan tinggi (95–99) memiliki peluang promosi hingga 99,5%.
   - Rata-rata skor pelatihan masih rendah (63,39), menunjukkan perlunya peningkatan kualitas pelatihan.

2. **Jumlah Pelatihan vs. Efektivitas**:
   - Karyawan dengan lebih banyak pelatihan memiliki tingkat promosi lebih rendah. Karyawan dengan hanya satu kali pelatihan, yang memiliki proporsi promosi paling besar yaitu 9%.

3. **Penilaian Tahun Sebelumnya**:
   - Skor evaluasi sebelumnya berperan signifikan dalam peluang promosi, dengan korelasi positif terhadap tingkat promosi.

4. **Penghargaan dan Rekrutmen**:
   - Karyawan yang pernah memenangkan penghargaan memiliki peluang promosi lebih tinggi.
   - Saluran rekrutmen ‘referred’ menunjukkan proporsi promosi tertinggi (12,1%), meskipun hanya mencakup 2,1% total karyawan.

⚖️ **Evaluasi Model**
---------------------
1. **Type 1 Error (False Positive)**:
   - Dampak lebih langsung dan terukur, yaitu biaya tambahan evaluasi kandidat tidak relevan.
   - Prioritas diberikan pada Precision untuk meminimalkan False Positives.

2. **Type 2 Error (False Negative)**:
   - Risiko kehilangan karyawan potensial yang tidak terdeteksi.
   - Tetap dipertimbangkan untuk menjaga retensi karyawan.

**Metrik Utama**:
- **F-Beta Score (β=0.3)**: Fokus pada Precision untuk memprioritaskan efisiensi biaya evaluasi.
- **Precision**: Mengurangi evaluasi kandidat tidak relevan.
- **Recall**: Mendeteksi kandidat layak promosi sebanyak mungkin tanpa mengabaikan efisiensi.

📈 **Simulasi Penghematan Biaya**
---------------------------------
1. **Tanpa Model**:
   - Total biaya evaluasi: $2,351,760 (untuk semua karyawan).

2. **Dengan Model**:
   - Total biaya evaluasi: $90,720 (untuk kandidat yang diprediksi layak promosi).

**Total Penghematan**: $2,261,040.

**Kesimpulan**
---------------
Penggunaan model machine learning untuk prediksi promosi karyawan mampu memberikan efisiensi yang signifikan dalam waktu dan biaya. 
Dengan prioritas pada Precision dan simulasi penghematan hingga $2,261,040, model ini membuktikan efektivitasnya dalam mendukung strategi pengelolaan karyawan perusahaan. 
Selain itu, pendekatan berbasis data ini memberikan wawasan baru untuk meningkatkan kualitas tenaga kerja dan efektivitas pelatihan, sambil membuka peluang pengembangan model lebih lanjut.

📋 **Rekomendasi Pengembangan Model**
-------------------------------------
1. **Pengujian Prediksi vs. Evaluasi Manual**:
   - Lakukan pengujian untuk membandingkan hasil promosi berdasarkan prediksi model dengan evaluasi manual. Hal ini dapat memastikan bahwa strategi promosi menjadi lebih efisien dan akurat.

2. **Penambahan Fitur Baru**:
   - Tambahkan data terkait produktivitas tahunan, keterlibatan dalam proyek besar, feedback rekan kerja, atau skor kepuasan lingkungan kerja untuk memperkaya prediksi.

3. **Segmentasi Karyawan**:
   - Analisis lebih dalam berdasarkan senioritas, departemen, atau kontribusi terhadap proyek untuk memahami faktor yang paling memengaruhi promosi di setiap segmen.

4. **Analisis Kesalahan Prediksi**:
   - Perbarui data secara berkala untuk mengurangi bias dan meningkatkan akurasi. Pemahaman terhadap kesalahan model dapat memberikan peluang untuk iterasi model yang lebih baik.

5. **Dampak Promosi terhadap Turnover Rate**:
   - Lakukan analisis mendalam tentang hubungan promosi dan turnover untuk memahami kerugian potensial jika karyawan layak promosi tidak terdeteksi.

📌 Link Tableau
-------------------------------------
https://public.tableau.com/views/PurwadhikaEPSILON/HRDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

![image](https://github.com/user-attachments/assets/2637b723-cb73-4514-b581-5875d7614b7a)

📌 Link Streamlit
-------------------------------------
link github file streamlit : https://github.com/sofyansalim/st-hr-analisis

link public streamlit : https://finalprojectepsilon.streamlit.app/ 
