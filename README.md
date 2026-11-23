# Disease Prediction System (Healthcare AI)

Predicts likely diseases from patient symptoms and basic medical record values
using K-Nearest Neighbours (with Random Forest as a benchmark).

## Contents
- `Disease_Prediction_System.ipynb`: the full project (data, normalization, correlation-based
  feature selection, KNN tuning, evaluation, interactive predictor). Outputs are included.
- `disease_prediction_preview.html`: open in any browser for a live, simplified demo.
- `requirements.txt`: Python dependencies.

## Run
    pip install -r requirements.txt
    jupyter lab Disease_Prediction_System.ipynb

Run all cells. Section 7 holds the interactive predictor (`predict_disease(...)`,
`interactive_prompt()` and a widget). Running the notebook also saves `disease_knn_model.joblib`.

## Using real data
The notebook generates a synthetic dataset. To use real data (e.g. Kaggle "Disease Symptom Prediction"),
replace the Step 1 data cell with `df = pd.read_csv("your_file.csv")`, keeping the diagnosis in a
column named `disease`, and update the `SYMPTOMS` / `NUMERIC` lists to match your columns.

## Results (synthetic data)
KNN test accuracy 96.0% (k=11, Manhattan distance); Random Forest 96.4%.

## Disclaimer
Educational project only. Not a medical device and not a substitute for professional diagnosis.
