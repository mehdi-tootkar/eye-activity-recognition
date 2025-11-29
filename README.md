# eye-activity-recognition

This project focuses on **detecting the type of desktop activity performed by a user based on their eye-movement data (eye-tracking signals)**.  
The dataset includes **24 participants**, each performing **8 different tasks** (Browse, Debug, Interpret, Play, Read, Search, Watch, Write), resulting in **192 samples**.

## Project Description
The goal of this project is to classify the type of activity using only gaze coordinates (x, y) and timestamps.  
To achieve this, we perform **feature engineering** inspired by research in eye-tracking analysis, including:
- Basic gaze statistics (mean, standard deviation, min, max for x and y)  
- Saccade dynamics (average movement between consecutive gaze points, variance, max)  
- Time-related features (average interval between gaze points, variation in intervals)  

With these engineered features, several **machine learning models** were applied:
- Logistic Regression (70% accuracy)  
- Random Forest (80% accuracy)  
- XGBoost (82.5% accuracy, best performance)  
- SVM, MLP, and others for comparison  

The evaluation followed a **user-wise split** (19 participants for training, 5 participants for testing), ensuring that the model is tested on unseen users for a realistic scenario.

## Key Results
- **Best model**: XGBoost (72.5% accuracy)  
- Demonstrated that engineered eye-movement features can capture task-specific patterns.  
- Provides a baseline for future deep learning approaches (e.g., LSTM, GRU).  

## Dataset
The dataset is available on Kaggle:  
👉 [Eye Movement Data Set for Desktop Activities](https://www.kaggle.com/datasets/namratasri01/eye-movement-data-set-for-desktop-activities)

*Note: The dataset is not included in this repository due to size. See `data/README.md` for instructions to download and prepare the dataset.*
