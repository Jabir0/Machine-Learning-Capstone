# Pendahuluan  

Kami membuat model deteksi risiko stunting-wasting dan kehamilan untuk memenuhi main quest ML stack. Model ini dirancang untuk memberikan solusi yang dapat membantu masyarakat, khususnya para ibu, dalam mendeteksi risiko stunting-wasting dan kondisi kehamilan secara dini. Selain itu, model ini menyediakan solusi berbasis data yang mudah diakses untuk mendukung pengambilan keputusan yang lebih tepat dan efektif.

# Alasan Kami Memilih Fitur Ini dan Menggunakan Model Ini  

Kami mengkritisi masalah orang tua yang tidak tahu apakah anak mereka mengalami risiko stunting-wasting atau apakah kondisi kehamilan mereka dalam keadaan baik atau berisiko. Ketidaktahuan ini sering kali menghambat tindakan pencegahan yang sebenarnya dapat dilakukan lebih awal untuk mengurangi dampak buruk terhadap kesehatan ibu dan anak. Dengan fitur ini, kami ingin memberikan alat diagnostik yang sederhana namun berbasis data akurat untuk membantu masyarakat memahami kondisi kesehatan mereka dengan lebih baik dan mengambil langkah yang tepat sejak dini.

# Persiapan Dataset
Organisasi Kesehatan Dunia (WHO) telah menetapkan kriteria standar untuk mengklasifikasikan status gizi, termasuk untuk kondisi stunting (pendek) dan wasting (kekurangan berat badan). Stunting terjadi ketika tinggi badan anak lebih rendah dari standar yang ditentukan untuk usia mereka, menunjukkan kurangnya asupan gizi jangka panjang yang berdampak pada perkembangan fisik. Sedangkan, wasting mengindikasikan kekurangan berat badan secara signifikan yang dapat menyebabkan masalah kesehatan akut.

Dalam bagian ini, kami akan menunjukkan distribusi stunting dan wasting berdasarkan data WHO, yang akan memberikan gambaran mengenai prevalensi status gizi pada anak-anak dan ibu hamil.

## Stunting WHO Chart
Berikut adalah chart WHO yang menggambarkan **Stunting Pria** dan **Stunting Wanita** Berdasarkan standar WHO. 

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

