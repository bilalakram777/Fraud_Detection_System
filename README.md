Project Overview
The Credit Card Fraud Detection Project aims to identify fraudulent transactions using machine learning techniques. The project leverages a dataset containing various features related to credit card transactions, including a target variable that indicates whether a transaction is fraudulent or legitimate. The primary objective is to build a predictive model that can accurately classify transactions based on their features.

Steps to Run the Scripts
Prerequisites:

Ensure that Python is installed on your system.
Install the necessary libraries required for data manipulation and machine learning. This can be done using the following command:
pip install pandas scikit-learn imbalanced-learn

Dataset Preparation:

Download the Credit Card dataset in CSV format and save it as creditcard.csv in the same directory as your script. This dataset contains various features related to credit card transactions, including a target variable named 'Class' that indicates whether a transaction is fraudulent (1) or legitimate (0).
Loading the Data:

The first step in the script is to load the dataset using the Pandas library. The pd.read_csv() function reads the CSV file and stores the data in a DataFrame. The initial rows of the dataset are printed to the console to provide a glimpse of the data structure and the features available for analysis.
Data Preparation:

The dataset is then prepared for modeling by separating the features (X) from the target variable (y). The 'Class' column, which indicates the transaction type, is dropped from the features, while the remaining columns are retained for model training.
Train-Test Split:

The dataset is split into training and testing sets using the train_test_split() function from the Scikit-learn library. This function randomly divides the data, with a specified proportion (20% in this case) reserved for testing the model's performance after training.
Handling Class Imbalance with SMOTE:

Credit card fraud datasets often exhibit class imbalance, where legitimate transactions vastly outnumber fraudulent ones. To address this issue, the Synthetic Minority Over-sampling Technique (SMOTE) is applied to the training data. SMOTE generates synthetic samples for the minority class (fraudulent transactions) to create a more balanced dataset, which helps improve the model's ability to learn from both classes.
Model Training:

A Random Forest Classifier is chosen for this project due to its robustness and effectiveness in handling classification tasks. The model is instantiated with specific parameters, such as the number of estimators (50) and maximum depth (10), to control overfitting. The model is then trained on the resampled training data, allowing it to learn the patterns associated with both fraudulent and legitimate transactions.
Model Evaluation:

After training, the model's performance is evaluated using the testing set. The classification_report() function from Scikit-learn provides a comprehensive overview of the model's performance metrics, including precision, recall, and F1-score for both classes. These metrics help assess how well the model can distinguish between fraudulent and legitimate transactions.
Testing the Model:

A function is defined to allow users to input transaction details for testing the fraud detection model. The user is prompted to enter values for various features, including the time since the first transaction and the transaction amount. The model then predicts whether the transaction is fraudulent or legitimate based on the input features.
Running the Testing Interface:

The testing function is executed if the script is run as the main program. This interactive interface allows users to test the model with their own transaction data, providing immediate feedback on whether a transaction is classified as fraudulent or legitimate.


How to Run the Scripts
To successfully run the Credit Card Fraud Detection project scripts, follow these steps:

1. Set Up Your Environment
Install Python: Ensure that you have Python installed on your machine. You can download it from python.org.
Install Required Libraries: Open your command line interface (CLI) and install the necessary libraries using pip. Run the following command:
pip install pandas scikit-learn imbalanced-learn


2. Download the Dataset
Obtain the Dataset: Download the Credit Card dataset in CSV format. You can find it on various platforms, such as Kaggle or UCI Machine Learning Repository. Save the file as creditcard.csv in the same directory where your script will be located.
3. Prepare the Script
Create a Python Script: Open your preferred code editor (e.g., VSCode, PyCharm, or Jupyter Notebook) and create a new Python file (e.g., fraud_detection.py).
Copy the Code: Copy the provided code into your Python script. Ensure that the code is complete and correctly formatted.
4. Run the Script
Execute the Script: Open your command line interface, navigate to the directory where your script is located, and run the script using the following command:
python fraud_detection.py


Observations
Data Imbalance: The original dataset is likely to have a significant imbalance between legitimate and fraudulent transactions. This imbalance can lead to biased model predictions, where the model may predict the majority class (legitimate transactions) more often than the minority class (fraudulent transactions).

Effectiveness of SMOTE: By applying the SMOTE technique, the model can learn from a more balanced dataset. This helps improve the model's ability to detect fraudulent transactions, as it has more examples of the minority class to learn from.

Model Performance: The Random Forest Classifier is a robust choice for this type of classification problem. The classification report generated after model evaluation provides insights into the model's performance, including precision, recall, and F1-score. High precision and recall values for the fraudulent class indicate that the model is effective in identifying fraud.

User Interaction: The interactive testing function allows users to input their own transaction details, making the model accessible for practical use. This feature enhances user engagement and provides a hands-on experience in testing the model's predictions.

Real-World Application: The project demonstrates the practical application of machine learning in the financial sector, particularly in fraud detection. The ability to identify fraudulent transactions in real-time can significantly reduce financial losses for banks and credit card companies.
