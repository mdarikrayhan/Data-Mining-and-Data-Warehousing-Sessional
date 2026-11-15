# Data Mining and Data Warehousing Sessional

Jupyter notebooks for **CSE-4250 Data Mining and Data Warehousing Sessional**, a lab course in the B.Sc. in CSE at BAUET (Bangladesh Army University of Engineering & Technology), written in the first half of 2024. The labs go from Python, NumPy and pandas basics to exploratory data analysis, clustering and classification with scikit-learn. A separate folder holds facial emotion recognition experiments with Keras.

## Contents

### Weekly labs ([Codes](Codes))

| Notebook | What it does |
| --- | --- |
| [Day_1.ipynb](Codes/Day_1.ipynb) | Python basics: printing, variables, data types and arithmetic operators |
| [Day_2.ipynb](Codes/Day_2.ipynb) | NumPy arrays and array operations; pandas DataFrames with `iloc`, `loc` and boolean indexing |
| [Day_3.ipynb](Codes/Day_3.ipynb) | Matplotlib line and scatter plots, pandas Series and DataFrames, reading a CSV file |
| [Day_4.ipynb](Codes/Day_4.ipynb) | Pima Indians diabetes data: summary statistics, min-max normalisation of the age column, class distribution, histograms, correlation matrix and scatter matrix |
| [Day_5.ipynb](Codes/Day_5.ipynb) | Iris data: summary statistics, missing-value check, histograms, seaborn scatter and pair plots, correlation heatmap |
| [Day_6.ipynb](Codes/Day_6.ipynb) | Fills missing income values with the column mean and compares two months' incomes with histograms |
| [Day_7.ipynb](Codes/Day_7.ipynb) | One-dimensional k-means clustering written from scratch, printing every step (the notebook is headed "KNN") |
| [KNN.cpp](Codes/KNN.cpp) | The same one-dimensional k-means in C++ |
| [Kmeans.ipynb](Codes/Kmeans.ipynb) | K-means (k = 2) with scikit-learn on the standardised diabetes data, plotted by glucose and blood pressure |
| [Lab5.ipynb](Codes/Lab5.ipynb) | Iris exploration, then logistic regression, k-nearest neighbours and decision tree classifiers |
| [Lab_Final.ipynb](Codes/Lab_Final.ipynb) | Lab final practice: loading data, summaries, filling missing values, feature engineering (a combined date column and BMI), correlation and plots. Its `Lab_Final.csv` uses placeholder names and dates, and the saved outputs were cleared |

### Fruit classification ([Codes/Fruit Data with Colours](Codes/Fruit%20Data%20with%20Colours))

| Notebook | What it does |
| --- | --- |
| [Code.ipynb](Codes/Fruit%20Data%20with%20Colours/Code.ipynb) | Loads the fruit data and counts each fruit |
| [fruit_data_with_colours.ipynb](Codes/Fruit%20Data%20with%20Colours/fruit_data_with_colours.ipynb) | Explores and plots the fruit data, then classifies the fruit with k-nearest neighbours and compares accuracy for different values of k |
| [LAB_Final.ipynb](Codes/Fruit%20Data%20with%20Colours/LAB_Final.ipynb) | Box plots, scatter matrix and histograms, then compares decision tree, logistic regression, k-nearest neighbours, Gaussian naive Bayes and SVM classifiers |

### House price regression ([Codes/Lab Work](Codes/Lab%20Work))

| Notebook | What it does |
| --- | --- |
| [Task.ipynb](Codes/Lab%20Work/Task.ipynb) | Cleans a house sales dataset, plots its features, label-encodes and normalises it, removes outliers with DBSCAN and fits a linear regression, reporting MAE, MSE and RMSE |

### Facial emotion recognition ([Lab Work](Lab%20Work))

| Item | What it is |
| --- | --- |
| [efficientnetv2-emotion-recognition.ipynb](Lab%20Work/efficientnetv2-emotion-recognition.ipynb) | Transfer learning with EfficientNetV2-M on an emotion recognition image dataset, written for Kaggle |
| [ED_CNN](Lab%20Work/ED_CNN) | A shorter copy of that notebook, plus [main.py](Lab%20Work/ED_CNN/main.py), which reads the webcam, finds faces with a Haar cascade and labels each face's emotion with the Keras model in `data.h5` |
| [FER2013](Lab%20Work/FER2013) | A CNN trained on the FER2013 dataset, with training, testing, custom-image and confusion-matrix scripts; see its [README](Lab%20Work/FER2013/README.md) |

## Tech stack

- Python 3 with Jupyter: pandas, NumPy, Matplotlib, seaborn, scikit-learn
- TensorFlow/Keras and OpenCV for the emotion recognition work
- C++ for `KNN.cpp`

## Getting started

```bash
pip install notebook numpy pandas matplotlib seaborn scikit-learn
jupyter notebook
```

Most notebooks read their CSV files from the same folder. `Day_4.ipynb`, `Kmeans.ipynb` and `Lab Work/ED_CNN/main.py` use absolute paths from the author's computer; change them to relative paths (for example `pima_indians_diabetes_data.csv`) before running. The emotion recognition scripts also need `tensorflow`, `keras` and `opencv-python`, and the EfficientNet notebooks expect the Kaggle dataset path `/kaggle/input/emotion-recognition-dataset`.

## Credits

- [Lab Work/FER2013](Lab%20Work/FER2013) follows the FER2013 project its README links to (`gitshanks/fer2013`).
- [Lab Work/ED_CNN](Lab%20Work/ED_CNN) keeps the README of the "Emotion_Detection_CNN_keras" project it is based on.

## Author

Md Arik Rayhan — [mdarikrayhan.com](https://mdarikrayhan.com)
