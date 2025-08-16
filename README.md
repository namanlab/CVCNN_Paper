# Phase-Aware Deep Learning with Complex-Valued CNNs for Audio Signal Applications

This repository contains the implementation for the experiments described in the paper:  
**Phase-Aware Deep Learning with Complex-Valued CNNs for Audio Signal Applications**  

It includes code, datasets, and notebooks for:  
- **Experiment 1** – Baseline image classification on MNIST, KMNIST, and Fashion-MNIST  
- **Experiment 2** – Audio signal classification with MFCCs (Binary & Multi-class)  
- **Experiment 3** – Phase-aware Graph Neural Network (GNN) audio experiments  

---

## 📂 Repository Structure

```
.
├── data/                     # All dataset folders and preprocessed features
│   ├── FashionMNIST/raw/
│   ├── KMNIST/raw/
│   ├── MNIST/raw/
│   ├── music_genre_binary_data/
│   ├── music_genre_multiclass_data/
│
├── results/                  # Saved experimental outputs (plots, logs, metrics)
│
├── EXP1_MNIST.ipynb           # Experiment 1 – MNIST
├── EXP1_KMNIST.ipynb          # Experiment 1 – KMNIST
├── EXP1_FMNIST.ipynb          # Experiment 1 – Fashion-MNIST
├── EXP2_3_Binary_MusicGenre.ipynb   # Experiments 2 and 3 – Binary genre classification
├── EXP2_3_Multi_MusicGenre.ipynb    # Experiments 2 and 3 – Multi-class genre classification
├── requirements.txt           # Python dependencies
├── LICENSE
└── README.md
```

---

## ⚙️ System & Environment Details

All experiments were conducted locally on a:

- **Machine:** MacBook Pro (Model MPHE3HN/A)  
- **OS:** macOS 14.5 (Sonoma)  
- **Chip:** Apple M2 Pro (10 cores: 6 performance + 4 efficiency)  
- **RAM:** 16 GB unified memory  
- **Python:** 3.11  
- **Backend:** PyTorch with Metal acceleration for Apple Silicon  

**Training was CPU-based**, leveraging Apple Silicon's accelerated linear algebra operations.

---

## 📦 Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

###  2️⃣ Create a virtual environment (recommended)

```bash
python3.11 -m venv env
source env/bin/activate   # On macOS / Linux
env\Scripts\activate      # On Windows
```

###  3️⃣ Install dependencies

```bash
pip install --upgrade pip
pip install -r requirements.txt
```

---

## 📜 Requirements

`requirements.txt` includes:

```
torch
torchvision
complexPyTorch
matplotlib
seaborn
numpy
json5
librosa
scipy
pathlib
scikit-learn
```

---

## 🚀 Running Experiments

### **Experiment 1: Image Classification with CVCNNs**

Run any of the three notebooks for MNIST, KMNIST, or Fashion-MNIST:

```bash
jupyter notebook EXP1_MNIST.ipynb
jupyter notebook EXP1_KMNIST.ipynb
jupyter notebook EXP1_FMNIST.ipynb
```

### **Experiments 2 & 3: Audio Genre Classification & Phase-Aware GNNs**

These notebooks contain both:

- Experiment 2 – MFCC-based CNN classification (Binary & Multi-class). 
- Experiment 3 – Phase-aware GNN classification. 

Binary Genre Classification (Rock vs Classical):

```bash
jupyter notebook EXP2_3_Binary_MusicGenre.ipynb
```

Multi-class Genre Classification:

```bash
jupyter notebook EXP2_3_Multi_MusicGenre.ipynb
```



## 🎯 Notes
- All datasets are stored in the `data/` directory.  
- Audio feature extraction uses **Librosa**; MFCC workflows are detailed in the paper.  

---

## 📄 License
This project is licensed under the terms of the **MIT License**. See the [LICENSE](LICENSE) file for details.

