# Student Performance Analysis and Prediction

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Version](https://img.shields.io/badge/version-1.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## Objective
This project aims to understand how students' performance (test scores) is affected by various factors such as gender, ethnicity, parental level of education, lunch, and test preparation courses.

## Data Collection
- **Dataset Source:** [Kaggle - Student Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?datasetId=74977)
- **Data Size:** 8 columns and 1000 rows.

### Dataset Information
- `gender`: Sex of students (Male/Female)
- `race/ethnicity`: Ethnicity of students (Group A, B, C, D, E)
- `parental level of education`: Parents' final education (bachelor's degree, some college, master's degree, associate's degree, high school)
- `lunch`: Having lunch before the test (standard or free/reduced)
- `test preparation course`: Completion of the test preparation course (complete or not complete)
- `math score`
- `reading score`
- `writing score`

## Process Followed
I have followed a modular approach to solving the problem. The process includes:

### Basic Files Configurations
1. **Setup File:** Initializes all the required packages to be imported.
2. **Logger:** Generates logs during model execution for better process understanding and maintenance.
3. **Exception Handling:** Generates custom exceptions when needed.

### Project Structure
The project is structured into the following modules:
- **data_ingestion.py:** Acquires data from `stud.csv`, splits it into train-test sets, and saves the files in artifacts.
- **data_transformation.py:** Transforms the data using preprocessing techniques (OneHotEncoder, StandardScaler).
- **model_trainer.py:** Loads and transforms data, trains the model using different algorithms, and evaluates them based on the r2 score.

## Exploratory Data Analysis
### Conclusions
- Student performance is related to lunch, race, and parental level of education.
- Females lead in pass percentage and are also top-scorers.
- Student performance is not significantly related to the test preparation course.
- Completing the preparation course is beneficial.

## Model Training
Trained models include:
- Random Forest
- Decision Tree
- Gradient Boosting
- Linear Regression
- XGBRegressor
- CatBoosting Regressor 
- AdaBoost Regressor

Fine-tuning of models was performed using Grid Search CV.

## Deployment
For deployment:
- Created `.ebextensions` file for setup configuration.
- Deployed in AWS Elastic Beanstalk.
- Created a pipeline in AWS connected to the GitHub repository.

## Tools Used
- Numpy 
- Pandas
- Seaborn
- Matplotlib
- Scikit-learn
- Catboost
- Xgboost
- Dill
- Flask

---

Feel free to reach out for any questions or contributions!

![License](https://img.shields.io/badge/license-MIT-green)
