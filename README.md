 💊 Handwritten Prescription Recognition System

This project is a **Deep Learning–based Handwritten Prescription Recognition System** designed to extract and digitize text from handwritten medical prescriptions.  
It combines **EasyOCR** for detecting text regions and a **custom deep learning model** for recognizing handwritten words and characters — automating the process of reading doctors’ handwriting.

---

## 🧠 Overview

The system performs **two main tasks**:
1. **Text Region Detection** – Uses **EasyOCR** to identify areas of interest (handwritten text) within prescription images.  
2. **Text Recognition** – A deep learning model based on **CNN + BiLSTM + CTC** decodes the detected handwriting into digital text.

This hybrid approach improves accuracy and ensures that only relevant text regions are processed for recognition.

---

## 📂 Project Structure

I am  handwritten Dataset format.

---

## ⚙️ Workflow

1. **Data Preparation**  
   - Prescription datasets are divided into characters and words.  
   - Labels are stored in CSV files (`image_labels.csv`, `words_labels.csv`).

2. **Text Detection (EasyOCR)**  
   - EasyOCR detects and crops handwritten text regions from prescription images.

3. **Preprocessing**  
   - Each cropped region is preprocessed: noise removal, thresholding, resizing, normalization.

4. **Model Training**  
   - The CNN-BiLSTM-CTC model learns to recognize characters and words from preprocessed handwriting data.

5. **Recognition & Postprocessing**  
   - Recognized words are combined and formatted into complete digital prescription text.

6. **Evaluation**  
   - The model’s performance is validated on unseen prescription samples.

---

System Pipeline :

       ┌────────────────────────────┐
       │   Handwritten Prescription │
       └──────────────┬─────────────┘
                      │
                      ▼
             [1] EasyOCR Detection
         ─────────────────────────────
         → Detects text regions in an image
         → Crops regions of interest
                      │
                      ▼
        [2] Image Preprocessing (OpenCV)
         ─────────────────────────────
         → Denoising, thresholding, resizing
         → Normalization for model input
                      │
                      ▼
       [3] Recognition Model (CNN + BiLSTM + CTC)
         ─────────────────────────────
         → Learns visual & sequential features
         → Predicts character sequences
                      │
                      ▼
           🧾 Recognized Digital Text Output


## 🧩 Technologies Used

- **Python**
- **TensorFlow / Keras**
- **OpenCV**
- **EasyOCR**
- **NumPy**
- **Matplotlib**
- **Pandas**

---

## 🎯 Objective

To develop an intelligent system capable of **accurately reading and digitizing handwritten medical prescriptions**, assisting healthcare professionals in digital record-keeping and minimizing medication interpretation errors.

---

## 📸 Example (Optional)

> **Input:** Image of a handwritten prescription  
> **Text Detection:** EasyOCR identifies text regions  
> **Output:** `"Paracetamol 500mg twice daily after meal"`

Upload Sample image :

![1](https://github.com/user-attachments/assets/0dd7ea9d-9e2f-48f0-b5a0-8a88d8e40541)
<img width="624" height="498" alt="9" src="https://github.com/user-attachments/assets/67456055-90c0-4840-b0de-f6da6780f8ad" />
<img width="685" height="938" alt="29" src="https://github.com/user-attachments/assets/6b413593-e515-4576-af6e-32613c6c50bf" />


Word and Character Detection :
<img width="1530" height="633" alt="800" src="https://github.com/user-attachments/assets/1210689e-ce3a-44d7-93bc-44f72bcc7587" />
<img width="1541" height="577" alt="Captuqwqwqwqre" src="https://github.com/user-attachments/assets/04179483-552c-4876-be13-c7cda52fc1c7" />
<img width="1534" height="475" alt="Caqwwqwwqpture" src="https://github.com/user-attachments/assets/5a65d273-6303-46a3-ae8e-76d259f882aa" />

Result :
<img width="1107" height="794" alt="Capturqwqwqwe" src="https://github.com/user-attachments/assets/fbafc740-394b-49cb-a985-0bfa5628a111" />
<img width="1102" height="705" alt="Captuqwqwqwqwqre" src="https://github.com/user-attachments/assets/6eeb629d-cab9-4c91-ba76-371508dbc10e" />
<img width="994" height="491" alt="Captqwqwqwure" src="https://github.com/user-attachments/assets/ef6e3b82-c186-4755-b1d2-f0cc1eadc869" />


Result Saving in TXT file :



---

## 🏁 How to Run

1. Clone this repository  
   ```bash
   git clone https://github.com/<Tanvir-Azad-Mahir>/Prescription_Recognition_System.git
   cd Prescription_Recognition_System
   
2 . Install dependencies
3. pip install -r requirements.txt
4. Open and run the notebook
5. Jupyter notebook main.ipynb
Train or test the model using your dataset.

📜 License

This project is open-source and available under the MIT License.

👨‍💻 Author

Developed by Tanvir Azad Mahir
Focused on handwritten text recognition for medical prescription automation.

