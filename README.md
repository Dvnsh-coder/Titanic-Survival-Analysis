# Titanic Survival Analysis and Machine Learning

## Project Objective

The objective of this project is to analyse the Titanic passenger dataset and build machine learning models that predict whether a passenger survived.

## Dataset

The dataset contains information about 891 Titanic passengers.

Important columns include:

- `Survived`: Survival outcome (`0` = Did Not Survive, `1` = Survived)
- `Pclass`: Passenger class
- `Sex`: Passenger gender
- `Age`: Passenger age
- `SibSp`: Number of siblings/spouses aboard
- `Parch`: Number of parents/children aboard
- `Fare`: Ticket fare
- `Embarked`: Boarding port

## Tools and Libraries Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Git and GitHub

## Exploratory Data Analysis

Key findings from the dataset:

- Most passengers were in their 20s and 30s.
- Female passengers had a higher survival rate than male passengers.
- First-class passengers had a higher survival rate than third-class passengers.
- The `Age` column contained missing values.
- The `Cabin` column contained a large number of missing values.
- Passenger gender, passenger class, fare, and family-related features appeared useful for survival prediction.

## Feature Engineering

The following additional features were created:

- `FamilySize`: Total number of family members travelling together, including the passenger.
- `IsAlone`: Indicates whether a passenger travelled alone (`1`) or with family (`0`).

## Data Preprocessing

The following preprocessing steps were applied:

- Split the dataset into training data and testing data.
- Filled missing numerical values using median imputation.
- Filled missing categorical values using the most frequent category.
- Converted categorical columns such as `Sex` and `Embarked` into numerical features using one-hot encoding.
- Used a Scikit-learn preprocessing pipeline to prevent data leakage.

## Machine Learning Models

The following classification models were trained:

1. Logistic Regression
2. Random Forest Classifier
3. Tuned Random Forest Classifier using GridSearchCV and cross-validation

## Model Evaluation

Models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

| Model | Test Accuracy | Survivor Precision | Survivor Recall | Survivor F1-score |
|---|---:|---:|---:|---:|
| Logistic Regression | 80% | 78% | 68% | 72% |
| Baseline Random Forest | 80% | 75% | 72% | 74% |
| Tuned Random Forest | 81% | 80% | 66% | 73% |

## Final Model

The final selected model was **Baseline Random Forest** because it has better survivor recall and better f1-score.

## Limitations

- The dataset is relatively small and represents a historical event.
- Some values, such as passenger age and boarding port, were missing.
- Missing values were imputed using statistical assumptions and may not reflect the true original values.
- Model predictions show associations in the dataset and do not prove causation.
- More advanced feature engineering, such as extracting titles from passenger names, may improve performance.

## How to Run the Project

1. Clone this repository.
2. Install the required Python libraries.
3. Open `titanic_eda.ipynb` in Jupyter Notebook or VS Code.
4. Run the cells from top to bottom.

## Author

Devansh Sharma  
Aspiring Data Scientist