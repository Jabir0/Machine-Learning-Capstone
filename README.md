# Machine Learning Repository (GIZI)

# Introduction

We developed a detection model for **stunting**, **wasting**, and **maternal health risks** to fulfill the main quest of the ML stack. This model is designed to assist the community, especially mothers, in early detection of children’s nutritional conditions and pregnancy risks. It provides data-driven solutions that are easily accessible. The primary goal of this model is to improve the quality of life and health of children in Indonesia, particularly in addressing the ongoing challenges of stunting and wasting.

---

# Why We Chose These Features and This Model

We observed that many parents are unaware of whether their children are experiencing **stunting** or **wasting**, or whether their pregnancy is at risk. This lack of knowledge often prevents early preventive measures, which are crucial for ensuring the health of both mother and child. Through this feature, we aim to provide a simple yet data-driven diagnostic tool that allows parents to monitor their children's nutritional conditions and take early preventive actions. Additionally, the tool offers data-based recommendations to mitigate the risk of stunting and wasting among Indonesian children.

---

# Stunting and Wasting Detection


## Dataset Preparation

The World Health Organization (WHO) has established standard criteria to classify nutritional statuses, including conditions like **stunting** (short stature) and **wasting** (underweight).  

- **Stunting** occurs when a child’s height is below the standard for their age, indicating long-term nutritional deficiencies that impact physical development.  
- **Wasting** signifies a significant underweight condition, often due to acute malnutrition or illnesses that affect the child’s weight over a short period.  

In this section, we present the class distribution and dataset division based on indicators such as **HAZ (Height-for-Age Z-score)** for stunting and **WAZ (Weight-for-Age Z-score)** for wasting.  

---

## **Stunting WHO Chart and Dataset Class Distribution**

**Stunting** refers to chronic malnutrition that results in a child’s height being lower than the standard for their age.  

### **Stunting Categories (HAZ):**
- **Severely Stunted:** Height less than -3 SD.  
- **Stunted:** Height between -3 SD and -2 SD.  
- **Normal:** Height between -2 SD and +3 SD.  
- **Tall:** Height greater than +3 SD. 

<a href="https://hellosehat.com/parenting/bayi/gizi-bayi/status-gizi-bayi/">Source</a>

### **Stunting WHO Chart Visualization**

<div style="text-align: center;">
    <h3>Stunting WHO Chart</h3>
</div>

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Stunting (Male)</h4>
    <img src="Main Quest model (MVP Requirement)\images\chartWHO\stunting_pria.jpg" alt="Stunting Male" style="width: 80%;"/>
  </div>
  <div style="flex: 1; padding-left: 10px; text-align: center;">
    <h4>Stunting (Female)</h4>
    <img src="Main Quest model (MVP Requirement)/images/chartWHO/stunting_wanita.jpg" alt="Stunting Female" style="width: 80%;"/>
  </div>
</div>

---

### **Stunting Class Distribution**

The following chart illustrates the class distribution for stunting in the dataset, depicting the prevalence of children based on their height measurements.  

<div style="text-align: center;">
    <h3>Stunting Class Distribution</h3>
</div>

<div style="text-align: center;">
    <img src="Main Quest model (MVP Requirement)/images/datasetdistribution/distribusi_stunting.png" alt="Stunting Class Distribution" style="width: 80%;"/>
</div>

---

## **Wasting WHO Chart and Dataset Class Distribution**

**Wasting** indicates acute nutritional deficiency when a child’s weight is below the standard for their age.  

### **Wasting Categories (WAZ):**
- **Severely Underweight:** Weight less than -3 SD.  
- **Underweight:** Weight between -3 SD and -2 SD.  
- **Normal:** Weight between -2 SD and +1 SD.  
- **Risk of Overweight:** Weight greater than +1 SD. 

<a href="https://hellosehat.com/parenting/bayi/gizi-bayi/status-gizi-bayi/">Source</a>


### **Wasting WHO Chart Visualization**

<div style="text-align: center;">
    <h3>Wasting WHO Chart</h3>
</div>

<div style="display: flex; justify-content: space-between;">
  <div style="flex: 1; padding-right: 10px; text-align: center;">
    <h4>Wasting (Male)</h4>
    <img src="Main Quest model (MVP Requirement)/images/chartWHO/wasting_pria.jpg" alt="Wasting Male" style="width: 80%;"/>
  </div>
  <div style="flex: 1; padding-left: 10px; text-align: center;">
    <h4>Wasting (Female)</h4>
    <img src="Main Quest model (MVP Requirement)/images/chartWHO/wasting_wanita.jpg" alt="Wasting Female" style="width: 80%;"/>
  </div>
</div>

---

### **Wasting Class Distribution**

The chart below illustrates the class distribution for wasting in the dataset, showing the prevalence of children based on their weight measurements.  

<div style="text-align: center;">
    <h3>Wasting Class Distribution</h3>
</div>

<div style="text-align: center;">
    <img src="Main Quest model (MVP Requirement)/images/datasetdistribution/distribusi_wasting.png" alt="Wasting Class Distribution" style="width: 80%;"/>
</div>

---

# Model Evaluation
<div style="text-align: center;">
    <img src="Main Quest model (MVP Requirement)/images/Model Result/output_model_1.png" style="width: 80%;"/>
</div>

---

# Maternal Health Risk

### Introduction
The maternal health risk detection model is designed to help identify risky medical conditions in pregnant women, such as hypertension, diabetes, and heart problems. The goal of this model is to detect potential health issues during pregnancy early and provide data-based solutions to reduce risks for both mother and baby.

### Why We Chose This Feature and Model
We chose this feature because many pregnant women are unaware of potential health risks that could endanger themselves and their babies. Early detection of conditions like hypertension and glucose abnormalities can significantly reduce maternal and infant mortality rates. This model aims to provide a simple yet data-driven prediction tool for pregnant women.

### Dataset Preparation
This dataset contains medical records of pregnant women with features such as age, blood pressure, blood sugar levels, body temperature, heart rate, and pregnancy risk levels. This data is used to train the model to predict pregnancy risks based on medical indicators.

### Dataset Details
The **Maternal Health Risk** dataset consists of 1014 entries with 7 key columns:
- **Age**: Age of the pregnant woman.  
- **SystolicBP**: Systolic blood pressure.  
- **DiastolicBP**: Diastolic blood pressure.  
- **BS**: Blood sugar levels.  
- **BodyTemp**: Body temperature.  
- **HeartRate**: Heart rate.  
- **RiskLevel**: Pregnancy risk level (High risk, Low risk, Mid risk).  

### Dataset Source
This dataset is from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/863/maternal+health+risk). Thanks to the dataset provider for enabling this model's development.

### Class Distribution
The dataset contains three categories in **RiskLevel**:
- **High risk**: High risk.  
- **Low risk**: Low risk.  
- **Mid risk**: Moderate risk.  

The class distribution is as follows:

<div style="text-align: center;">
    <h3>Maternal Health Risk Class Distribution</h3>
</div>

<div style="text-align: center;">
    <img src="Main Quest model (MVP Requirement)/images/datasetdistribution/distribusi_maternal_health_risk.png" alt="Maternal Health Risk Class Distribution" style="width: 80%;"/>
</div>

# Model Evaluation
<div style="text-align: center;">
    <img src="Main Quest model (MVP Requirement)/images/Model Result/output_model_2.png" style="width: 80%;"/>
</div>

---

# Model Results in the Application

After the model was saved in TensorFlow Lite (TFLite) format, it was integrated into an Android application to provide real-time predictions. The app receives user inputs and displays prediction results directly on the device screen.

### Stunting and Wasting Predictions

The first part of the app provides predictions related to Stunting and Wasting, helping parents detect their child's nutritional conditions based on height and weight data.

![Model Prediction Results for Stunting and Wasting](./images/screenshot_apk_result.png)

The following image shows how prediction results for Stunting and Wasting are displayed, providing information on whether a child experiences Stunting, Wasting, or Normal conditions based on their height and weight.

- **Stunting**: Displays whether the child falls into the Severely Stunted, Stunted, or Normal category based on their height.  
- **Wasting**: Displays whether the child is Severely Underweight, Underweight, or Normal based on their weight.  

### Maternal Health Risk Prediction

The second part of the app provides predictions related to Maternal Health Risks, helping pregnant women monitor their health by detecting risky medical conditions such as hypertension, diabetes, and heart problems.

![Model Prediction Results for Maternal Health Risk](./images/screenshot_apk_result.png)

The following image shows how prediction results for Maternal Health Risks are displayed, providing information about the pregnancy risk level based on medical data such as blood pressure, glucose levels, body temperature, and heart rate.

- **High risk**: High risk, indicating potential serious complications.  
- **Low risk**: Low risk, indicating no signs of serious complications.  
- **Mid risk**: Moderate risk, indicating some factors to monitor to prevent complications.  

---

# Main Quest (MVP Requirement for Machine Learning) 
### ✅ Utilize TensorFlow architecture for building machine learning models.
### ✅ Vertex AI can only be used if you intend to build Generative AI. (Note: Vertex AI is a relatively expensive service, so it's your responsibility to use the provided GCP credits wisely.)
### ✅ Students are prohibited from using existing models from TensorFlow Hub and similar resources.
### ✅ Students are prohibited from using models directly from API services such as ChatGPT API, Gemini API, etc.
### ✅ Using AutoML for creating discriminative AI models is prohibited (Vertex AI is allowed only for Generative AI use cases).

# Side Quest: Domain-Specific Chatbot with Gemini 1.0 Pro 002  

## Introduction  
We present a domain-specific chatbot developed through fine-tuning the **Gemini 1.0 Pro 002** base model in Vertex AI Studio. This project leverages the text-to-text generation capabilities of Gemini 1.0 Pro 002 to create a chatbot that can swiftly and accurately address frequently asked questions related to maternal and child health.  

## Why We Chose This Feature  
We identified a common issue with existing doctor consultation platforms: response times are often too long for patients seeking urgent answers.  

<table style="width: 100%;">
  <tr>
    <td style="width: 50%; text-align: center;">
      <h4>Patient Inquiry Time</h4>
      <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/waktu_pasien_bertanya.png" alt="Patient Inquiry Time" style="width: 100%;"/>
    </td>
    <td style="width: 50%; text-align: center;">
      <h4>Doctor Response Time</h4>
      <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/waktu_dokter_menjawab.png" alt="Doctor Response Time" style="width: 100%;"/>
    </td>
  </tr>
</table>

This delay causes discomfort for expectant mothers, new parents, and young mothers who need prompt answers. To tackle this issue, we designed a domain-specific chatbot capable of delivering accurate answers to frequently asked questions.

---

## Fine-Tuning Preparation  

### 1. Preparing the Model  
We selected the best model from the Model Garden in Vertex AI to support the domain-specific chatbot feature.  

<div style="text-align: center;">
  <h4>Model Garden in Vertex AI</h4>
  <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/model_garden_vertexai (1).png" alt="Model Garden Overview" style="width: 100%; margin-bottom: 10px;"/>
  <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/model_garden_vertexai (2).png" alt="Model Selection" style="width: 100%;"/>
</div>

After evaluating various options, we chose **Gemini 1.0 Pro 002** for fine-tuning because:  

- It supports **text-to-text generation**, aligning with our use case and prompts.  
- It balances quality, performance, and cost for tasks like **content generation**, **editing**, **summarization**, and **classification**.  
- It fits the chatbot requirements for maternal and child health topics.  

---

### 2. Preparing the Dataset  
We gathered data from doctor consultation platforms to obtain question-answer pairs.  

**Sources of Question-Answer Data:**  
- [Alodokter - Baby Health Community](https://www.alodokter.com/komunitas/topic-tag/bayi)  
- [Alodokter - Stunting Community](https://www.alodokter.com/komunitas/topic-tag/stunting)  

To handle repetitive questions on these platforms, we utilized Generative AI to augment common question-answer pairs. The resulting dataset is compiled into a CSV file:  

- [Dataset (CSV)](https://github.com/Jabir0/Machine-Learning-GIZI/blob/main/Side%20Quest%20model%20(finetuning%20gemini%201.0%20in%20Vertex%20AI%20Studio)/dataset/persiapan_dataset_qna.csv)  

**Dataset Distribution:**  
- **60%** of the data is sourced from doctor consultation platforms.  
- **40%** of the data is generated using Generative AI.  

**Fine-Tuning Dataset Requirements:**  
The dataset prepared for Gemini 1.0 Pro 002 follows this structure:  

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

Key details:  
- **Role**: Can be `system`, `user`, or `model`.  
- **Content**: Contains the message text with a combined context and message token limit of **32,768 tokens**.  
- **System role** is used only as the first element in the array (optional).  
- Maximum token length per `model` message is **8,192 tokens**.  

For the **system** role, we defined it as a pediatrician, general practitioner, and nutritionist providing health education to parents. The **user** role contains user/patient queries, while the **model** role includes the doctor’s response.  

Example:  
```jsonl
{
  "messages": [
    {
      "role": "system",
      "content": "Anda adalah dokter spesialis anak yang memberikan edukasi dan saran mengenai kesehatan anak dan perawatan bayi."
    },
    {
      "role": "user",
      "content": "Dokter, bayi saya usia 4 bulan sekarang sedang pilek. Saya lebih suka menggunakan pengobatan alami terlebih dahulu. Bagaimana cara mengatasi pilek dengan cara alami? Mohon sarannya."
    },
    {
      "role": "model",
      "content": "Pilek pada bayi sering disebabkan oleh infeksi virus. Meskipun pengobatan medis mungkin diperlukan untuk gejala yang parah, berikut beberapa cara alami yang dapat membantu:\n\n1. **Humidifier**: Gunakan humidifier di kamar bayi untuk menjaga kelembapan udara. Ini membantu meredakan hidung tersumbat dan mengurangi iritasi.\n2. **Kompres hangat**: Tempelkan kain hangat pada wajah bayi, terutama di area hidung dan dada, untuk membantu melegakan pernapasan dan mengurangi ketidaknyamanan.\n3. **Atur posisi tidur**: Tidurkan bayi dengan posisi kepala sedikit lebih tinggi untuk mengurangi hidung tersumbat dan mempermudah pernapasan.\n4. **Udara bersih**: Pastikan udara di sekitar bayi bebas dari polusi atau asap rokok, karena dapat memperburuk pilek.\n\nJika pilek disertai demam tinggi, kesulitan bernapas, atau berlangsung lebih dari beberapa hari, segera konsultasikan dengan dokter anak."
    }
  ]
}
```  

Full dataset: [Q&A Dataset (JSONL)](https://github.com/Jabir0/Machine-Learning-GIZI/blob/main/Side%20Quest%20model%20(finetuning%20gemini%201.0%20in%20Vertex%20AI%20Studio)/dataset/dataset_qna_fix.jsonl)  

The processed dataset was stored in a Google Cloud Storage bucket for fine-tuning.  

<div style="text-align: center;">
  <h4>Cloud Storage Bucket</h4>
  <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/bucket capstone.png" alt="Cloud Storage" style="width: 100%;"/>
</div>

---

### 3. Fine-Tuning Settings  

<div style="text-align: center;">
  <h4>Fine-Tuning Configuration</h4>
  <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/finetuning preparation (1).png" alt="Fine-Tuning Configuration 1" style="width: 100%; margin-bottom: 10px;"/>
  <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/finetuning preparation (2).png" alt="Fine-Tuning Configuration 2" style="width: 100%;"/>
</div>

---

## Results  

### Fine-Tuning Metrics  
During the fine-tuning process, we monitored the metrics:  

<div style="text-align: center;">
  <h4>Monitoring Fine-Tuning Progress</h4>
  <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/finetuning-gemini1.0/documentation finetuning/dokumentasi monitor finetuning.png" alt="Fine-Tuning Metrics" style="width: 100%;"/>
</div>

---

### Test Results  
The fine-tuned chatbot successfully answered general questions with high relevance in Vertex AI Studio's testing environment.  

<div style="text-align: center;">
  <h4>Chatbot Testing</h4>
  <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/test-finetuning model (1).png" alt="Chatbot Test 1" style="width: 100%; margin-bottom: 10px;"/>
  <img src="Side Quest model (finetuning gemini 1.0 in Vertex AI Studio)/images/test-finetuning model (2).png" alt="Chatbot Test 2" style="width: 100%;"/>
</div>

---

## Deployment  
After completing the fine-tuning, the `chatbot_gizi_model` was handed over to the **Cloud Computing cohort** team to create an endpoint. This endpoint will serve as the backend for chatbot integration into the application.

--- 

# Side Quest 
### ✅ It is recommended to build two models if you want to model using Vertex AI. First Model: Use TensorFlow to build models from scratch (Transfer Learning is allowed).  Second Model: Use Vertex AI for Generative AI use cases.
### ✅ It is highly recommended to create your own or do your own fine tuning when solving Generative AI use cases.