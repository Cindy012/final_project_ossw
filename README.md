# final_project_ossw
For the final project of the course Open Source SW from Chung-Ang University, the assignment was to find the best model to fit the data points using scikit-learn.

## Dataset
The dataset is a tumor dataset. The dataset contains MRI information of various brain tumors. The tumor_dataset are classified in 4 folders, each containing the data of a different or no tumor. The folders are:
- glioma_tumor
- meningioma_tumor
- no_tumor
- pituitary_tumor

-> The tumor training dataset that is used for this project is not included in the code.

## Approach of finding the best model.
To find the best model, I have used a variety of models and compared their accuracy scores. The models I have used are:
* Logistic Regression
* Perceptron
* Decision Tree
* Random Forest
* Support Vector Machine
* K-Nearest Neighbors

### PreSelection
In the file `find_best_model.ipynb`, the training data is used to train and test the model (using train_test_split function of scikit-learn). The random state is set as 2 to compare the models. The accuracy scores of the classification methods (rounded with 3 decimals) are as follows:
1. Random Forest (0.891)
2. Support Vector Machine (0.830)
3. Logistic Regression (0.815)
4. Perceptron (0.814)
5. K-Nearest Neighbors (0.791)
6. Decision Tree (0.779)

### Random State
To compare the models, random state = 2 is used. It is decided to not find the best random state number as it takes too much time when that parameter is added to find the best parameters with gridsearch.

### GridSearch
From the PreSelection, it is clear that Random Forest, SVM, and Logistic Regression are the top 3 classification methods in general to classificate tumors. To find the best model, GridSearch will be used to find the best parameters (for each classification method model).

After performing GridSearch, new models are created using the best parameters, will be trained with the tumor data, and will have a new accuracy.

## Conclusion
After finding the top 3 classification methods (through the PreSelection) and best parameters for the model using GridSearch, it is clear that the **Random Forest model is the most accurate with the brain tumor dataset** compared to Logistic Regression and SVM.
 
## Files
The following files are used to define the best model:
* **final_project_cindy_ye_50231630.ipynb**
   * In this file the best model is used to train and predict with training data.
* **find_best_model.ipynb**
   * In this file is checked with classification methods models are the best in general.
* **gridsearch_log_reg.ipynb**
   * In this file GridSearch is performed for logistic regression. After finding the best parameters, the training data will be used to train the model. The new accuracy is used to find the best model after GridSearch.   
* **gridsearch_svm_random_forest.ipynb**
   * In this file GridSearch is performed for SVM and Random Forest. After finding the best parameters for each model, the training data will be used to train the models. The new accuracy of the models is used to find the best model after GridSearch.   

## Configuration
When using a code editor or Jupyter Notebook, please install the following if not installed:
```
pip install scikit-learn scikit-image numpy matplotlib
```

## Operating instructions
1. Open **final_project_cindy_ye_50231630.ipynb** using code editor of Jupyter Notebook.
2. Click on: run all cells.
3. Tumor data will be prepared.
4. Random Forest model will be created with the given parameters, and trained with the training data `X_train` and `y_train`.
5. Random Forest model will make predictions using the test data X_test. The data will be saved in `y_pred`.
6. Accuracy score will be printed using `y_test`, and `y_pred`.

## Copyright and licensing information
Please refer to the LICENSE file (MIT license) in the repository.

## Contact information
If there are any questions, please contact the project owner at [cindy.ye@windesheim.nl].
