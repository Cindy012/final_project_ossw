# final_project_ossw
For my final project of the course Open Source SW, I was given the assignment to find the best model to fit the data points using Scikit Learn.

# Dataset
The dataset I have used is a tumor dataset. The dataset contains MRI information of various brain tumors. THe tumor_dataset are classified in 4 folders, each containing the data of a different or no tumor. The folders are:
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
In the file 'find_best_model.ipynb', I have used the training data to train the model and used the test data to test the model. The random state is set as 2 to compare the models. The accuracy scores of the models (rounded with 3 decimals) are as follows:
1. Random Forest (0.891)
2. Support Vector Machine (0.830)
3. Logistic Regression (0.815)
4. Perceptron (0.814)
5. K-Nearest Neighbors (0.791)
6. Decision Tree (0.779)

## Random State
To compare the models, I have used a random state of 2. I decided not to find the best rnadom state number while doing the gridsearch as it would take too much time.
