# Pendahuluan

Kami membuat model deteksi **stunting**, **wasting**, dan **risiko kehamilan** untuk memenuhi main quest ML stack. Model ini dirancang untuk membantu masyarakat, khususnya para ibu, dalam mendeteksi kondisi gizi anak dan risiko kehamilan secara dini serta memberikan solusi berbasis data yang mudah diakses. Tujuan utama model ini adalah untuk meningkatkan kualitas hidup dan kesehatan anak-anak di Indonesia, terutama dalam menangani masalah stunting dan wasting yang masih menjadi tantangan besar.

---

# Alasan Kami Memilih Fitur Ini dan Menggunakan Model Ini

Kami mengkritisi masalah orang tua yang tidak mengetahui apakah anak mereka mengalami **stunting** atau **wasting**, atau apakah kondisi kehamilan mereka berisiko. Ketidaktahuan ini sering menghalangi tindakan pencegahan yang bisa diambil lebih awal, yang sangat penting untuk memastikan kesehatan ibu dan anak. Dengan fitur ini, kami ingin menyediakan alat diagnostik yang sederhana namun berbasis data, yang memungkinkan orang tua untuk memantau kondisi gizi anak dan mengambil langkah pencegahan sejak dini, serta memberikan rekomendasi berbasis data yang dapat mengurangi risiko stunting dan wasting pada anak-anak Indonesia.

---

# Persiapan Dataset

Organisasi Kesehatan Dunia (WHO) telah menetapkan kriteria standar untuk mengklasifikasikan status gizi, termasuk untuk kondisi **stunting** (pendek) dan **wasting** (kekurangan berat badan).  

- **Stunting** terjadi ketika tinggi badan anak lebih rendah dari standar yang ditentukan untuk usia mereka, menunjukkan kurangnya asupan gizi jangka panjang yang berdampak pada perkembangan fisik.  
- **Wasting** mengindikasikan kekurangan berat badan secara signifikan, yang sering kali disebabkan oleh malnutrisi akut atau penyakit yang memengaruhi berat badan anak dalam waktu singkat.  

Dalam bagian ini, kami akan menunjukkan pembagian kelas dan distribusi dataset berdasarkan indikator **PB/U (Panjang Badan sesuai Umur)** untuk stunting dan **BB/U (Berat Badan sesuai Umur)** untuk wasting.  

---

## **Stunting WHO Chart dan Distribusi Kelas Dataset**

**Stunting** mengacu pada kondisi kekurangan gizi kronis yang menyebabkan tinggi badan anak lebih rendah dari standar yang sesuai dengan usianya.  

### **Kategori Kelas Stunting (PB/U):**
- **Sangat Pendek:** Tinggi badan kurang dari -3 SD.  
- **Pendek:** Tinggi badan berada di -3 SD hingga kurang dari -2 SD.  
- **Normal:** Tinggi badan berada di -2 SD hingga +3 SD.  
- **Tinggi:** Tinggi badan lebih dari +3 SD.  

### **Visualisasi Stunting WHO Chart**

<div style="text-align: center;">
    <h3>Stunting WHO Chart</h3>
</div>

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Stunting Pria</h4>
    <img src="./images/chartWHO/stunting_pria.jpg" alt="Stunting Pria" style="width: 100%;"/>
  </div>
  <div style="flex: 1; padding-left: 10px; text-align: center;">
    <h4>Stunting Wanita</h4>
    <img src="./images/chartWHO/stunting_wanita.jpg" alt="Stunting Wanita" style="width: 100%;"/>
  </div>
</div>

---

### **Distribusi Kelas Stunting**

Grafik berikut menunjukkan sebaran kelas stunting dalam dataset, menggambarkan prevalensi anak-anak berdasarkan panjang badan mereka.  

<div style="text-align: center;">
    <h3>Distribusi Kelas Stunting</h3>
</div>

<div style="text-align: center;">
    <img src="./images/datasetdistribution/distribusi_stunting.png" alt="Distribusi Kelas Stunting" style="width: 80%;"/>
</div>

---

## **Wasting WHO Chart dan Distribusi Kelas Dataset**

**Wasting** adalah kondisi gizi akut yang terjadi ketika berat badan anak lebih rendah dari standar usianya.  

### **Kategori Kelas Wasting (BB/U):**
- **Berat Badan Sangat Kurang:** Berat badan kurang dari -3 SD.  
- **Berat Badan Kurang:** Berat badan berada di -3 SD hingga kurang dari -2 SD.  
- **Normal:** Berat badan berada di -2 SD hingga +1 SD.  
- **Risiko Berat Badan Berlebih:** Berat badan lebih dari +1 SD.  

### **Visualisasi Wasting WHO Chart**

<div style="text-align: center;">
    <h3>Wasting WHO Chart</h3>
</div>

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Wasting Pria</h4>
    <img src="./images/chartWHO/wasting_pria.jpg" alt="Wasting Pria" style="width: 100%;"/>
  </div>
  <div style="flex: 1; padding-left: 10px; text-align: center;">
    <h4>Wasting Wanita</h4>
    <img src="./images/chartWHO/wasting_wanita.jpg" alt="Wasting Wanita" style="width: 100%;"/>
  </div>
</div>

---

### **Distribusi Kelas Wasting**

Grafik berikut menunjukkan sebaran kelas wasting dalam dataset, menggambarkan prevalensi anak-anak berdasarkan berat badan mereka.  

<div style="text-align: center;">
    <h3>Distribusi Kelas Wasting</h3>
</div>

<div style="text-align: center;">
    <img src="./images/datasetdistribution/distribusi_wasting.png" alt="Distribusi Kelas Wasting" style="width: 80%;"/>
</div>

---

# Maternal Health Risk

### Pendahuluan
Model deteksi risiko kesehatan kehamilan ini dirancang untuk membantu mengidentifikasi kondisi medis yang berisiko pada ibu hamil, seperti hipertensi, diabetes, dan masalah jantung. Tujuan model ini adalah untuk mendeteksi secara dini potensi masalah kesehatan selama kehamilan dan memberikan solusi berbasis data untuk mengurangi risiko bagi ibu dan bayi.

### Alasan Kami Memilih Fitur Ini dan Menggunakan Model Ini
Kami memilih fitur ini karena banyak ibu hamil yang tidak menyadari adanya potensi risiko kesehatan yang dapat membahayakan diri mereka dan bayi. Deteksi dini terhadap kondisi seperti hipertensi dan masalah gula darah dapat mengurangi angka kematian ibu dan bayi. Model ini bertujuan untuk memberikan alat prediksi yang sederhana namun berbasis data bagi ibu hamil.

### Persiapan Dataset
Dataset ini berisi data medis ibu hamil dengan fitur-fitur seperti usia, tekanan darah, kadar gula darah, suhu tubuh, detak jantung, dan level risiko kehamilan. Data ini digunakan untuk melatih model dalam memprediksi risiko kehamilan berdasarkan indikator medis.

### Detail Dataset
Dataset **Maternal Health Risk** terdiri dari 1014 entri dengan 7 kolom utama:
- **Age**: Usia ibu hamil.
- **SystolicBP**: Tekanan darah sistolik.
- **DiastolicBP**: Tekanan darah diastolik.
- **BS**: Level gula darah.
- **BodyTemp**: Suhu tubuh.
- **HeartRate**: Denyut jantung.
- **RiskLevel**: Level risiko kehamilan (High risk, Low risk, Mid risk).

### Credit Dataset
Dataset ini berasal dari [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/863/maternal+health+risk). Terima kasih kepada penyedia dataset yang memungkinkan pengembangan model ini.

### Distribusi Kelas
Dataset ini memiliki tiga kategori dalam **RiskLevel**:
- **High risk**: Risiko tinggi.
- **Low risk**: Risiko rendah.
- **Mid risk**: Risiko menengah.

Berikut adalah distribusi kelas pada dataset ini:

<div style="text-align: center;">
    <h3>Distribusi Kelas Maternal Health Risk</h3>
</div>

<div style="text-align: center;">
    <img src="./images/datasetdistribution/distribusi_maternal_health_risk.png" alt="Distribusi maternal health risk" style="width: 80%;"/>
</div>

---

# Hasil Model pada APK

Setelah model disimpan dalam format TensorFlow Lite (TFLite), model diintegrasikan ke dalam aplikasi Android untuk memberikan prediksi secara real-time. Aplikasi ini menerima input dari pengguna dan kemudian menampilkan hasil prediksi langsung di layar perangkat.

### Prediksi Stunting dan Wasting

Bagian pertama dari aplikasi memberikan prediksi terkait Stunting dan Wasting, yang membantu orang tua untuk mendeteksi kondisi gizi anak berdasarkan data tinggi dan berat badan mereka.

![Hasil Model Prediksi Stunting Dan Wasting](./images/screenshot_apk_result.png)

Pada gambar berikut, Anda dapat melihat bagaimana hasil prediksi untuk Stunting dan Wasting ditampilkan, memberikan informasi apakah anak mengalami Stunting, Wasting, atau Normal berdasarkan data tinggi badan dan berat badan mereka.

- **Stunting**: Menampilkan hasil prediksi apakah anak termasuk dalam kategori Sangat Pendek, Pendek, atau Normal berdasarkan tinggi badan mereka.
- **Wasting**: Menampilkan hasil prediksi apakah anak mengalami Berat Badan Sangat Kurang, Berat Badan Kurang, atau Normal berdasarkan berat badan mereka.

### Prediksi Risiko Kesehatan Kehamilan (Maternal Health Risk)

Bagian kedua dari aplikasi adalah prediksi terkait Risiko Kesehatan Kehamilan, yang berfungsi untuk membantu ibu hamil memantau kesehatan mereka dengan mendeteksi kondisi medis berisiko seperti hipertensi, diabetes, dan masalah jantung.

![Hasil Model Prediksi Stunting Dan Wasting](./images/screenshot_apk_result.png)

Pada gambar berikut, Anda dapat melihat bagaimana hasil prediksi untuk Maternal Health Risk ditampilkan, memberikan informasi mengenai tingkat risiko kesehatan ibu hamil berdasarkan data medis yang dimasukkan, seperti tekanan darah, kadar gula darah, suhu tubuh, dan denyut jantung.

- **High risk**: Risiko tinggi, menunjukkan bahwa ibu hamil berisiko mengalami komplikasi serius.
- **Low risk**: Risiko rendah, yang menunjukkan bahwa ibu hamil tidak menunjukkan tanda-tanda komplikasi serius.
- **Mid risk**: Risiko sedang, yang menunjukkan ada beberapa faktor yang perlu diperhatikan untuk mencegah komplikasi.

---