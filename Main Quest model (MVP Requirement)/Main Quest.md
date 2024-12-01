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
