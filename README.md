# Face Mask Detection

A simple Convolutional Neural Network (CNN) project to detect whether a person is **wearing a mask** or **not wearing a mask** using images. The project is based on a publicly available Kaggle dataset.

##  Main Code

- **`code.ipynb`** → This is the **main notebook**.  
  It contains all steps:  
  1. Loading and preprocessing the dataset (`Train`, `Validation`, `Test`)  
  2. Training the CNN model  
  3. Evaluating the model  
  4. Testing single images  
  5. (Optional) Real-time webcam detection  

> Users should open this notebook first and run all cells sequentially.

## Project Folder Structure

```text
Face-Mask-Detection/
│
├── images/
│
├── model/
│   └── maskDetector.h5
│
├── notebook/
│   └── code.ipynb
│
├── DATASET_README.md
├── README.md
├── .gitignore
└── .gitattributes
```
### Dataset

The dataset is **not included** in this repository because of its size.

Download it from Kaggle:

🔗 https://www.kaggle.com/datasets/ashishjangra27/face-mask-12k-images-dataset
*(Download and unzip the dataset into your project directory.)*

After downloading and extracting it, place the folders as follows:

```text
dataset/
├── Train/
│   ├── with_mask/
│   └── without_mask/
├── Validation/
│   ├── with_mask/
│   └── without_mask/
└── Test/
    ├── with_mask/
    └── without_mask/
```

Refer to `DATASET_README.md` for more details.
## Requirements

- Python 3.x  
- TensorFlow / Keras  
- OpenCV 
- NumPy  
- Matplotlib (optional, for visualizations)  

## Installation

Clone the repo:

```bash
git clone https://github.com/yourusername/Face-Mask-Detection.git
cd Face-Mask-Detection
```
## Usage Instructions

**To run the model:**
- Open `code.ipynb` in Jupyter/VSCode
- Execute all cells in order
- Model trains, evaluates, and saves as `maskDetector.h5`
- Test images directly in notebook

**For webcam detection (optional):**
- Run the webcam section in notebook
- Face detection with OpenCV
- Real-time mask classification
- Green/Red indicators for mask status
- Press 'q' to quit
- 
## CNN Architecture
```text
Input: (256, 256, 3)
│
├── Conv2D (32 filters, 3×3) → ReLU
├── MaxPooling2D (2×2)
│
├── Conv2D (64 filters, 3×3) → ReLU
├── MaxPooling2D (2×2)
│
├── Conv2D (128 filters, 3×3) → ReLU
├── MaxPooling2D (2×2)
│
├── Flatten
├── Dense (128 units) → ReLU
├── Dense (64 units) → ReLU
└── Dense (1 unit) → Sigmoid
```
### 🔧 Training Configuration
- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy
- **Metrics**: Accuracy
- **Epochs**: 20
- **Batch Size**: 32
- **Validation Split**: 20%
---

---
<div align="center">
  
### License
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

###  Author
**Prabin Karki**  
[![GitHub](https://img.shields.io/badge/GitHub-Prabinkarki67-black?style=flat&logo=github)](https://github.com/Prabinkarki67)

</div>

---

*Dataset: [Kaggle - Face Mask Detection](https://www.kaggle.com/datasets/omkargurav/face-mask-detection)*  
*Code: [code.ipynb](code.ipynb) • Model: [maskDetector.h5](maskDetector.h5)*
