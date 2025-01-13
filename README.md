# Money-Laundering-Detection
This is a project aimed at attempting to build a money laundering detection with machine learning and deep learning models, with a pre-existing generated labelled transactions for banks dataset.
The dataset is available publicly via Kaggle here: https://www.kaggle.com/datasets/ealtman2019/ibm-transactions-for-anti-money-laundering-aml/data

###
It is important to note that the project takes on two separate approaches while running the same models and parameters to ensure consistency and comparability across approaches.
1. Using the suggested High-Illicit Activity datasets, large, medium, and small, as the train, test, and validation datasets
2. Using the High-Illicit Activity - Medium dataset and perform SMOTE oversampling method at a 80:20 ratio
Both datasets have been downsampled at the same factor based on its size, and performed label & one-hot encoding to convert some columns into numerical format.

###
For starters, I recommend looking through the OSEMN & Baseline Models first to understand the data downsampling and pre-processing process. Furthermore, have a look at the EDA to understand the data trends and distributions.

###
To improve the transparency of the machine learning model building & tuning process, the code is readily available for viewing and to be tuned as necessary to enhance the performances, furthermore a feature importance graph is computed to understand the significance of the weights given to each variable.

The platform used to host the code is Google Colab platform, which has been able to perform the necessary transformations and model building process.

###
The Sci-Kit learn version that has been used for the code is 1.5.2, as there has been some issues with XGBoost and AdaBoost unable to find the necessary model to perform GridSearchCV, when it comes to sklearn_tag, just keep that in mind when running the code. The rest has been default, based on the platform.

The GPU Models used has been primarily the L4 option and occassionally the A100 module. However, it is not necessary to run the codes with the best graphic card option, it will do the job with just CPU operations if you don't mind having it run on the background.

Last thing, the datasets are huge, especially the HI-Large, at 180 Million observations, coming in at 16 Gigabytes in total. Therefore, enough ram is necessary in order to perform the necessary breakdown before proceeding with the rest of the code to improve code-running efficiency and not wasting any unnecessary computational power, saving a copy will help.

###
Machine Learning Models (Baseline + GridSearchCV @ 5 Cross Validations)
1. Naive Bayes Classification
2. Decision Tree
3. Random Forest
4. XGBoost
5. AdaBoost

###
Machine Learning Models (Baseline + RandomSearchCV @ 10 Samples and 5 Cross validations)
1. Logistic Regression
2. Gradient Boosting

###
Deep Learning Models (Epoch = 10, 30, Learning Rate = 0.1, 0.01, 0.001)
1. Keras Deep Learning
2. Reccurent Neural Network (RNNs)
3. Long Short Term Memory (LSTM)

###
Evaluation Metrices
1. Accuracy
2. Precision
3. Recall
4. F1-Score
5. Youden's J
6. ROC AUC
7. ROC Curve
8. Confusion Matrix
