** "Heart Disease Prediction (UCI Dataset)" **

This project uses machine learning to predict the likelihood of heart disease based on patient medical data.


* Two approaches are implemented:

I. Train/Test Split (80/20) → Quick evaluation using Logistic Regression.

II. 5-Fold Cross-Validation → More robust estimate of model performance.


* Dataset

Source: UCI Heart Disease Dataset
Link: https://www.kaggle.com/datasets/redwankarimsony/heart-disease-data/data

- Columns Description:
    - id: (Unique id for each patient)
    - age: (Age of the patient in years)
    - dataset: (place of study)
    - sex: (MaleFemale)
    - cp: chest pain type ([typical angina, atypical angina, non-anginal, asymptomatic])
    - trestbps: resting blood pressure (resting blood pressure (in mm Hg on admission to the hospital))
    - chol: (serum cholesterol in mgdl)
    - fbs: (if fasting blood sugar  120 mgdl)
    - restecg: (resting electrocardiographic results) --> Values [normal, stt abnormality, lv hypertrophy]
    - thalach: maximum heart rate achieved
    - exang: exercise-induced angina (True False)
    - oldpeak: ST depression induced by exercise relative to rest
    - slope: the slope of the peak exercise ST segment
    - ca: number of major vessels (0-3) colored by fluoroscopy
    - thal: [normal; fixed defect; reversible defect]
    - num: the predicted attribute

- Features include:
    age, sex, chest pain type (cp), blood pressure, cholesterol, ECG results, exercise-induced angina, etc.

- Target: Presence (1) or absence (0) of heart disease.


* Methods

I. Logistic Regression as the baseline model.
II. Preprocessing: Handling missing values, encoding categorical features, normalization.
III. Evaluation metrics: Accuracy, Confusion Matrix.
IIII. Cross-validation (5-fold) to assess generalization.


* Results

Train/Test Split (80/20): Accuracy ≈ 82% (higher, but optimistic).

Cross-Validation (5 folds): Mean accuracy ≈ 80% (lower, but more reliable).


* Conclusion: Cross-validation gives a more realistic estimate of performance, while a single split is useful for a quick check.



* Project Structure
```
Heart-Disease-Prediction/
│
├── Data/                                           # dataset
│   ├── heart_disease_uci.csv
│   └── Data Column Descriptions.txt
│
├── notebooks/
│   ├── Heart_Disease_80%20%.ipynb                  # 80/20 split approach
│   └── Heart_Disease_Cross-Validation.ipynb        # CV approach
│
├── models/                                         # saved trained models
│   └── logistic_model_80%20%.pkl
│
├── README.md
├── pyproject.toml                                  # Poetry dependency file
├── poetry.lock
├── How_To_Run.txt
└── .gitignore
```


*** *** How to Run (with Poetry) *** ***
# Clone the repository:
>> git clone https://github.com/arebrahimif/Heart-Disease-Prediction
>> cd Heart-Disease-Prediction

# Install dependencies using Poetry:
>> poetry install

# Activate the virtual environment:
>> poetry shell

# Start JupyterLab:
>> jupyter lab



* Dependencies

Main libraries:
-pandas
-numpy
-scikit-learn
-matplotlib
-seaborn
-jupyterlab
(Managed via Poetry, see pyproject.toml).



* Future Work

    - Add Random Forest / Gradient Boosting models.

    - Perform hyperparameter tuning (GridSearchCV, RandomizedSearchCV).

    - Add feature importance analysis and visualization.

    - Deploy as a web app with Streamlit.



* Author

Project by ARMIN EBRAHIMI
