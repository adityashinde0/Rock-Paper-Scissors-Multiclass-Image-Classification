# ✊✋✌️ Rock Paper Scissors — Multiclass Image Classification

A Convolutional Neural Network (CNN) built with TensorFlow/Keras that classifies hand gesture images into three categories: **Rock**, **Paper**, and **Scissors**. The model achieves **100% accuracy** on the validation set after 25 epochs of training.

---

## 📌 Project Overview

| Detail | Info |
|---|---|
| Task | Multiclass Image Classification |
| Classes | Rock, Paper, Scissors |
| Framework | TensorFlow / Keras |
| Input Size | 150 × 150 × 3 (RGB) |
| Training Images | 2,520 |
| Validation Images | 372 |
| Final Val Accuracy | 100% |

---

## 🧠 Model Architecture

The model is a Sequential CNN with the following layers:

```
Conv2D(64, 3×3, relu) → MaxPooling2D(2×2)
Conv2D(64, 3×3, relu) → MaxPooling2D(2×2)
Conv2D(128, 3×3, relu) → MaxPooling2D(2×2)
Conv2D(128, 3×3, relu) → MaxPooling2D(2×2)
Flatten
Dense(512, relu)
Dense(3, softmax)
```

- **Loss:** Sparse Categorical Crossentropy  
- **Optimizer:** RMSprop  
- **Epochs:** 25

---

## 📂 Project Structure

```
rock-paper-scissors-cnn/
│
├── Multiclass_Classification.ipynb   # Main notebook (training + prediction)
├── rps_model.keras                   # Saved trained model (if included)
├── requirements.txt                  # Python dependencies
├── .gitignore                        # Files excluded from version control
└── README.md                         # Project documentation
```

> **Note:** The dataset folders (`rps/`, `rps-test-set/`) and zip files are downloaded automatically inside the notebook and are excluded from the repository via `.gitignore`.

---

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/rock-paper-scissors-cnn.git
cd rock-paper-scissors-cnn
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Notebook
Open `Multiclass_Classification.ipynb` in Jupyter and run all cells. The dataset will be downloaded automatically from Google's public storage.

### 4. Predict on Your Own Image
Replace `Mtest.jpg` with your own hand gesture image and run the prediction cell:
```python
fn = 'your_image.jpg'
```

---

## 📊 Training Results

The model converges quickly and reaches perfect accuracy:

| Epoch | Train Accuracy | Val Accuracy |
|-------|---------------|-------------|
| 1     | 98.73%        | 100%        |
| 2+    | 100%          | 100%        |

---

## 📦 Requirements

- Python 3.10+
- TensorFlow 2.x
- NumPy
- Keras (included with TensorFlow)

Install all with:
```bash
pip install tensorflow numpy
```

---

## 📁 Dataset

The dataset is sourced from [TensorFlow's public datasets](https://storage.googleapis.com/learning-datasets/):
- `rps.zip` — Training set (Rock, Paper, Scissors images)
- `rps-test-set.zip` — Validation set

The notebook downloads and extracts these automatically. **Do not upload the dataset to GitHub.**

---

## 💾 Saved Model

The trained model is saved as `rps_model.keras` and can be reloaded with:
```python
from tensorflow.keras.models import load_model
model = load_model('rps_model.keras')
```

> **Note:** The `.keras` model file can be large. Consider using [Git LFS](https://git-lfs.com/) if you want to include it in your repository.

---

## 🙋 Author

**Your Name**  
[GitHub](https://github.com/adityashinde0) ·
