# 🧠 Liver Tumor Segmentation using Deep Learning

## 🔍 Project Title
**Investigation and Development of Machine Learning Model for the Detection of Liver Tumors**

## 📌 Overview
This project focuses on automating the **detection and segmentation of liver tumors** in CT scans using deep learning models like **U-Net** and **ResUNet**. It aims to support radiologists by providing accurate, fast, and consistent segmentation results, reducing manual workload and improving diagnosis efficiency.

---

## 🗂️ Dataset
- **Source**: [LiTS – Liver Tumor Segmentation Challenge](https://competitions.codalab.org/competitions/17094)
- **Format**: 3D CT scan volumes (`.nii` format) with annotated masks for liver and tumors
- **Preprocessing**:
  - Converted 3D volumes to 2D axial slices
  - Applied Hounsfield Unit windowing `[-100, 400]`
  - Normalized and resized to `512x512`

---

## 🧠 Model
- **Architecture**: U-Net (with skip connections)
- **Other Models Used**: ResUNet (for comparison and ensemble)
- **Input**: 512×512 grayscale CT slices
- **Output**: Binary segmentation masks (liver/tumor regions)

---

## 🛠️ Postprocessing
- **Morphological operations** (opening, closing)
- **Connected component analysis** to remove false positives
- **Stacking** 2D slices to reconstruct 3D segmentation

---

## 📈 Evaluation Metrics
- **Dice Coefficient**
- **IoU (Jaccard Index)**
- **Accuracy**
- **Precision & Recall**
- Results are visualized using **bar charts** for better interpretation

---

## 📊 Results
- Achieved around **85–90% accuracy** and **84% Dice score**
- Visual output includes:
  - CT slice
  - Ground truth mask
  - Predicted mask
  - Overlay for comparison

---

## 📦 Libraries & Tools Used
- Python, NumPy, Matplotlib
- PyTorch (for model development)
- OpenCV, scikit-image (for postprocessing)
- scikit-learn (for evaluation metrics)
- Google Colab (for training)


---

## ✅ Future Improvements
- Use 3D U-Net for volumetric segmentation
- Add attention mechanisms (e.g., Attention U-Net)
- Train on diverse datasets for better generalization
- Integrate with clinical platforms for real-world use


---

## 📜 License
This project is for academic and research use only. License terms may depend on LiTS dataset usage rules.

---

## 📬 Contact
Feel free to reach out via GitHub Issues or vvsaikumar1234@gmail.com for questions or collaboration.
