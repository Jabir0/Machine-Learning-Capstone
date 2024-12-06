# Side Quest: Domain-Specific Chatbot with Gemini 1.0 Pro 002  

## Introduction  
Kami mempersembahkan domain-specific chatbot yang dibuat melalui proses fine-tuning menggunakan base model **Gemini 1.0 Pro 002** di Vertex AI Studio. Proyek ini bertujuan untuk memanfaatkan kemampuan text-to-text generation yang ditawarkan oleh Gemini 1.0 Pro 002 untuk menciptakan chatbot yang dapat menjawab pertanyaan-pertanyaan umum terkait kesehatan ibu dan anak dengan cepat dan relevan.  

## Reason Why We Choose This Feature  
Kami mengkritisi platform konsultasi dokter yang sering memerlukan waktu terlalu lama untuk merespons pertanyaan pasien.

<table>
  <tr>
    <td><div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Waktu Pasien Bertanya</h4>
    <img src="images\waktu_pasien_bertanya.png" alt="Pasien bertanya" style="width: 50%;"/>
  </div>
  </div></td>
    <td><div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Waktu Dokter Menjawab</h4>
    <img src="images\waktu_dokter_menjawab.png" alt="Pasien bertanya" style="width: 100%;"/>
  </div>
  </div></td>
  </tr>
</table>

Masalah ini dapat menyebabkan ketidaknyamanan bagi calon ibu, orang tua baru, dan ibu-ibu muda yang membutuhkan jawaban cepat. Untuk menjawab tantangan ini, kami merancang domain-specific chatbot yang mampu memberikan jawaban akurat terhadap pertanyaan umum yang sering diajukan.  

## Fine-Tuning Preparation  

### 1. Preparing the Model  
Kami memilih model terbaik dari Model Garden untuk mendukung fitur domain-specific chatbot.
<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Model Garden Vertex AI</h4>
    <img src="images\model_garden_vertexai (1).png" alt="Model Garden" style="width: 100%;"/>
  </div>
</div>

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="images\model_garden_vertexai (2).png" alt="Model Garden" style="width: 100%;"/>
  </div>
</div>

Setelah mempertimbangkan berbagai opsi, kami memutuskan menggunakan **Gemini 1.0 Pro 002** untuk fine-tuning karena: 

- **Use case** dan prompt-nya fokus pada **text-to-text generation**.  
- Dirancang untuk menyeimbangkan kualitas, performa, dan biaya untuk tugas seperti **content generation**, **editing**, **summarization**, dan **classification**.  
- Cocok untuk kebutuhan chatbot terkait kesehatan ibu dan anak.  

### 2. Preparing the Dataset  
Kami mengumpulkan data dari platform konsultasi dokter untuk memperoleh pasangan pertanyaan dan jawaban.

Link Kumpulan Tanya Jawab :

https://www.alodokter.com/komunitas/topic-tag/bayi
https://www.alodokter.com/komunitas/topic-tag/stunting


Karena banyak pertanyaan yang serupa di platform tersebut, kami menggunakan Generative AI untuk melakukan augmentasi pada pertanyaan dan jawaban umum. Hasilnya kami kumpul ke dalam csv berikut :

[Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/dataset/persiapan_dataset_qna.csv](https://github.com/Jabir0/Machine-Learning-GIZI/blob/main/Side%20Quest%20model%20(finetuning%20gemini%201.0%20in%20Vertex%20AI%20Studio)/dataset/persiapan_dataset_qna.csv)

Distribusi dataset yang digunakan adalah:  
- **60% data** dari platform konsultasi dokter.  
- **40% data** yang dihasilkan melalui Generative AI.  

**Finetuning Dataset Requirements:**  
Dataset yang disiapkan untuk Gemini 1.0 Pro 002 memiliki struktur berikut:  
```jsonl
{
  "messages": [
    {
      "role": "string",
      "content": "string"
    }
  ]
}
```  
Detail penting:  
- **Role:** dapat berupa `system`, `user`, atau `model`.  
- **Content:** berisi isi pesan dengan batas maksimal token untuk konteks dan pesan gabungan sebesar **32,768 tokens**.  
- **System role** hanya digunakan sebagai elemen pertama dalam array (opsional).  
- Panjang token maksimal per pesan untuk role `model` adalah **8,192 tokens**.  

**role** `system`, kami mengatur bahwa `system` adalah seorang dokter anak,dokter umum, dan ahli gizi yang mencoba memberikan edukasi kesehatan kepada orang tua. 

**role** `user`, diisi dengan chat/pertanyaan dari user/pasien, dan **role** `model` diisi dengan jawaban dari dokter untuk pertanyaan user/pasien.

Berikut contohnya :
```jsonl
{"messages": [{"role": "system", "content": "Anda adalah dokter spesialis anak yang memberikan edukasi dan saran mengenai kesehatan anak dan perawatan bayi."}, {"role": "user", "content": "Dokter bayi saya usia 4 bulan, sekarang lagi pilek dok, saya prefer obatin secara alami dulu dok, bagaimana cara mengatasi pilek pake obat alami ya dok? Mohon saran nya dok "}, {"role": "model", "content": "Pilek pada bayi bisa disebabkan oleh infeksi virus, dan meskipun pengobatan medis mungkin diperlukan jika gejalanya parah, ada beberapa cara alami yang bisa membantu meringankan gejala pilek pada bayi:\n\n1. **Menggunakan humidifier**: Gunakan humidifier di kamar bayi untuk menjaga kelembapan udara. Ini membantu meringankan hidung tersumbat dan mengurangi iritasi pada saluran napas bayi.\n2. **Kompres hangat**: Kompreskan kain hangat di bagian wajah bayi, terutama pada area hidung dan dada, untuk membantu melegakan pernapasan dan mengurangi ketidaknyamanan.\n3. **Mengatur posisi tidur**: Tidurkan bayi dengan posisi kepala sedikit lebih tinggi untuk membantu mengurangi hidung tersumbat dan memudahkan pernapasan.\n4. **Menjaga kebersihan udara**: Pastikan udara di sekitar bayi tidak tercemar polusi atau asap rokok, karena ini bisa memperburuk pilek bayi.\n\nJika pilek disertai demam tinggi, kesulitan bernapas, atau tidak membaik setelah beberapa hari, sebaiknya segera konsultasikan dengan dokter anak."}]}
```

Untuk lebih lengkapnya, bisa liat pada dataset berikut :
https://github.com/Jabir0/Machine-Learning-GIZI/blob/main/Side%20Quest%20model%20(finetuning%20gemini%201.0%20in%20Vertex%20AI%20Studio)/dataset/dataset_qna_fix.jsonl

Setelah dataset diproses, kami menyimpannya ke dalam Google Cloud Storage bucket untuk keperluan fine-tuning.  
<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="images\bucket capstone.png" alt="Bucket Capstone" style="width: 100%;"/>
  </div>
</div>

### 3. Fine-Tuning the Model Setting
Berikut Settingan Finetuning model kami :

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="images\finetuning preparation (1).png" alt="Bucket Capstone" style="width: 100%;"/>
  </div>
</div>
<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="images\finetuning preparation (2).png" alt="Bucket Capstone" style="width: 100%;"/>
  </div>
</div>

## Results  

### Fine-Tuning Metrics  
Setelah start tuning dan masuk ke proses fine-tuning, kami memperoleh hasil metrics berikut:

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Monitor Tuning Progress</h4>
    <img src="finetuning-gemini1.0\documentation finetuning\dokumentasi monitor finetuning.png" alt="Monitoring Tuning Progress" style="width: 100%;"/>
  </div>
</div>

<table>
  <tr>
    <td><div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="finetuning-gemini1.0\documentation finetuning\Fraction of correct next step preds.png" alt="Fraction of correct next step preds" style="width: 100%;"/>
  </div></div></td>
    <td><div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="finetuning-gemini1.0\documentation finetuning\Fraction of correct next step preds.png" alt="Fraction of correct next step preds" style="width: 100%;"/>
  </div></div></td>
    <td><div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="finetuning-gemini1.0\documentation finetuning\Fraction of correct next step preds.png" alt="Fraction of correct next step preds" style="width: 100%;"/>
  </div></div></td>
  </tr>
</table>

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Tunning Model Dataset</h4>
    <img src="dataset\dokumentasi dataset finetuning_1.png" alt="Tuning Model Dataset" style="width: 100%;"/>
  </div>
</div>
<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="dataset\dokumentasi dataset finetuning_2.png" alt="Tuning Model Dataset" style="width: 100%;"/>
  </div>
</div>
<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="dataset\dokumentasi dataset finetuning_3.png" alt="Tuning Model Dataset" style="width: 100%;"/>
  </div>
</div>

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Tunning Model Details</h4>
    <img src="finetuning-gemini1.0\documentation finetuning\dokumentasi detail finetuning.png" alt="Tunning Model Details" style="width: 100%;"/>
  </div>
</div>

### Test Results  
Hasil uji model fine-tuning ditampilkan pada chat di Vertex AI Studio. Chatbot berhasil menjawab pertanyaan umum dengan tingkat relevansi yang tinggi.

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Test Chatbot</h4>
    <img src="images\test-finetuning model (1).png" alt="Coba Finetuning Model" style="width: 100%;"/>
  </div>
</div>
<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <img src="images\test-finetuning model (2).png" alt="Coba Finetuning Model" style="width: 100%;"/>
  </div>
</div>

## Deploying the Model  
Setelah proses fine-tuning selesai, fine-tuning model `chatbot_gizi_model` diserahkan ke tim **Cloud Computing cohort** untuk pembuatan endpoint. Endpoint ini akan digunakan sebagai backend untuk integrasi chatbot dalam aplikasi.  
