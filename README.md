# Villa Pool Image Classifier

This repository contains a Jupyter notebook (`Pool_Detector.ipynb`) that implements a model to **detect whether a villa image contains a swimming pool or not**. The problem was part of the **“استخرمون نشه؟ (Let it not be our pool?)”** problemset in the Quera Technology Olympic. :contentReference[oaicite:0]{index=0}

---

## 🧠 Project Overview

When evaluating vacation lodging listings (e.g. villas, resorts), one desirable feature is the presence of a swimming pool. The goal of this project is to build a pipeline that — given one or more images of a villa — predicts whether a pool is present.

Key points:

- Input images are **not** satellite / overhead images, but normal villa photos (exteriors, angles, pool-level shots).  
- Combination of **image processing / computer vision techniques** + **deep neural network** (using Keras / TensorFlow).  
- The model is evaluated using **weighted F1 score** (minimum threshold: 0.4) per the problem specification. :contentReference[oaicite:1]{index=1}  
- This is a challenge / competition-style problem, so the notebook includes experiments, preprocessing steps, training, evaluation, and inference code.

---

## Features & Methods

Here’s a summary of what’s implemented in the notebook:

- **Data preprocessing & augmentation** (resizing, normalization, flips, color augmentations)  
- **Classical image-processing / CV heuristics** (optional or hybrid steps)  
- **Deep neural network (CNN)** built using **Keras / TensorFlow**  
- Training loops, validation, metrics (precision, recall, F1)  
- Inference and producing a `result.zip` for submission  
- (Optional) Ablation or comparison of simpler CV vs deep models  
- Clear modular code structure so you can replace parts (e.g. change architecture)

---

## Setup & Usage

### Requirements

You should have Python 3 (>= 3.7) and the following libraries installed (you can use a `requirements.txt` or `pip install`):

- tensorflow  
- keras  
- numpy  
- matplotlib  
- scikit-image / OpenCV (cv2)  
- scikit-learn  
- pandas  

### Running the Notebook

1. Clone this repository  
2. Install dependencies  
3. Open `Pool_Detector.ipynb` in Jupyter / JupyterLab / Google Colab  
4. Follow the cells in order: data loading → preprocessing → model training → evaluation → inference  
5. At the end, run the result-producing cell so that `result.zip` is generated (as required by the original problem).  

### Tips & Cards

- You may want to enable GPU acceleration (if available) for training speed  
- Use early stopping, learning-rate scheduling, or model checkpoints for better performance  
- Visualize misclassified examples to help debug tricky cases  
- Experiment with architectures or adding attention / segmentation modules

---

> *Note: Your actual results may vary depending on data splits, hyperparameters, and augmentations.*

You can also include sample images: one with correct detection, one with false positive/negative, etc.

---

## Project Structure

