# Decision-Trees-and-Random-Forests
1. Imported Required Libraries
We started by importing Python libraries like pandas, scikit-learn, matplotlib, and seaborn to:

Load and handle data

Build machine learning models

Visualize trees and results
2. Loaded the Dataset
We used the Heart Disease Dataset, which contains medical information such as:

Age

Blood Pressure

Cholesterol

Chest Pain Type

Target (1 = heart disease, 0 = no disease)

We separated:

Features (X) = all columns except target

Labels (y) = target column (what we’re trying to predict)
3.Split the Data
We split the dataset into:

Training set (80%): used to train the model

Test set (20%): used to check how well the model performs on unseen data
4. Trained a Decision Tree Classifier
We trained a basic Decision Tree with limited depth (max_depth=4) to avoid overfitting.
We evaluated its accuracy on the test data and generated a classification report showing:

Precision

Recall

F1 Score

We also visualized the decision tree using tree.plot_tree() — this shows how the model makes decisions step by step.

5.Overfitting Analysis
To understand overfitting:

We trained several Decision Trees with increasing depth (1 to 19).

We plotted Training vs. Testing Accuracy.

This helped us observe how increasing complexity affects performance.

Insight:
Too shallow = underfitting
Too deep = overfitting

6. Trained a Random Forest Classifier
Then, we trained a Random Forest:

An ensemble of many Decision Trees (we used 100)

It’s more accurate and stable than a single tree

Reduces overfitting by averaging predictions from multiple trees (bagging)

We compared its accuracy and classification report to that of the Decision Tree.

7. Feature Importance
Random Forest tells us which features are most important for making predictions.
We plotted these feature importances to interpret:

Which medical factors affect heart disease the most.

8. Cross-Validation
We evaluated the Random Forest using 5-fold cross-validation:

This splits the data into 5 parts and tests the model on each

Helps confirm the model is stable and generalizes well



