
# Lyra_Leaf_Chlorose

A lightweight CNN trained on scanned leaves of *Hedera helix* (common ivy) to classify between **healthy** and **chlorotic** specimens.  
This project demonstrates how a minimal yet accurate deep learning model can be trained on real-world data collected from a garden environment.

---

## 🌿 Project Summary

This project aims to detect visible chlorosis in leaves of *Hedera helix* using a convolutional neural network (CNN) trained from scratch on a small, well-prepared dataset.  
Leaves were scanned using a flatbed scanner under controlled lighting, and labeled manually based on visual chlorosis symptoms.

---

## 🧠 Key Features

- Classification task: **Healthy** vs **Chlorotic** leaves
- Architecture: 3-layer CNN with dropout and data augmentation
- Accuracy: **100% on validation set** (44 images)
- Input: 128×128 RGB images from scanned real leaves
- Dataset: 80 images for training, 44 for validation
- Perfect confusion matrix: no false positives or false negatives
- Notebook included: ready-to-run on JupyterLab or Colab

---

## 🗂️ Project Structure

```
Lyra_Leaf_Chlorose/
├── dataset_sample/
│   ├── chlorose/
│   └── saine/
│   
├── Lyra_Leaf_Chlorose.ipynb
├── README.md
└── example_output/
    ├── accuracy_plot.png
    ├── confusion_matrix.png
    └── classification_report.txt
```

---

## 🔬 Dataset Details

- Total images: **124**  
- Format: `.png` scanned images (300 DPI)  
- Classes:
  - `saine/` : Healthy leaves
  - `chlorose/` : Visibly chlorotic leaves (yellowing due to iron or nitrogen deficiency)
> 📝 **Note on dataset quality**  
> Unlike PlantVillage, which contains field photos taken under variable conditions (lighting, background, camera type), this dataset uses **flatbed-scanned leaves** under **controlled lighting and uniform background**.  
> This ensures **clarity**, **reproducibility**, and a **high signal-to-noise ratio**, making it particularly suitable for **pedagogical uses, diagnostic accuracy, and scientific reproducibility**.

---

## 🛠️ Model Architecture

- Input: `(128, 128, 3)`
- 3× Conv2D + MaxPooling layers
- Dense(64) + Dropout(0.3)
- Softmax(2) output for binary classification
- Optimizer: Adam
- Loss: Categorical Crossentropy

---

## 📊 Evaluation Results

- **Validation accuracy**: 100%
- **F1-score (both classes)**: 1.00
- **No overfitting** observed (training stopped after 5 epochs)
- Model shows strong generalization on visually distinct data

---

## 📑 Full classification report

👉 See [`example_output/classification_report.txt`](example_output/classification_report.txt)

---

## 🧪 Notes

This project was designed as a pedagogical example and ecological demonstration.  
It is part of a broader initiative to integrate AI into **citizen science**, **plant diagnostics**, and **field ecology**.

---

## 📘 License

MIT License

---

## 🤖 Author

Developed by [Jérôme Frasson](https://github.com/Jerome-openclassroom)  
Contact: jerome.frasson.vsi@gmail.com  

🔗 Related projects:

- [Lyra_Leaf_SPAD_Calibration](https://github.com/Jerome-openclassroom/Lyra_Leaf_SPAD_Calibration) – SPAD sensor calibration for estimating chlorophyll density in leaves.
- [Lyra_LowCost_Soil_Leaf](https://github.com/Jerome-openclassroom/Lyra_LowCost_Soil_Leaf) – Integrated low-cost soil and leaf model for terrestrial primary productivity.
- [TurbiditySensor_OpenScience](https://github.com/Jerome-openclassroom/TurbiditySensor_OpenScience) – Optical-based estimation of aquatic turbidity and primary productivity using open-source sensors.
- [Lyra_DO_Green_Mesurim](https://github.com/Jerome-openclassroom/Lyra_DO_Green_Mesurim) - A low-tech protocol combining MesurimPro and ImageJ to estimate chlorophyll levels from scanned leaves, with validation against SPAD readings and AI-assisted correlation analysis.
- [AI_Assisted_Lake_Ecology](https://github.com/Jerome-openclassroom/AI_Assisted_Lake_Ecology) – A full-scale NPP model combining field measurements, physical modeling, and GPT-4o-assisted ecological interpretation. Includes empirical correction for realistic annual productivity in clear lakes.
- [LimonTree_NPP_Model](https://github.com/Jerome-openclassroom/LimonTree_NPP_Model) — Low-cost water and NPP model for a potted lemon tree.
