# Heart-Disease-Prediction [Machine Learning Project]
# Introduction
Heart Disease , also known as cardiovascular disease, is the primary basis of death worldwide over the span of the past few decades. This makes heart disease a major concern to be dealt with. But, it is difficult to identify heart disease because of several contributory risk factors such as diabetes, high blood pressure, high cholesterol, abnormal pulse rate, and many other factors.
So, there should be some method which can predict the heart disease in advance with as much accuracy as possible.
So, with the help of this project, we can predict whether a person has heart disease or not. 
I build a Machine Learning model which will take some input features and will predict the target value based on input features.
I have used the "Logistic Regression" algorithm to train the model because our target variable will give the answer in yes or no only.
# Types of Attributes:
1. pid: Patient identification number.
2. age: The person's age in years.
3. sex: The person's sex (1=male,0=female)
4. cp: The chest pain experienced (Value 1: Typical angina, Value 2: Atypical angina, Value 3: Non-    anginal pain, Value 4: Asymptomatic).
5. trestbps: The person's resting blood pressure ( mm Hg on admission to the hospital ).
6. chol: The person's cholesterol measurement in mg/dl
7. famhist: Family history of coronary artery disease (1=yes; 0=no).
8. fbs: The person's fasting blood sugar ( > 120 mg/dl, 1= true; 0= false)
9. restecg: Resting electrocardiographic measurement (0 = normal, 1 = having ST-T wave 
   abnormality, 2 = showing probable or definite left ventricular hypertrophy by Estes'            criteria).
10. Smoke: 1 = yes; 0 = no (is or is not a smoker).
11. thalach: The person's maximum heart rate achieved.
12. exang: Exercise induced angina (1 = yes; 0 = no).
13. Oldpeak: ST depression induced by exercise relative to rest.
14. slope: The slope of the peak exercise ST segment (Value 1: upsloping, Value 2: flat, Value       3: downsloping).
15. ca: The number of major vessels (0-4).
16. thal: A blood disorder called thalassemia.
17. target: Heart disease (0= no, 1= yes).
# Data Preprocessing Steps:
1. Data cleaning: 
   * In this, I have removed all the NULL values using 'dropna'.
   * Then, I have checked whether there is any NULL value present or not using  
     df.isnull().any().


2. Data reduction:
   * In data reduction, I remove some unwanted columns.
        - pid
        - smoke
        - famhist
3. Data encoding:
   * In this, I replace some column values with numeric values.
        Example: 
                 -  In column ‘Sex’, I replace ‘M’ with 1 and ‘F’ 
                    with 0.
                 -  In column 'cp', I replace 'Typical Angina' with 1, Atypical Angina with 2,                     Non-Angina pain with 3, 'Asymptomatic' with 4.
   * As in column ‘fbs’, I replace ‘TRUE’ values with 1 and ‘FALSE’ values with 0. So, 
     I have to change the datatype also from ‘boolean’ to ‘int’.
     
4. Normalization:
   * I need normalization because in this case, values of all attributes differ very much from        each other.

# Separating and Splitting of data.
* First of all, I separate the X and Y values.
* Then, I split the data into 'train' and 'test' data.

# Apply various ML algorithms.
* On training data: Maximum accuracy is achieved by SVM, i.e, 92.97%
* On testing data: Maximum accuracy is achieved by Logistic Regression, i.e, 83.60%
# Predict the target values.
* In this, a set of input features is given to the model and then, the model will predict         whether the patient has heart disease or not.
* If the value of the target variable is 1, then the patient has heart disease. Otherwise, not.
