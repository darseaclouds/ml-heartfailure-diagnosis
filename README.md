# ml-heartfailure-diagnosis
# Heart Failure Prediction from Chest X-Ray Embeddings

**Tools Used:**  
`TensorFlow` · `scikit-learn` · `Google Cloud Platform (GCP)`

---

## 📝 Introduction

**Abstract:**  
Heart failure is a major public health challenge with growing costs. Ejection fraction (EF) is a key metric for the diagnosis and management of heart failure. However, estimating EF using echocardiography is expensive and requires extensive expertise. An existing deep learning model is able to identify EF from chest x-rays, which are quick, inexpensive, and require less expertise. However, this model requires enormous computational resources to train and has inequitable performance across race.

This project introduces a model that distinguishes EF in chest x-rays using image embeddings from the MIMIC dataset. Compared to the existing model trained for the same task on raw images, the proposed model performs similarly while significantly reducing the computational resources needed for training and updating. Upon further model analysis based on race, gender, and insurance, the proposed embedding model shows performance disparities that correlate with representation in the dataset. A final discussion on bias in clinical settings contextualizes the model within the broader American healthcare system.

> ⚠️ **Important Notice:**  
Due to HIPAA regulations and the sensitive nature of the data used, the full codebase and raw datasets for this project cannot be shared publicly. The dataset used is **“Generalized Image Embeddings for the MIMIC Chest X-Ray”**, which requires credentialed access and human subjects training through PhysioNet. Please refer to the final paper in `final-paper.pdf` for full results, methodology, and discussion.

---

## 📂 Repository Contents

This repository includes **Jupyter notebooks**, supporting **presentation slides**, and **related papers** that detail the development process and theoretical background.

### 🔍 Jupyter Notebooks

1. **`chest-playground.ipynb`**  
   _Initial Exploration_  
   Conducts exploratory data analysis on the image embeddings. Includes PCA decomposition and visualization of feature space.

2. **`data-pre.ipynb`**  
   _Preprocessing Round 1_  
   Performs initial data cleaning and formatting. Embeddings are processed, and demographic variables (race, gender, insurance) are extracted for later fairness analysis.

3. **`data-HF.ipynb`**  
   _Data Preparation for Modeling_  
   Structures and balances the dataset for the EF classification task. Handles training/test splits and ensures alignment of labels with embeddings.

4. **`model-HF.ipynb`**  
   _Model Training_  
   Trains a resource-efficient deep learning model to classify heart failure from x-ray embeddings. Includes performance metrics and fairness diagnostics. See `final-paper.pdf` for full training pipeline and results.

---

## 📄 Additional Materials

- **`presentation-slides.pdf`**  
  Slides used for presenting the project, including motivation, methodology, model architecture, results, and ethical considerations.

- **`final-paper.pdf`**  
  Full research paper containing background, implementation details, evaluation metrics, and an in-depth discussion of model bias in healthcare.

- **`embeddings-creation.pdf`** & **`supercon.pdf`**  
  Supporting literature used to understand the embedding creation methodology and theoretical foundation of the model's design.

---

## 📬 Questions & Contact

This work was completed as part of a research project. For academic inquiries or collaborations, please feel free to reach out via the contact information listed in the final paper.
