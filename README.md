# 🧠 Brain Tumor Classifier using CNN and Gradio

This project is a **Brain Tumor Classifier** built with TensorFlow/Keras and deployed using Gradio. The model classifies brain MRI scans into four categories: **glioma**, **meningioma**, **no tumor**, and **pituitary**.

## 🚀 Features
- CNN-based image classification.
- Trained on a labeled dataset from Google Drive.
- Deployed with an easy-to-use Gradio web interface.

---

## 🗂️ Dataset Structure

Dataset should be organized in your Google Drive as follows:

Brain Tumor Segmentation/
└── Training/
├── glioma/
├── meningioma/
├── notumor/
└── pituitary/

yaml
Copy
Edit

Each subfolder contains the respective tumor-type images.

---

## 🛠️ Setup and Dependencies

Run the following in Google Colab:

```bash
pip install gradio opencv-python-headless
📌 Steps Performed in the Code
Mount Google Drive:

python
Copy
Edit
from google.colab import drive
drive.mount('/content/drive')
Load and Resize Images:

Images are loaded from each category folder.

Resized to 128x128 pixels.

Normalized to range [0, 1].

Preprocess Labels:

Labels are one-hot encoded using LabelBinarizer.

Split Dataset:

Train-test split using train_test_split.

Build CNN Model:

Convolutional layers with Batch Normalization and Pooling.

Global Average Pooling and Dense layers with Dropout.

softmax activation for multi-class classification.

Train Model:

Trained for 10 epochs with validation split.

Gradio Interface:

A simple web UI for image upload and prediction display.

Returns the most probable tumor class.

🧪 Sample Usage
Once run, a web interface will be launched:

Upload an image (MRI scan).

The model will return the predicted tumor class (e.g., meningioma).

🎓 Requirements
Python 3.x

TensorFlow (>=2.0)

Gradio

OpenCV

NumPy

scikit-learn

📈 Future Improvements
Save and load trained models for reuse.

Add evaluation metrics like confusion matrix.

Use transfer learning for improved accuracy.

🧠 Author
Developed using Keras & Gradio

Run on Google Colab

yaml
Copy
Edit

