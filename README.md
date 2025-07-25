# 🫀 Heart Disease Prediction Using Machine Learning and Deep Learning

[![](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=darkgreen)](https://www.python.org)  [![](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=TensorFlow&logoColor=white)](https://www.tensorflow.org) [![](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/stable/) [![](https://img.shields.io/badge/SciPy-654FF0?style=for-the-badge&logo=SciPy&logoColor=white)](https://www.scipy.org) [![](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org) [![](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org)  [![](https://img.shields.io/badge/Plotly-239120?style=for-the-badge&logo=plotly&logoColor=white)](https://plotly.com) [![](https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=Keras&logoColor=white)](https://keras.io) [![](https://img.shields.io/badge/conda-342B029.svg?&style=for-the-badge&logo=anaconda&logoColor=white)](https://www.anaconda.com)

## Introduction 

Predicting the condition of a patient in the case of __heart disease__ is important. It would be good if a patient could get to know the condition before itself rather than visiting the doctor. Patients spend a __significant amount__ of time trying to get an appointment with doctors. After they get the appointment, they would have to give a lot of tests. 

<img src = "https://github.com/Sankethprasad09/Images/blob/23d7e4ec988b5bace0e457209f84d22ecb590657/Heart%20Disease%20Prediction/heart1.jpg" height = 375 width = 250/> <img src = "https://github.com/Sankethprasad09/Images/blob/23d7e4ec988b5bace0e457209f84d22ecb590657/Heart%20Disease%20Prediction/heart3.jpg" height = 375 width = 250/> <img src = "https://github.com/Sankethprasad09/Images/blob/23d7e4ec988b5bace0e457209f84d22ecb590657/Heart%20Disease%20Prediction/stetoscope.jpg" height = 375 width = 250/>

It is also important that a doctor be present so that they could treat them. To make things worse, the tests usually take a long time before __diagnosing__ whether a person would suffer from heart disease. However, it would be handy and better if we automate this process which ensures that we save a lot of time and effort on the part of the doctor and patient. 

## Machine Learning and Data Science 

With the aid of machine learning, it is possible to get to know the condition of a patient whether he/she would have heart disease or not based on a few features such as glucose levels and so on. Using machine learning algorithms, we are going to predict the chances of a person suffering from heart disease. In other words, we would be using various machine learning models for the prediction of the chances of heart disease in a patient. 

## Data 

Some of the input features that would be considered in this example are __blood pressure__, __chest pain type__ and __cholestrol levels__. This is just a sample dataset with 303 rows. This is created just to understand different classification machine learning algorithms and sklearn implementation of them. Below is the link where you can find the source of the data. Thanks to __'kaggle'__ for providing this data. 

https://www.kaggle.com/johnsmith88/heart-disease-dataset

## Exploratory Data Analysis (EDA)

When we are performing EDA, interesting insights could be drawn from the data and understood. Below are the key insights that were found as a result of working with the data. 

* The features __'thalach'__ and __'slope'__ are positively correlated. However, they are not highly correlated.
* Features such as __'age'__ and __'thalach'__ which stands for __maximum heart rate achieved__ are negatively correlated as indicated by the correlation heatmap plot. 
* __'age'__ is negatively correlated with __'restecg'__ as shown in the heatmap plot.
* The features __'cp'__ and __'exang'__ are negatively correlated.
* The feature __'resting blood pressure'__ is somewhat positively correlated with __'age'__ as shown in the plots. 
* The feature __'trestbps'__ that stands for resting blood pressure is somewhat correlated with the feature __'fbs'__ that stands for fasting blood pressure.

## Visualizations 

In this section, we will be visualizing some interests plots and trends in the data which is used by machine learning models to make predictions. We will also evaluate the performance of different machine learning and deep learning models on a given dataset by comparing various metrics. To identify the best version of each model, we will examine their hyperparameters.

To begin, we will review the list of rows and columns (features) in our dataset, which includes age, sex, cp (chest pain), chol, and others. This will provide insight into the types of features present and help us determine if additional features are necessary for analysis.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Data.png"/>

Next, we will examine the list of non-null values in the data to identify any missing values. Since there are 303 entries, we know that the dataset includes 303 patients. Additionally, the memory usage is minimal, so downcasting is not necessary.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Data%20info.png"/>

The study's participants have an **average age** of approximately **55 years**. While most values in the dataset are **numerical**, some are **categorical**. To convert categorical features into numerical ones, we will use **one-hot encoding**.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Data%20description.png"/>

This plot demonstrates the total number of patients who had a **heart disease** vs. the number of patients who did not have a **heart disease**. This shows that a large number of patients had **heart disease**. Therefore, it becomes easy for us to build interesting **classifiers** as we have more information about patients with **heart disease**. In addition, the total classes are **balanced** which means that we can use metrics such as **accuracy** for understanding the ML model performance.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Target%20count.png"/>

The plot shows the **prevalence** of heart disease by **gender**. The data has more samples for males than females and suggests a gender difference in **survival rates**. The data is slightly imbalanced but not significantly.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Gender%20plot.png"/>

The heatmap shows the **correlations** between pairs of features. The lighter the color, the stronger the correlation according to the color map. For example, 'thalach' and 'slope' have a positive correlation, while 'slope' and 'oldpeak' have a negative correlation. Other features can be further explored for their correlations.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Heatmap.png"/>

The plot below shows a **negative** correlation between age and thalach. This suggests that thalach can be a predictor of age and vice versa. This relationship can be useful for model predictions.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/thalach%20vs%20age.png"/>

There are some interesting **trends and patterns** found in the dataset. It could be seen that **higher values of thalach** and **lower values of oldpeak** can have an impact about whether a person can suffer from heart disease. All in all, having a higher value of thalach is one of the factors that can be leading to heart disease according to the scatterplots displayed below. 

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/scatterplots.png"/>

The plot shows a strong **positive** correlation between age and cholesterol levels. This reflects the common observation that older people tend to have higher cholesterol levels. This may vary across different countries and populations, but it is a general trend in the plot.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Chol%20Vs.%20Age%20Scatterplots.png"/>

The **cholesterol** feature in our dataset is univariate and primarily concentrated within the range of 200-300. However, there are a few **outliers**, such as values of 400 or 500. Although the sample size is not large, we cannot simply discard these values when inputting the feature into machine learning models for prediction purposes.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Cholestrol%20boxplot.png"/>

According to the dataset, the **average** age of the patients is approximately 55 years, with the youngest being 30 and the oldest being 85 years old. The majority of individuals fall within the age range of 50-60 years.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Age%20boxplot.png"/>

The plot displays the **performance** of various machine learning models based on different **evaluation metrics**, including accuracy, f1-score, precision, recall, and AUC scores. Naive Bayes stands out as a promising model for predicting heart disease, having achieved a high accuracy rate. Moreover, both KNN and Naive Bayes exhibit similar f1-scores and AUC scores, indicating comparable overall performance in terms of predicting heart disease.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Model%20Outcomes%20Metrics.png"/>

In machine learning, **normalization** and **standardization** are common preprocessing techniques used to ensure that data distribution does not affect model performance. If the initial data given to the model was standardized but not normalized, we can perform normalization and assess model performance on the test set.

After normalization, the **Naive Bayes model** had the highest accuracy and F1-score compared to other models. This suggests that Naive Bayes is a good fit for the normalized data.

<img src = "https://github.com/Sankethprasad09/Heart-Disease-Prediction/blob/4d61aaf2fd3445e21f3107ffd5266012d8d78025/images/Normalized%20metrics.png"/>

## Machine Learning Models 

There were many machine learning models used in the process of predicting the __heart diseases__. Below are the models that were used in the process of predicting heart diseases.

* [__K Nearest Neighbors (KNN)__](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsClassifier.html)
* [__Logistic Regression__](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html)
* [__Naive Bayes__](https://scikit-learn.org/stable/modules/generated/sklearn.naive_bayes.MultinomialNB.html)
* [__Random Forest Classifier__](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)

## Outcomes

* Based on the results generated, it could be seen that the __Naive Bayes model__ was performing the best in terms of the __F1 score__, __precision__, and __recall__ respectively. 
* __Naive Bayes model__ was also having the __highest accuracy__ in terms of classifying whether a person would have a __heart disease__ or not.

## Future Scope

* __Additional data__ from many sources could be taken so that the models would be able to predict for __different conditions__ for the patients.
* __More features__ that help determine whether a person would suffer from heart disease could be considered.
* The **Naive Bayes model**, which had the best performance, could be deployed in real-time to provide doctors with faster inference results. This could aid in the diagnosis of whether a person is suffering from heart disease or not. 
* The quick and accurate results from the model could potentially help **doctors** make more timely and effective decisions in treating their patients.

## 👉 Directions to download the repository and run the notebook 

This is for the Washington Bike Demand Prediction repository. But the same steps could be followed for this repository. 

1. You'll have to download and install Git which could be used for cloning the repositories that are present. The link to download Git is https://git-scm.com/downloads.
 
&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/68ec804a501be2c8861643e707166d33a5d0ccd2/washington_bike_prediction_images/Screenshot%20(14).png" width = "600"/>
 
2. Once "Git" is downloaded and installed, you'll have to right-click on the location where you would like to download this repository. I would like to store it in the "Git Folder" location. 

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/68ec804a501be2c8861643e707166d33a5d0ccd2/washington_bike_prediction_images/Screenshot%20(15).png" width = "600" />

3. If you have successfully installed Git, you'll get an option called "Gitbash Here" when you right-click on a particular location. 

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/68ec804a501be2c8861643e707166d33a5d0ccd2/washington_bike_prediction_images/Screenshot%20(16).png" width = "600" />

4. Once the Gitbash terminal opens, you'll need to write "Git clone" and then paste the link to the repository.

5. The link to the repository can be found when you click on "Code" (Green button) and then, there would be an HTML link just below. Therefore, the command to download a particular repository should be "Git clone HTML" where the HTML is replaced by the link to this repository. 

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/68ec804a501be2c8861643e707166d33a5d0ccd2/washington_bike_prediction_images/Screenshot(17).png" width = "600" />

6. After successfully downloading the repository, there should be a folder with the name of the repository as can be seen below.

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/60b3eb7b600fef4bc619331ba5caf21e93b149ef/washington_bike_prediction_images/Screenshot%20(19).png" width = "600" />

7. Once the repository is downloaded, go to the start button and search for "Anaconda Prompt" if you have anaconda installed. 

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/60b3eb7b600fef4bc619331ba5caf21e93b149ef/washington_bike_prediction_images/Screenshot%20(20).png" width = "600" />

8. Later, open the Jupyter notebook by writing "Jupyter notebook" in the Anaconda prompt. 

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/60b3eb7b600fef4bc619331ba5caf21e93b149ef/washington_bike_prediction_images/Screenshot(21).png" width = "600" />

9. Now the following would open with a list of directories. 

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/60b3eb7b600fef4bc619331ba5caf21e93b149ef/washington_bike_prediction_images/Screenshot(22).png" width = "600" />

10. Search for the location where you have downloaded the repository. Be sure to open that folder. 

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/60b3eb7b600fef4bc619331ba5caf21e93b149ef/washington_bike_prediction_images/Screenshot%20(12).png" width = "600" />

11. You might now run the .ipynb files present in the repository to open the notebook and the python code present in it. 

&emsp;&emsp; <img src = "https://github.com/Sankethprasad09/Images/blob/60b3eb7b600fef4bc619331ba5caf21e93b149ef/washington_bike_prediction_images/Screenshot(13).png" width = "600" />

That's it, you should be able to read the code now. Thanks. 
