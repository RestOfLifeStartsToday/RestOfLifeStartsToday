# **Project description**

Beta Bank customers are leaving: little by little, chipping away every month. The bankers figured out it&#39;s cheaper to save the existing customers rather than to attract new ones.

We need to predict whether a customer will leave the bank soon. You have the data on clients&#39; past behavior and termination of contracts with the bank.

Build a model with the maximum possible _F1_ score. To pass the project, you need an _F1_ score of at least 0.59. Check the _F1_ for the test set.

Additionally, measure the _AUC-ROC_ metric and compare it with the _F1_.

**Project instructions**

1. Download and prepare the data. Explain the procedure.
2. Examine the balance of classes. Train the model without taking into account the imbalance. Briefly describe your findings.
3. Improve the quality of the model. Make sure you use at least two approaches to fixing class imbalance. Use the training set to pick the best parameters. Train different models on training and validation sets. Find the best one. Briefly describe your findings.
4. Perform the final testing.

**Data description**

The data can be found in /datasets/Churn.csv file. [Download the dataset.](https://code.s3.yandex.net/datasets/Churn.csv)

**Features**

- _RowNumber_ — data string index
- _CustomerId_ — unique customer identifier
- _Surname_ — surname
- _CreditScore_ — credit score
- _Geography_ — country of residence
- _Gender_ — gender
- _Age_ — age
- _Tenure_ — period of maturation for a customer&#39;s fixed deposit (years)
- _Balance_ — account balance
- _NumOfProducts_ — number of banking products used by the customer
- _HasCrCard_ — customer has a credit card
- _IsActiveMember_ — customer&#39;s activeness
- _EstimatedSalary_ — estimated salary

**Target**

- _Exited_ — сustomer has left