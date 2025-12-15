# Self-Supervised Learning Playground

This project explores how deep learning models learn visual representations **without labels** and how they behave when exposed to **unseen data distributions**.

---

## 🔍 Motivation

Most ML demos focus on accuracy.
This project focuses on **understanding**.

I wanted to explore:
- What does a self-supervised model actually learn?
- How confident is it when the input distribution changes?
- How can users *interactively* observe this behavior?

---

## 🧠 Approach

1. Train a ResNet-based encoder using **self-supervised contrastive learning**
2. Freeze the encoder and evaluate it using a **linear probe**
3. Build an **interactive inference pipeline** where users can:
   - test CIFAR-10 images
   - upload their own images
   - observe prediction confidence

---

## ⚙️ Technical Stack

- PyTorch
- ResNet-18
- Contrastive Learning (NT-Xent loss)
- CIFAR-10
- UMAP for embedding visualization
- Kaggle Notebook environment

---

## 🧪 Key Observation

- In-distribution images → confident predictions
- Out-of-distribution images → low confidence, unstable predictions

This highlights the **domain gap** problem in real-world ML deployment.

---

## ▶️ How to Run

1. Open the notebook in Kaggle or Jupyter
2. Run all cells sequentially
3. Use the interactive cells to:
   - input an image index
   - upload an image and observe predictions

---

## 📸 Demo

<p align="center">
  <img src="Output Screenshots/cifar_prediction.png" width="400"/>
  <img src="Output Screenshots/real_image_prediction.png" width="400"/>
</p>

---

## 🧩 Limitations

- Trained on CIFAR-10 (32×32 resolution)
- Real-world images may not match training distribution
- Focus is on behavior, not state-of-the-art accuracy

---

## 📌 Takeaway

A good ML system doesn’t just predict — it communicates **uncertainty**.

---

