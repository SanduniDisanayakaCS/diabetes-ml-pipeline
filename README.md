# 🧠 Diabetes Risk Prediction with AWS SageMaker

This project implements a complete machine learning pipeline for predicting diabetes using the [Pima Indians Diabetes Dataset](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database). The model is trained, evaluated, and deployed on **AWS SageMaker**, demonstrating an end-to-end ML workflow in the cloud.

![AWS SageMaker](https://img.shields.io/badge/Built%20with-AWS%20SageMaker-orange?logo=amazon-aws)
![ML Model](https://img.shields.io/badge/Model-XGBoost-blueviolet?logo=python)
![Status](https://img.shields.io/badge/Deployment-Done-green?style=flat-square)

---

## 🔬 Features

✅ Upload dataset to Amazon S3  
✅ Train ML model using SageMaker’s built-in **XGBoost**  
✅ Deploy real-time inference endpoint  
✅ Predict diabetes risk from live data  
✅ Clean up endpoint to avoid AWS charges

---

## 📂 Project Structure

diabetes-ml-pipeline/
├── train_diabetes_model.ipynb # Full Jupyter notebook pipeline
├── diabetes.csv # (Optional) Raw dataset
├── README.md # This file
└── requirements.txt # (Optional) Notebook dependencies


---

## 🧪 Technologies Used

| Component       | Tool / Service              |
|----------------|-----------------------------|
| Model          | XGBoost (binary:logistic)   |
| Platform       | AWS SageMaker               |
| Storage        | Amazon S3                   |
| Interface      | Jupyter Notebook            |
| Language       | Python                      |

---

## 🚀 Quickstart (on SageMaker)

1. Launch SageMaker Studio or Notebook Instance
2. Upload `train_diabetes_model.ipynb`
3. Upload `diabetes.csv` to S3
4. Run the notebook:
   - Upload data
   - Train model
   - Deploy endpoint
   - Predict
   - Clean up endpoint

---

## 📊 Sample Prediction Output

Prediction Result: 0.0030 (Low diabetes risk)


---

## 🧹 Cleanup

To avoid AWS charges, always run this after testing:

```python
predictor.delete_endpoint()
