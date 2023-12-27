# Project Description

## Step 1: Problem Statement
Given a dataset containing various chemical properties of wines, including Alcohol content, Phenolic compounds, and Color intensity, the goal is to develop a classification model using Principal Component Analysis (PCA) and Logistic Regression. The aim is to accurately predict wine categories (0, 1, or 2) based on their chemical composition.

## Step 2: Data Gathering
The dataset, sourced from Kaggle, is in CSV format with approximately 200 rows and 14 columns. This diverse dataset becomes the canvas on which we paint our vinicultural exploration.
 
## Step 3: Exploratory Data Analysis (EDA)
In this phase, we meticulously examined the dataset:
- Checked for information about the table and data types.
- Explored null values and utilized descriptive statistics.
- Statistical Information: Calculate mean, median, and other descriptive statistics (e.g., standard deviation) using functions describe() to gain insights into data characteristics.

## Step 4: Feature Engineering

Feature engineering is pivotal for shaping the dataset for optimal model performance. This step involves:

#### Outlier Handling:-

Identified and addressed outliers using the Interquartile Range (IQR) method. Outliers were meticulously examined and replaced to ensure robust model training.

#### Standardization in PCA:-
Standardized data using `StandardScaler()` after outlier handling.

**Equal Scaling:** Ensures consistent scale among features, preventing dominance by larger-scaled variables.

**Mean-Centering:** Centers principal components around the origin, revealing true variability in the data.

**Handling Unit Differences:** Mitigates unit variations, crucial for unbiased PCA and reliable feature extraction.

**Interpretability:** Enhances interpretability by providing consistent scaling, making PCA loadings more meaningful.

## Step 5: model training
1.The dataset was divided into training and testing sets using the `train_test_split` function.

2.The PCA model was then trained for dimensionality reduction.

3.PCA, a powerful dimensionality reduction technique, was applied to the standardized data. This step not only enhances model efficiency but also provides insights into the underlying patterns of the dataset.

####  PCA and Logistic Regression Implementation
1.The `PCA_1` model with `n_components=2` was employed. The transformed data for both training and testing sets was obtained using the `fit_transform` method. The explained variance ratio provided insights into the significance of each principal component.

2.The PCA model was then trained for dimensionality reduction. The implementation of Logistic Regression followed, as the dataset is inherently a classification dataset.

## Step 6: Model Evaluation
The model's performance was meticulously assessed:
- **Accuracy:** Achieved a remarkable 98% accuracy on training data and 96% on testing data.
- **Confusion Matrix:** Upon analysis, the training data confusion matrix revealed only two mispredicted values in the second class, while the remaining two classes were accurately predicted.
For the testing data, a solitary mispredicted value emerged in the second class, whereas the first class and the third class of the target column exhibited accurate predictions.
This meticulous examination of the confusion matrix provides insights into the model's ability to predict values within the same class and identifies instances of mispredictions.

#### Confusion Matrix for Training Data

 [[41  0  0]
 [ 1 48  1]
 [ 0  0 33]]
 
#### Confusion Matrix for Training Data

 [[17  1  0]
 [ 1 20  0]
 [ 0  0 15]]
 

## Step 7: Conclusion
The journey through the Chemical Composition Analysis of Wines has been a captivating exploration of the intricate world of viniculture. From data gathering to model evaluation, each step has unraveled the secrets hidden in the chemical makeup of wines. The application of PCA and Logistic Regression has not only classified wines accurately but has also provided visual insights into the classification boundaries.

