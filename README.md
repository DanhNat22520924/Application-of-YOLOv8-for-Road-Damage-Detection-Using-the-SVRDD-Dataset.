# Application of YOLOv8 for Road Damage Detection  
### Using the SVRDD Dataset

## 1. Project Overview
This project applies the **YOLOv8n (Nano)** object detection model to automatically detect and classify **road surface damages** such as cracks and potholes. The system is designed to be **lightweight, efficient**, and suitable for **edge-device deployment**, enabling real-world road monitoring applications.

**Key objectives:**
- Detect road damages with high accuracy
- Maintain low computational cost
- Support deployment on embedded and edge devices

**Model:** YOLOv8n (Ultralytics)  
**Dataset:** SVRDD (Surface Vehicular Road Damage Dataset)

---

## 2. Dataset
- **Name:** SVRDD – Surface Vehicular Road Damage Dataset  
- **Link:** https://zenodo.org/records/10100129  
- **Description:** A specialized dataset containing annotated images of various road surface damages captured in real-world conditions.

⚠️ The test set is not publicly distributed. Please contact the authors for access.

---

## 3. Installation
Clone the repository and install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## 4. Project Structure
The repository is organized as follows (dataset structure may vary slightly):

```
Road-Surface-Damage-Detection/
├── dataset/
│   ├── images/
│   │   ├── train/
│   │   ├── val/
│   │   └── test/
│   └── labels/
│       ├── train/
│       ├── val/
│       └── test/
├── requirements.txt
├── DoAnEmbeddedAI.ipynb      # Training notebook
├── ChayMoHinh.ipynb         # Inference & demo notebook
└── README.md
```

---

## 5. Usage

### 5.1 Training
Use the training notebook to train YOLOv8 on the SVRDD dataset:

```text
DoAnEmbeddedAI.ipynb
```

This notebook includes:
- Dataset loading and configuration
- YOLOv8n model training
- Evaluation metrics calculation

---

### 5.2 Inference
Run inference using the trained model with:

```text
ChayMoHinh.ipynb
```

The notebook supports:
- Loading trained weights
- Running predictions on test images
- Visualizing detection results

---

## 6. Demo Results
Below are example outputs from the trained YOLOv8n model on SVRDD test images.

Each bounding box represents a detected road damage type with its corresponding confidence score.

---

## 7. Performance
After training, the model achieved the following results:

- **mAP@0.5:** 0.311  
- **mAP@0.5:0.95:** 0.19  

These results indicate that the model is capable of effective localization and classification of road surface damages.

**Note:**  
Performance may vary depending on training epochs, learning rate, batch size, and dataset configuration.

---

## 8. Future Work
- **Model optimization:** Apply quantization techniques (e.g., INT8) to improve inference speed on edge devices.
- **Dataset enhancement:** Incorporate additional datasets to improve generalization.
- **Embedded deployment:** Deploy the model on platforms such as **Raspberry Pi** or **Jetson Nano** for real-time road damage detection.

---

## 9. Authors
**Nguyễn Hoàng Nam**  
**Danh Nat**

📧 **Email:**  
- ng.h.nam0802@gmail.com  
- danhnatit@gmail.com  

🔗 **LinkedIn:**  
- https://www.linkedin.com/in/nghnam0802

