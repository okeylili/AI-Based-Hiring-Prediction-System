# AI-Based Hiring Prediction System

## Project Overview
This project builds an end-to-end Machine Learning model to predict whether a candidate will be:
- Hired (1)
- Rejected (0)

based on resume features such as skills, experience, education, certifications, projects, and salary expectations.

The system simulates a real-world AI resume screening tool used in HR analytics.

------------------------------------------------------------

## Dataset Description
The dataset contains 1000+ synthetic resumes with the following columns:

- Resume_ID (Dropped)
- Name (Dropped)
- Skills
- Experience (Years)
- Education
- Certifications
- Job Role
- Recruiter Decision (Target Variable)
- Salary Expectation ($)
- Projects Count
- AI Score (Not used to avoid data leakage)

Target Encoding:
- Hire   -> 1
- Reject -> 0

------------------------------------------------------------

## Project Workflow

1. Data Loading & Inspection
   - Checked shape, column names, data types
   - Analyzed missing values
   - Reviewed summary statistics

2. Data Cleaning
   - Dropped Resume_ID and Name
   - Converted Recruiter Decision to binary (0/1)
   - Handled missing values

3. Text Feature Engineering
   - Combined Skills, Certifications, and Job Role
   - Cleaned text (lowercase, removed special characters, trimmed spaces)
   - Applied TF-IDF Vectorization

4. Categorical Encoding
   - Encoded Education using Label Encoding / One-Hot Encoding

5. Feature Scaling
   - Applied StandardScaler to:
     - Experience (Years)
     - Salary Expectation
     - Projects Count

6. Train-Test Split
   - 80% Training
   - 20% Testing
   - random_state = 42

------------------------------------------------------------

## Models Implemented

- Logistic Regression
- Random Forest
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

Models were evaluated using:
- Accuracy Score
- Classification Report

The best-performing model was selected based on accuracy and overall performance.

------------------------------------------------------------

## Final Output

The system predicts:
- Hire or Reject
- Probability Score

------------------------------------------------------------

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

------------------------------------------------------------

## Conclusion

This project demonstrates:
- Data preprocessing and feature engineering
- Text vectorization using TF-IDF
- Model training and comparison
- Practical implementation of an AI hiring prediction system

It reflects real-world HR automation and resume screening applications.
