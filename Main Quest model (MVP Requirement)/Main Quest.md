# Pendahuluan  

Kami membuat model deteksi stunting, wasting, dan risiko kehamilan untuk memenuhi main quest ML stack. Model ini dirancang untuk membantu masyarakat, khususnya para ibu, dalam mendeteksi kondisi gizi anak dan risiko kehamilan secara dini serta memberikan solusi berbasis data yang mudah diakses, yang dapat meningkatkan kualitas hidup dan kesehatan anak-anak di Indonesia.

# Alasan Kami Memilih Fitur Ini dan Menggunakan Model Ini  

Kami mengkritisi masalah orang tua yang tidak mengetahui apakah anak mereka mengalami stunting atau wasting, atau apakah kondisi kehamilan mereka berisiko. Ketidaktahuan ini sering menghalangi tindakan pencegahan yang dapat diambil lebih awal, yang penting untuk memastikan kesehatan ibu dan anak. Dengan fitur ini, kami ingin menyediakan alat diagnostik yang sederhana namun berbasis data, yang memungkinkan orang tua untuk memantau dan mengambil langkah pencegahan sejak dini, serta memberikan rekomendasi yang dapat mengurangi risiko stunting dan wasting pada anak-anak Indonesia.

# Persiapan Dataset
Organisasi Kesehatan Dunia (WHO) telah menetapkan kriteria standar untuk mengklasifikasikan status gizi, termasuk untuk kondisi stunting (pendek) dan wasting (kekurangan berat badan). Stunting terjadi ketika tinggi badan anak lebih rendah dari standar yang ditentukan untuk usia mereka, menunjukkan kurangnya asupan gizi jangka panjang yang berdampak pada perkembangan fisik. Sedangkan, wasting mengindikasikan kekurangan berat badan secara signifikan yang dapat menyebabkan masalah kesehatan akut.

Dalam bagian ini, kami akan menunjukkan distribusi stunting dan wasting berdasarkan data WHO, yang akan memberikan gambaran mengenai prevalensi status gizi pada anak-anak dan ibu hamil.

## Stunting WHO Chart
Stunting adalah masalah gizi jangka panjang yang dapat memengaruhi perkembangan anak. Di bawah ini adalah **chart WHO** yang menggambarkan **Stunting Pria** dan **Stunting Wanita**, berdasarkan standar pertumbuhan **WHO**.

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

## Wasting WHO Chart
Wasting sendiri adalah masalah kesehatan akut yang terjadi ketika anak kekurangan berat badan yang signifikan. Ini biasanya terjadi akibat malnutrisi yang parah dalam jangka pendek. Berikut adalah **chart WHO** yang menggambarkan **Wasting Pria** dan **Wasting Wanita**, juga berdasarkan standar **WHO**.

<div style="text-align: center;">
    <h3>Stunting WHO Chart</h3>
</div>

<div style="display: flex; justify-content: space-between;">

  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Wasting Pria</h4>
    <img src="./images/chartWHO/wasting_pria.jpg" alt="Stunting Pria" style="width: 100%;"/>
  </div>

  <div style="flex: 1; padding-left: 10px; text-align: center;">
    <h4>Wasting Wanita</h4>
    <img src="./images/chartWHO/wasting_wanita.jpg" alt="Stunting Wanita" style="width: 100%;"/>
  </div>

</div>