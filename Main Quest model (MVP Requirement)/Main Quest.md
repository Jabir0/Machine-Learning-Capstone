# Pendahuluan

Kami membuat model deteksi stunting, wasting, dan risiko kehamilan untuk memenuhi main quest ML stack. Model ini dirancang untuk membantu masyarakat, khususnya para ibu, dalam mendeteksi kondisi gizi anak dan risiko kehamilan secara dini serta memberikan solusi berbasis data yang mudah diakses. Tujuan utama model ini adalah untuk meningkatkan kualitas hidup dan kesehatan anak-anak di Indonesia, terutama dalam menangani masalah stunting dan wasting yang masih menjadi tantangan besar.

# Alasan Kami Memilih Fitur Ini dan Menggunakan Model Ini

Kami mengkritisi masalah orang tua yang tidak mengetahui apakah anak mereka mengalami stunting atau wasting, atau apakah kondisi kehamilan mereka berisiko. Ketidaktahuan ini sering menghalangi tindakan pencegahan yang bisa diambil lebih awal, yang sangat penting untuk memastikan kesehatan ibu dan anak. Dengan fitur ini, kami ingin menyediakan alat diagnostik yang sederhana namun berbasis data, yang memungkinkan orang tua untuk memantau kondisi gizi anak dan mengambil langkah pencegahan sejak dini, serta memberikan rekomendasi berbasis data yang dapat mengurangi risiko stunting dan wasting pada anak-anak Indonesia.

# Persiapan Dataset

Organisasi Kesehatan Dunia (WHO) telah menetapkan kriteria standar untuk mengklasifikasikan status gizi, termasuk untuk kondisi **stunting** (pendek) dan **wasting** (kekurangan berat badan). **Stunting** terjadi ketika tinggi badan anak lebih rendah dari standar yang ditentukan untuk usia mereka, yang menunjukkan kurangnya asupan gizi jangka panjang yang berdampak pada perkembangan fisik. **Wasting** mengindikasikan kekurangan berat badan secara signifikan yang dapat menyebabkan masalah kesehatan akut.

Dalam bagian ini, kami akan menunjukkan distribusi **stunting** dan **wasting** berdasarkan data WHO, yang akan memberikan gambaran mengenai prevalensi status gizi pada anak-anak dan ibu hamil.

## **Stunting WHO Chart**

Stunting adalah masalah gizi jangka panjang yang dapat memengaruhi perkembangan anak. Di bawah ini adalah **chart WHO** yang menggambarkan **Stunting**, berdasarkan standar pertumbuhan **WHO**.

<div style="text-align: center;">
    <h3>Stunting WHO Chart</h3>
</div>

<div style="text-align: center;">
    <img src="./images/chartWHO/stunting_pria.jpg" alt="Stunting" style="width: 100%;"/>
</div>

---

## **Distribusi Kelas Stunting**

Di bawah ini adalah **distribusi dataset stunting** yang menunjukkan sebaran kelas dalam dataset kami, berdasarkan data yang dikumpulkan. Grafik ini menggambarkan prevalensi kondisi stunting secara keseluruhan, tanpa dibedakan berdasarkan jenis kelamin.

<div style="text-align: center;">
    <h3>Distribusi Kelas Stunting</h3>
</div>

<div style="text-align: center;">
    <img src="./images/datasetdistribution/distribusi_stunting.png" alt="Distribusi Kelas Stunting" style="width: 80%;"/>
</div>

---

## **Wasting WHO Chart**

Wasting adalah masalah kesehatan akut yang terjadi ketika anak kekurangan berat badan yang signifikan. Biasanya ini terjadi akibat malnutrisi yang parah dalam jangka pendek. Berikut adalah **chart WHO** yang menggambarkan **Wasting**, berdasarkan standar **WHO**.

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

## **Distribusi Kelas Wasting**

Di bawah ini adalah **distribusi dataset wasting** yang menunjukkan sebaran kelas dalam dataset kami, menggambarkan prevalensi kondisi wasting secara keseluruhan.

<div style="text-align: center;">
    <h3>Distribusi Kelas Wasting</h3>
</div>

<div style="text-align: center;">
    <img src="./images/datasetdistribution/distribusi_wasting.png" alt="Distribusi Kelas Wasting" style="width: 80%;"/>
</div>

