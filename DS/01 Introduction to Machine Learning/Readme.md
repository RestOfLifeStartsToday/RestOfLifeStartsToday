# **Project description**

Mobile carrier Megaline has found out that many of their subscribers use legacy plans. They want to develop a model that would analyze subscribers&#39; behavior and recommend one of Megaline&#39;s newer plans: Smart or Ultra.

You have access to behavior data about subscribers who have already switched to the new plans (from the project for the Statistical Data Analysis course). For this classification task, you need to develop a model that will pick the right plan. Since you&#39;ve already performed the data preprocessing step, you can move straight to creating the model.

Develop a model with the highest possible _accuracy_. In this project, the threshold for _accuracy_ is 0.75. Check the _accuracy_ using the test dataset.

**Project instructions**

1. Open and look through the data file. Path to the file:datasets/users\_behavior.csv[Download dataset](https://code.s3.yandex.net/datasets/users_behavior.csv)
2. Split the source data into a training set, a validation set, and a test set.
3. Investigate the quality of different models by changing hyperparameters. Briefly describe the findings of the study.
4. Check the quality of the model using the test set.
5. Additional task: sanity check the model. This data is more complex than what you&#39;re used to working with, so it&#39;s not an easy task. We&#39;ll take a closer look at it later.

**Data description**

Every observation in the dataset contains monthly behavior information about one user. The information given is as follows:

- сalls — number of calls,
- minutes — total call duration in minutes,
- messages — number of text messages,
- mb\_used — Internet traffic used in MB,
- is\_ultra — plan for the current month (Ultra - 1, Smart - 0).