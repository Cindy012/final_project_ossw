# final_project_ossw
For the final project of the course Open Source SW, the assignment was to find the best model to fit the data points using Scikit Learn.

# Dataset
The dataset is a tumor dataset. The dataset contains MRI information of various brain tumors. THe tumor_dataset are classified in 4 folders, each containing the data of a different or no tumor. The folders are:
- glioma_tumor
- meningioma_tumor
- no_tumor
- pituitary_tumor

# Approach of finding the best model.
To find the best model, I have used a variety of models and compared their accuracy scores. The models I have used are:
* Logistic Regression
* Perceptron
* Decision Tree
* Random Forest
* Support Vector Machine
* K-Nearest Neighbors

## PreSelection
In the file 'find_best_model.ipynb', the training data is used to train and test the model (using train_test_split function of sklearn). The random state is set as 2 to compare the models. The accuracy scores of the models (rounded with 3 decimals) are as follows:
1. Random Forest (0.891)
2. Support Vector Machine (0.830)
3. Logistic Regression (0.815)
4. Perceptron (0.814)
5. K-Nearest Neighbors (0.791)
6. Decision Tree (0.779)

## Random State
To compare the models, random state = 2 is used. It is decided to not find the best random state number as it takes too much time when that parameter is added to find the best parameters with gridsearch.
