# 💊 Handwritten Prescription Recognition System

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

Prescription_Recognition_System/
│
├── Datasets/
│ ├── Character/
│ │ ├── Char_Images/
│ │ └── image_labels.csv
│ │
│ └── Words/
│ ├── word_images/
│ │ ├── word1/
│ │ ├── word2/
│ │ └── ...
│ └── words_labels.csv
│
└── main.ipynb


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

*(You can add a sample input/output image here once available.)*

---

## 🏁 How to Run

1. Clone this repository  
   ```bash
   git clone https://github.com/<Tanvir-Azad-Mahir>/Prescription_Recognition_System.git
   cd Prescription_Recognition_System


