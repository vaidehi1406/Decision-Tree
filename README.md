# Decision-Tree

The provided code builds and visualizes a Decision Tree classifier using the Bank Personal Loan Modelling dataset.

---

A decision tree is a supervised machine learning algorithm used for both classification and regression tasks. It works by recursively partitioning the dataset into subsets based on the most significant attribute at each step, creating a tree-like structure of decisions. Each node in the tree represents a decision based on a particular feature, and each leaf node represents the predicted outcome.

---

 Let's break down the code and analyze the results.

**Code Explanation:**

**1.Data Import:**

* The necessary libraries are imported: pandas, matplotlib, seaborn, LabelEncoder, and the required modules from scikit-learn.
* The dataset "Bank_Personal_Loan_Modelling.csv" is read into a Pandas DataFrame.

**2.Data Exploration:**

* df.info() is used to display information about the dataset, including data types and non-null counts.
* df.head() is used to display the first few rows of the dataset.

**3.Feature Extraction:**

* The 'Personal Loan' column is designated as the target variable (target), and the rest of the columns are considered as input features (inputs).

**4.Label Encoding:**

* Label encoding is applied to categorical variables using the LabelEncoder class for each relevant feature.
* New columns with suffix '_n' are created for each feature, storing the encoded values.

**5.Drop Unnecessary Columns:**

* Some columns like 'ID', 'ZIP Code', 'Age', 'Experience', 'Income', 'Family', 'CCAvg', 'Education', 'Mortgage', 'Securities Account', 'CD Account', 'Online', 'CreditCard' are dropped from the dataset as they are either redundant or not needed for the model.

**6.Model Building:**

* A Decision Tree classifier is initialized with the criterion set to 'entropy' and a maximum depth of 12.
* The model is fitted to the training data (inputs_n and target).

**7.Model Evaluation:**

* The model's accuracy score on the training data is computed using dtree.score(inputs_n, target). The result is 0.9994, indicating high accuracy.

**8.Visual Representation:**

* The Decision Tree is visualized using tree.plot_tree() from scikit-learn's tree module. The resulting plot shows the structure of the Decision Tree.
