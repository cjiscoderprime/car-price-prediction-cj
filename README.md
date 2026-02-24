This project uses supervised machine learning. It is performed using labeled data and it's purpose is to predict the next value with a dataset that has both input and output values. It is similar to a student learning from practice questions and answers, to solve new unseen problems on their own.



Our goal is to predict continuous and numerical values. This can be achieved with regression.



1\) Linear Regression models the relationship between a dependent and independent variable. It tries to fit a straight line into the observed data.



2\) Lasso Regression stands for Least Absolute Shrinkage and punishes large coefficients. It is a technique used to prevent overfitting by penalizing the model for being too complex.



If Linear Regression tries to listen to every single person in a crowded room,

Lasso listens to the person with the megaphone, and mutes quiet people entirely.

Focusing on stronger features and reducing errors massively, lasso creates a sparse model. It reduces variance and improve interoperability just by focusing on smaller number of features.





**Dataset used (what’s inside)**



The dataset has 301 entries and the columns:



Car\_Name 



Year (car manufacturing year)



Selling\_Price (this is the target to predict)



Present\_Price (current showroom price)



Kms\_Driven (how much the car has been driven)



Fuel\_Type (Petrol / Diesel / CNG)



Seller\_Type (Dealer / Individual)



Transmission (Manual / Automatic)



Owner (0, 1, 3 etc. meaning how many previous owners)





**Workflow** 



1\. Load the dataset

2\. Clean and preprocess data

3\. Encode categorical variables (Fuel\_Type, Seller\_Type, Transmission)

4\. Split into train and test sets

5\. Train regression models:

&nbsp;  - Linear Regression

&nbsp;  - Lasso Regression

6\. Evaluate using R² score

7\. Plot Actual vs Predicted prices





**Evaluation Metric**

**R² Score**



Measures how much variance in selling price is explained by the model:

\- 1.0 = perfect predictions

\- 0.0 = no better than predicting the mean





**Visualization of Predictions**



To evaluate prediction quality, scatter plots of Actual vs Predicted values were generated.



Each regression model produces two scatterplots:





**1.) Linear Regression** – Training Data	Checks how well the model fits known data



**2.) Linear Regression** – Testing Data	Checks generalization to unseen data



**3.) Lasso Regression** – Training Data	Fit of regularized model on training set



**4.) Lasso Regression** – Testing Data	Generalization of regularized model





**Technologies Used**



**Python**



**NumPy**



**Pandas**



**Scikit-Learn**



**Matplotlib**







**Linear Regression**

**Dataset	R² Score**



**Training Data**	0.8799

**Testing Data**	0.8366





On training data, the model explains ~87.99% of the variance in selling price.

On unseen testing data, it explains ~83.66% of the variance.





**Lasso Regression**

**Dataset	R² Score**



**Training Data**	0.8428

**Testing Data**	0.8709





Training performance is slightly lower than Linear Regression (because of regularization).

However, testing performance is higher than Linear Regression.







**Final Observation** 



Linear Regression fits training data very well but slightly loses performance on unseen data.



Lasso Regression, by penalizing large coefficients, avoids memorizing noise in training data.



Lasso Regression achieved better performance on the testing dataset, indicating improved generalization due to regularization.













