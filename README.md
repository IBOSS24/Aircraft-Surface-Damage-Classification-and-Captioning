# ✈️ Aircraft Surface Damage Classification and Captioning

This project combines **deep learning for image classification** and **vision-language modeling** to identify and describe aircraft surface damage such as **dents** and **cracks**.  
It leverages **VGG16** (a pretrained CNN model) for damage detection and **BLIP Transformer** for automatic image captioning and summarization.

---

## 🚀 Project Overview

The aviation industry requires quick and accurate detection of surface damage to ensure flight safety and reduce downtime.  
This project demonstrates how AI can automate damage assessment by:

1. **Classifying aircraft surface images** as either:
   - `Dent`
   - `Crack`

2. **Generating descriptive captions** and a **summary** using a pretrained BLIP transformer model.

---
## 🛠️ Installation  

### **Prerequisites**  

Before setting up the project, ensure you have the following installed on your system:  

- **Python 3.8+**  
- **TensorFlow 2.17.1**  
- **CUDA** *(optional, for GPU acceleration)*  
- **pip** (Python package manager)  

You can verify your Python version with:  
```bash
python --version
```

---

### **Setup**  

#### 1️⃣ Clone the repository  
```bash
git clone https://github.com/yourusername/aircraft-damage-classification.git
cd aircraft-damage-classification
```

#### 2️⃣ Install dependencies  
```bash
pip install -r requirements.txt
```

> 💡 *Tip: If you’re using GPU acceleration, make sure your TensorFlow and CUDA versions are compatible. Refer to the official [TensorFlow GPU support guide](https://www.tensorflow.org/install/gpu).*  

---
## 💾 Dataset  

> ⚠️ Dataset not included in the repository due to size restrictions.  
You can structure your dataset as follows:
```
aircraft_damage_dataset_v1/
  ├── train/
  │   ├── dent/
  │   └── crack/
  ├── valid/
  │   ├── dent/
  │   └── crack/
  └── test/
      ├── dent/
      └── crack/

```
---
## 🧠 Methodology

### 1. **Data Preprocessing**
- Images of aircraft surfaces are resized and normalized.
- Labels are encoded into categorical form.
- Data augmentation techniques (rotation, flipping, etc.) improve model generalization.

### 2. **Feature Extraction with VGG16**
- A pretrained **VGG16** network (from ImageNet) is used as a **feature extractor**.
- The final fully-connected layers are replaced with a custom classifier to distinguish between “Dent” and “Crack”.

### 3. **Training and Evaluation**
- The model is trained using transfer learning to minimize computational cost.
- Evaluation metrics include **accuracy**, **precision**, **recall**, and **confusion matrix** visualization.

### 4. **Caption and Summary Generation**
- A **BLIP Transformer** (Bootstrapped Language Image Pretraining) is used to generate:
  - A **caption** describing the detected aircraft image.
  - A **summary** that contextualizes the visual content.

---

## 🧩 Technologies Used

| Category | Tools |
|-----------|--------|
| Programming | Python, Jupyter Notebook |
| Deep Learning | TensorFlow / Keras |
| Vision Models | VGG16 (Pretrained on ImageNet) |
| Vision-Language Model | BLIP Transformer |
| Visualization | Matplotlib, Seaborn |
| Data Handling | NumPy, Pandas |

---

## 📊 Results

- Achieved high accuracy in detecting **dents** vs **cracks**.
- Generated meaningful captions describing aircraft components and visible damage.
- Created concise summaries integrating both classification and captioning insights.

---

## 🖼️ Example Output

Below is an example of the model’s output on an aircraft image:

![Aircraft Damage Example](https://github.com/IBOSS24/Aircraft-Surface-Damage-Classification-and-Captioning/blob/main/image/Dent-predicted%20.png)

**Prediction:** Dent  
**Caption:** "A close-up view of an aircraft wing with visible dent damage."  
**Summary:** "this is a detailed photo showing the damage of the nose of a b - 17 bomber, requiring inspection."

---

## 📈 Model Performance

### **Classification Results**
- **Training Accuracy:** ~95%  
- **Validation Accuracy:** ~93%  
- **Test Accuracy:** ~91%

### **Training Configuration**
- **Epochs:** 5  
- **Batch Size:** 32  
- **Learning Rate:** 0.0001  
- **Optimizer:** Adam  
- **Loss Function:** Binary Crossentropy

---

## 🔬 Technical Highlights

### **Transfer Learning Approach**
- **Frozen Base Model:** VGG16 layers remain frozen to preserve learned ImageNet features  
- **Custom Classifier:** Two fully-connected layers with dropout for regularization  
- **Feature Extraction:** Leverages deep convolutional features without retraining  

### **Data Preprocessing**
- **Image Augmentation:** Rescaling pixel values to [0, 1] range  
- **Batch Processing:** Efficient data loading with `ImageDataGenerator`  
- **Consistent Sizing:** All images resized to 224×224 pixels  

### **Custom Keras Layer**
- **BLIP Integration:** Custom layer wrapping the transformer model  
- **Task Flexibility:** Single layer handles both captioning and summarization  
- **TensorFlow Compatible:** Seamless integration with Keras pipelines  

---

## 🎓 Learning Outcomes

This project demonstrates proficiency in:

✅ Transfer learning with pretrained CNNs  
✅ Binary classification for computer vision tasks  
✅ Model evaluation and visualization  
✅ Transformer-based image captioning  
✅ Custom Keras layer implementation  
✅ Production-ready ML pipeline development  

---

## 🔮 Future Enhancements
- Multi-class classification (more damage types)  
- Object detection for damage localization  
- Mobile deployment (TensorFlow Lite)  
- Real-time video processing  
- Damage severity estimation  
- Integration with aircraft maintenance systems  

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---
## 📝 License

This project is licensed under the CC BY 4.0 License — see the LICENSE file for details.
Dataset provided by Roboflow under CC BY 4.0.

---

## 🙏 Acknowledgments

VGG16: Simonyan & Zisserman (2014)

BLIP: Li et al., Salesforce Research (2022)

Dataset: Roboflow Community

Framework: TensorFlow / Keras Team

---
## 📧 Contact

- **Email**: [med.marin17@gmail.com](med.marin17.ad@gmail.com)
- **LinkedIn**: [linkedin.com/Mohammed](https://www.linkedin.com/in/mohammed-e-a13664182/)
