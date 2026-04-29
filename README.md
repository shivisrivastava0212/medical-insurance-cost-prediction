# Medical Insurance Cost Prediction 🏥

A Machine Learning project focused on predicting individual medical insurance costs using **Multiple Linear Regression**. This project demonstrates end-to-end data preprocessing, feature engineering, and model evaluation.

## 🛠 Tech Stack
- **Language:** Python
- **Libraries:** `Pandas`, `Scikit-learn`, `NumPy`, `Matplotlib`/`Seaborn`
- **Environment:** Google Colab

## 📊 Dataset Features
- **Age:** Age of the primary beneficiary.
- **Sex:** Insurance contractor gender (male/female).
- **BMI:** Body Mass Index.
- **Children:** Number of children covered by insurance.
- **Smoker:** Smoking status (Yes/No).
- **Region:** The beneficiary's residential area in the US.
- **Charges:** Individual medical costs (Target Variable).

## 🚀 Key Highlights
- **Data Cleaning:** Handled categorical variables and performed feature scaling for better model performance.
- **Model Building:** Implemented Multiple Linear Regression to establish relationships between health factors and insurance charges.
- **Evaluation:** Used metrics like R-squared and Mean Squared Error (MSE) to determine model accuracy.

## 🛠 How to Run
1. Clone this repository: 
   `git clone https://github.com/shivisrivastava0212/medical-insurance-cost-prediction.git`
2. Open `Multiple_Linear_Regression.ipynb` in Google Colab.
3. Ensure `insurance.csv` is uploaded in the same directory.
4. Run all cells to execute the model and view the evaluation results.

## 📈 Results & Evaluation

The model's performance was evaluated by comparing predicted costs against actual medical charges.

- **R-squared Score:** `0.7836` 
  - This indicates that approximately 78.4% of the variance in medical charges is explained by the model's features (age, BMI, smoker status, etc.).
- **Mean Squared Error(MSE):** 33596915.85136145
- **Status:** Training Complete & Validated.

## 📊 Actual vs. Predicted Charges
The plot below visualizes the model's accuracy, where points closer to the red dashed line represent more accurate predictions:

![Actual vs Predicted Charges](results_plot.png)

## 🔍 Key Insights & Analysis
Beyond the numbers, the model provides significant insights into the factors driving medical insurance costs:

* **Primary Drivers:** Analysis of the model coefficients confirms that **Smoker Status**, **Age**, and **BMI** have the highest positive correlation with medical charges.
* **The "Smoker" Effect:** Being a smoker is the single most significant predictor, leading to a substantial increase in predicted insurance premiums.
* **Data Transformation:** Categorical variables (Sex, Smoker, Region) were handled using **One-Hot Encoding** to ensure the Linear Regression model could process the non-numeric data effectively.

## 📂 Dataset Information
* **Source:** [Medical Cost Personal Datasets (Kaggle)](https://www.kaggle.com/datasets/mirichoi0218/insurance)
* **Description:** The dataset contains 1,338 records of beneficiary data, including health habits and demographic information.

## 💾 Model Artifacts
- **insurance_model.pkl:** Serialized file containing the best model weights for direct deployment.

- **insurance.csv:** The dataset used for training and testing.

## 💡 Future Improvements
* **Feature Engineering:** Implementing Polynomial features to capture non-linear trends.
* **Hyperparameter Tuning:** Using `GridSearchCV` to optimize the regression coefficients.
* **Advanced Modeling:** Testing Gradient Boosting algorithms (XGBoost) for potentially higher accuracy.
## 🚀 Deployment & Usage
This model is serialized for production use. You can load the trained model without re-training:

1. **Model Saving:** The model is saved using `joblib` as `insurance_model.pkl`.
2. **Loading the Model:**
   ```python
   import joblib
   model = joblib.load('insurance_model.pkl')
   # Now you can use model.predict(new_data)

---
*Created for learning and professional development.*
