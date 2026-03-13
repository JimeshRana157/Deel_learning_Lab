Name:-Jimesh Rana
ID:-202511061
# IT549 Lab 3 – Image-Based AQI Classification

This project is a Jupyter notebook implementation of **image-based Air Quality Index (AQI) classification** using convolutional neural networks (CNNs) and pretrained models (via `torchvision`). It is part of the IT549 Deep Learning course (Lab 3).

## 📌 What it does

- Loads a CSV file (`data.csv`) containing image filenames and AQI class labels
- Loads corresponding images from a folder and prepares PyTorch `Dataset`/`DataLoader`
- Trains a basic CNN from scratch for AQI class prediction
- Includes evaluation utilities (accuracy, confusion matrix, classification report)
- Uses standard preprocessing and augmentation (resize, normalization, flips, color jitter)

## 🗂️ Project structure

- `IT549_Lab3_AQI_Image_Classification.ipynb` – Main notebook containing all code, data preparation, model definition, training, and evaluation.
- `data.csv` – CSV file mapping image filenames to AQI class labels (not included in this repo; see dataset link).
- `sampled_images/` – Image folder used for training, validation, and testing (not included in this repo; see dataset link).

## 📥 Dataset

The dataset is referenced in the notebook, and it includes:
- A CSV file (`data.csv`) with columns like `Filename` and `AQI_Class`
- A directory of images referenced by `Filename`

Dataset link (as referenced in notebook):
- https://drive.google.com/drive/folders/1usBxgNB67GfhCQ2f7xRkDlF6fgIZZrP?usp=sharing

## 🧰 Requirements

This notebook uses Python and the following packages:

- `torch`, `torchvision`
- `numpy`, `pandas`
- `scikit-learn`
- `matplotlib`, `seaborn`
- `Pillow`

You can install them with:

```bash
pip install torch torchvision numpy pandas scikit-learn matplotlib seaborn pillow
```

> ⚠️ The notebook is configured to use CUDA if available. If you do not have a GPU, it will fall back to CPU.

## ▶️ How to run

1. Download the dataset (CSV + images) and update the paths in the notebook to match your local setup.
2. Open `IT549_Lab3_AQI_Image_Classification.ipynb` in Jupyter Lab / Jupyter Notebook.
3. Execute cells sequentially.

### Configuration (in the notebook)

At the top of the notebook, update these paths to match your local environment:

- `DATA_CSV` – path to `data.csv`
- `IMAGES_DIR` – path to the root folder containing the image files

## ✅ Notes

- The notebook uses a fixed random seed (`42`) for reproducibility.
- The model in Task 2 is a simple CNN trained from scratch; you can extend it using pretrained backbones (e.g., ResNet, EfficientNet).

---

Good luck, and enjoy experimenting with AQI image classification! 👩‍💻👨‍💻
