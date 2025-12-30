### **Leak-Free Alzheimer MRI Classification + Explainable Genetic Risk Insights**

 A reproducible AI system for **Alzheimer’s dementia stage classification on MRI scans** using a **leak-free data pipeline**, powered by a strong **EfficientNet CNN backbone**, and enhanced with **Grad-CAM spatial attention maps** and **independent genetic risk analysis**, fused only at inference for clinician-aligned explainability.

---

## 🚀 **Features that make this project stand out**

- 🧪 **Zero Data Leakage** → Filename-level dedup + fixed `70/15/15` stratified split
- 🧠 **EfficientNet CNN Backbone** → Robust MRI feature learning
- 🔥 **Grad-CAM Heatmaps (Smooth & Anatomical)** → True spatial attention, no pooling artifacts
- 🧬 **Genetic Risk Inference (Independent Model)** → Odds Ratio + −log10(p-value) scoring
- 🧩 **Late Fusion at Inference Only** → No invalid MRI-genetics joint training
- 📊 **Competition-Grade Metrics** → Accuracy, Macro-F1, AUC (OVR), Confidence Analysis
- 💻 **Kaggle Notebook Compatible** → Cloud GPU support (`cuda:0`)

---

## 🧠 **Grad-CAM Visualization Samples**

| Panel Output | Description |
|---|---|
| **Original MRI → Grad-CAM → Overlay** | Shows exactly where model focuses in the brain |
<img width="501" height="621" alt="image" src="https://github.com/user-attachments/assets/4fea4e02-57f9-43fa-912e-4ebae58aaef4" />
<img width="1115" height="525" alt="image" src="https://github.com/user-attachments/assets/a1c95dd4-7644-41d5-98d1-2057e43b1f4b" />


> These attention maps are extracted from the **last convolutional layer before pooling**, resized smoothly to `224×224`, and inverted before JET colormap for clinician-friendly “hot attention” visuals.

---

## 📊 **Separate Model Performance**

### 🧠 MRI Model Results
<img width="647" height="516" alt="image" src="https://github.com/user-attachments/assets/8560bcd5-2f33-40e5-afe3-a8d063b1d346" />
<img width="643" height="519" alt="image" src="https://github.com/user-attachments/assets/8ab966f5-c12d-43b0-96be-99dd6932aa2d" />


### 🧬 Genetic Model Results (Independent)
<img width="393" height="200" alt="image" src="https://github.com/user-attachments/assets/29ecdc0b-3dc5-4e57-8d07-92795c011a28" />


✔ Both models are **trained and evaluated separately** — **never jointly** to avoid invalid learning or leakage.






