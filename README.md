# Final-Project-Pengolahan-Sinyal-Group-1-
<div align="center">

# **Breast Cancer Severity Classification and Subtype Prediction from Mammographic Images for Treatment Recommendation**

**Group 1 | Biomedical Signal Processing**

Rufaida Kariemah (2206031561)
Annisa Rahmah (2206032412)
Shofiyah (2206060662)

</div>

---

## **About the Project**

*Breast cancer accounts for approximately 25% of new cancer cases among women worldwide (WHO, 2023). This project develops a cascaded deep learning system based on EfficientNet B0 to:*

1. **Severity Classification**: Using the INbreast dataset (410 DICOM images) to classify based on BI-RADS scores
2. **Molecular Subtype Prediction**: Using a subset of the CMMD2 dataset (2,956 images) to predict 4 subtypes
3. **Therapy Recommendation**: Mapping subtypes to clinical guidelines from NCCN 2023

---

## **Datasets Used**

### **A. INbreast Dataset**

* Type: Full-Field Digital Mammography (FFDM) dataset
* Cases: 115 cases (89 patients)
* Images: 410 DICOM images (`.dcm` format)

**Content/Labels:**

* BI-RADS score annotations (0 to 5)
* Lesion classification: normal, benign, malignant
* Additional information: lesion type (mass, microcalcification, asymmetry, architectural distortion, etc.)
* Optional lesion segmentation annotations (XML format from Mammo Viewer)

**Project Role**: Used in the initial stage to classify malignancy and severity.

---

### **B. CMMD (Chinese Mammography Database)**

* Version: CMMD2
* Images: 2,956 images (from 1,177 patients)
* Type: 2D mammography images (DICOM format)

**Content/Labels:**

* Histopathological diagnosis
* Molecular subtypes of cancer:

  * Luminal A
  * Luminal B
  * HER2-positive
  * Triple-negative
* Patient metadata: age, cancer stage, ER/PR/HER2 status

**Project Role**: Used for predicting molecular subtypes to support personalized therapy recommendations.

---

### **INbreast vs. CMMD2 Comparison**

| **Element**                | **INbreast Dataset**                | **CMMD2 Dataset**                              |
| -------------------------- | ----------------------------------- | ---------------------------------------------- |
| **Image Format**           | DICOM (`.dcm`)                      | DICOM (`.dcm`)                                 |
| **Classification Label**   | BI-RADS, benign/malignant/normal    | Cancer molecular subtypes                      |
| **Additional Annotations** | Optional XML segmentation masks     | Patient metadata (age, ER/PR/HER2 status)      |
| **Image Dimensions**       | High resolution (>3000x4000 pixels) | Medium-to-high resolution (\~2560x3328 pixels) |

