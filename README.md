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

## 🖼️ Example Output

Below is an example of the model’s output on an aircraft image:

![Aircraft Damage Example](image/Dent-predicted.png)

**Prediction:** Dent  
**Caption:** "A close-up view of an aircraft wing with visible dent damage."  
**Summary:** "this is a detailed photo showing the damage of the nose of a b - 17 bomber, requiring inspection."

