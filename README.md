# Fuzzy-Driven Kidney Tumor Detection

An AI-assisted research project for classifying kidney CT images into **Cyst, Normal, Stone, and Tumor** classes.

> **Important:** This repository is for academic/research demonstration only. It is not a medical diagnostic device and must not be used to make clinical decisions.

## Project Overview

The project combines image preprocessing, transfer-learning-based feature extraction, and machine-learning classification in a Django web application.

### Pipeline

1. Upload a kidney CT image
2. Preprocess and normalize the image
3. Apply fuzzy-inspired contrast enhancement
4. Extract deep features using two pretrained CNN backbones
5. Fuse the feature representations
6. Train/use SVM, Random Forest and Gradient Boosting classifiers
7. Combine predictions using weighted ensemble logic
8. Display the predicted class and confidence

The project report describes a broader TTN-WEML framework with explainability and MLOps components.

## Technologies

- Python
- Django
- TensorFlow / Keras
- OpenCV
- NumPy / Pandas
- Scikit-learn
- HTML / CSS / JavaScript
- MySQL (optional; SQLite is used by default for easy setup)
- MLflow (optional)

The report identifies Python, Django ORM, HTML, CSS, JavaScript and MySQL as core technologies.

## Repository Structure

```text
kidney-tumor-detection-ai/
├── README.md
├── requirements.txt
├── .gitignore
├── manage.py
├── config/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
├── detector/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   ├── views.py
│   ├── ml_pipeline.py
│   └── migrations/
├── templates/
│   ├── base.html
│   └── detector/
│       ├── home.html
│       └── result.html
├── static/
│   └── css/
│       └── style.css
├── ml/
│   └── README.md
├── models/
│   └── README.md
├── data/
│   └── README.md
└── media/
    └── .gitkeep
```

## Dataset

The source report describes four image classes:

- Cyst
- Normal
- Stone
- Tumor

Do **not** commit private patient data or copyrighted/large datasets to GitHub. Keep datasets outside the repository and follow the dataset's license and anonymization requirements.

## Setup

### 1. Clone

```bash
git clone https://github.com/YOUR_USERNAME/kidney-tumor-detection-ai.git
cd kidney-tumor-detection-ai
```

### 2. Create a virtual environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

Linux/macOS:

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run migrations

```bash
python manage.py migrate
```

### 5. Start the application

```bash
python manage.py runserver
```

Open `http://127.0.0.1:8000/`.

## Training

The web application can run with a demo fallback classifier until trained model artifacts are supplied. See `ml/README.md` for the recommended training workflow.

## Model Artifacts

Large `.h5`, `.keras`, `.pt`, `.pth`, and dataset files should generally not be committed directly. Use Git LFS or a model registry/object store when appropriate.

## Reported Results

The project report states 99.2% accuracy on high-quality images and 98.5% on noisy images. These figures are **reported project results**, not independently reproduced by this repository. Reproduce and document evaluation results before presenting them as experimentally verified.

## Disclaimer

This software is an academic/research prototype. Predictions may be incorrect. It is not intended to diagnose, treat, cure, or prevent any disease.

## Author

**M. Sunil Kumar**

B.Tech – Computer Science and Engineering  
2025–2026
