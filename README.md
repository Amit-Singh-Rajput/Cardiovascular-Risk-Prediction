# **Cardiovascular Risk Prediction**

## **Problem Statement**

The dataset is from an ongoing cardiovascular study on residents of the town of Framingham, Massachusetts. The classification goal is to predict whether the patient has a 10-year risk of future coronary heart disease (CHD). The dataset provides the patients’ information. It includes over 4,000 records and 15 attributes.

**Variables:**

Each attribute is a potential risk factor. There are both demographic, behavioral, and medical risk factors.

## **Data Description**

**Demographic:**

- Sex: male or female("M" or "F")
- Age: Age of the patient;(Continuous - Although the recorded ages have been truncated to whole numbers, the concept of age is continuous)

**Behavioral:**

- is_smoking: whether or not the patient is a current smoker ("YES" or "NO")
- Cigs Per Day: the number of cigarettes that the person smoked on average in one day.(can be considered continuous as one can have any number of cigarettes, even half a cigarette.)

**Medical(history):**

- BP Meds: whether or not the patient was on blood pressure medication (Nominal)
- Prevalent Stroke: whether or not the patient had previously had a stroke (Nominal)
- Prevalent Hyp: whether or not the patient was hypertensive (Nominal)
- Diabetes: whether or not the patient had diabetes (Nominal)

**Medical(current):**

- Tot Chol: total cholesterol level (Continuous)
- Sys BP: systolic blood pressure (Continuous)
- Dia BP: diastolic blood pressure (Continuous)
- BMI: Body Mass Index (Continuous)
- Heart Rate: heart rate (Continuous - In medical research, variables such as heart rate though in fact discrete, yet are considered continuous because of large number of possible values.)
- Glucose: glucose level (Continuous)

**Predict variable(desired target):**

- 10-year risk of coronary heart disease CHD(binary: “1”, means “Yes”, “0” means “No”) - DV

## **Project Flowchart**

Our project flowchart includes the following steps:

- Loading and diagnosing the data
- Data Cleaning
- Data Visualization
- Feature Selection
- Model Building
- Model Evaluation

## **Challenges**
- Handling the missing values.
- Making Class Imbalance.

## **Conclusion**
- The most important feature in determining the risk of coronary heart disease is the age of the patient.
- Consumption of cigarettes per day is directly proportional to the risk of heart disease.
- Patients with a history of BP medication, prevalent stroke, prevalent hypertension, diabetes, high cholesterol, high systolic blood pressure, and high diastolic blood pressure are at a higher risk of heart disease.
- Patients with high BMI are prone to heart disease risk.

It is important to have a high recall score in this scenario because it is okay if the model incorrectly identifies a healthy person as a high-risk patient because it will not result in death, but if a high-risk patient is incorrectly identified as healthy, it may result in fatality. Support Vector Machine with RBF kernel is the best model with a recall score of 0.88.

In cases where patients who are incorrectly classified as suffering from heart disease are equally important as patients who are correctly classified as suffering from heart disease, a high f1 score is desired. Logistic Regression, XGBoost, and K-NN are the models with the most F1 scores.

Overall, this project demonstrates the importance of accurate prediction of the risk of future coronary heart disease and the potential impact it can have on patient health outcomes.
