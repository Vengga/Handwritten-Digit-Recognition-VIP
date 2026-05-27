# Handwritten Digit Recognition (VIP Project)

Course: CDS6334 – Visual Information Processing (VIP)  
Project Type: Group Project  
Approach: Classical VIP Techniques (No Deep Learning)

---

##  Project Overview
This project implements a handwritten digit recognition system using
**Visual Information Processing (VIP)** techniques only.

The system supports:
- Single-digit recognition
- Multi-digit recognition (e.g., 5142, 9762)
- Real-time interaction via a Streamlit web application

No deep learning or machine learning classifiers are used.

---

##  Methods Used
- Gaussian smoothing
- Otsu thresholding
- Morphological operations
- Distance transform + watershed segmentation
- MNIST-style normalization
- Prototype template matching (MSE-based)

---

##  Project Structure
vip-digit-recognition/
│
├── app/
│ └── app.py
│
├── notebooks/
│ └── mnist_digit_recognition.ipynb
│
├── results/
│ └── prototypes_K8.npz
│
├── data/
│ └── mnist/
│ ├── train-images.idx3-ubyte
│ ├── train-labels.idx1-ubyte
│ ├── t10k-images.idx3-ubyte
│ └── t10k-labels.idx1-ubyte
│
├── requirements.txt
└── README.md


---

## Dataset
- MNIST handwritten digit dataset (IDX format)
- Source: Kaggle / Yann LeCun MNIST
- Images: 28×28 grayscale

---

## ⚙️ How to Run the Notebook
1. Place MNIST IDX files inside `data/mnist/`
2. Open:
notebooks/mnist_digit_recognition.ipynb

3. Run all cells (Kernel → Restart & Run All)
4. This will generate:
results/prototypes_K8.npz


---

##  How to Run the Web App
From the project root:

```bash
pip install -r requirements.txt
streamlit run app/app.py