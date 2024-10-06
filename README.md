# deep-learning-challenge
Report on Neural Network Model for Alphabet Soup
Overview of the Analysis
Alphabet Soup, an organization, wants to be able to predict where to make investments. Using data from successful fundings and charitable donations, the analysis will dive into 34,000 organizations that successfully captured metadata from their past successes. This analysis aims to utilize deep-learning neural networks to analyze and predict whether applicants will succeed if funded by Alphabet Soup.
Results

Data Preprocessing
•	Target Variable(s):
o	IS_SUCCESSFUL: This is the target variable for the model, indicating whether the funding was successful (1) or not (0).
•	Feature Variable(s):
o	The features selected for the model include the processed and encoded categorical variables such as:
	APPLICATION_TYPE
	AFFILIATION
	CLASSIFICATION
	USE_CASE
	ORGANIZATION
	STATUS
	INCOME_AMT
	SPECIAL_CONSIDERATIONS
	The ASK_AMT column was also used as a feature.
•	Removed Variable(s):
o	EIN: This unique identifier was removed because it does not provide predictive value.
o	NAME: This variable was also removed since it’s not relevant for predicting success and could lead to

 overfitting due to its high cardinality.

Compiling, Training, and Evaluating the Model
•	Initial Model
•	Neurons, Layers, and Activation Functions:
o	Input Layer:
	The input layer had the same number of neurons as there were features in the dataset.
o	First Hidden Layer:
	Number of neurons: 80
	Activation function: ReLU (Rectified Linear Unit) was chosen due to its efficiency in handling non-linear
 relationships.
o	Second Hidden Layer:
	Number of neurons: 30
	Activation function: ReLU
o	Output Layer:
	Number of neurons: 1
	Activation function: Sigmoid was used since it’s appropriate for binary classification.
o	Model Performance:
	Training Loss: 0.5773
	Training Accuracy: 72.77%
	The initial model did not achieve the target accuracy of 75%.

•	
•	First Optimized Model
•	Neurons, Layers, and Activation Functions:
o	Input Layer:
	The input layer had the same number of neurons as there were features in the dataset.
o	First Hidden Layer:
	Number of neurons: 100
	Activation function: ReLU (Rectified Linear Unit) was chosen due to its efficiency in handling non-linear
 relationships.
o	Second Hidden Layer:
	Number of neurons: 50
	Activation function: ReLU
o	Third Hidden Layer:
	Number of neurons: 25
	Activation function: ReLU
o	Output Layer:
	Number of neurons: 1
	Activation function: Sigmoid was used since it’s appropriate for binary classification.
o	Model Performance:
	Training Loss: 0.6009
	Training Accuracy: 72.58%
	The first optimized model did not achieve the target accuracy of 75%.
•	
•	Last Optimized Model
•	Neurons, Layers, and Activation Functions:
o	Input Layer:
	The input layer had the same number of neurons as there were features in the dataset.
o	First Hidden Layer:
	Number of neurons: 128
	Activation function: ReLU (Rectified Linear Unit) was chosen due to its efficiency in handling non-linear relationships.
o	Second Hidden Layer:
	Number of neurons: 64
	Activation function: ReLU
o	Third Hidden Layer:
	Number of neurons: 32
	Activation function: ReLU
o	Output Layer:
	Number of neurons: 1
	Activation function: Sigmoid was used since it’s appropriate for binary classification.
o	Model Performance:
	Training Loss: 0.5889
	Training Accuracy: 72.61%
	The last optimized model did not achieve the target accuracy of 75%.

•	Steps to Increase Performance:
o	Added more hidden layers.
o	Increased the number of neurons in each hidden layer.
o	Used early stopping to prevent overfitting.
o	Adjusted the number of epochs and batch size.
o	Combined rare categories into a new "Other" category to reduce noise.

Summary
•	Overall Results:
o	The final model achieved an accuracy of approximately 72% after several optimization efforts. Despite multiple attempts to optimize the model, achieving the target accuracy remained challenging.
•	Recommendation:
o	Given the current results, an alternative model such as a Random Forest classifier or Gradient Boosting Machine might be more effective for this classification problem. These models can handle a large number of features and can often achieve better performance with less need for complex hyperparameter tuning.

