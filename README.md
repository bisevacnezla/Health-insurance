# Health-insurance
In this repository, I'm training multiple linear regression to predict a health insurance charges based on the following factors:
* Age
* Sex
* BMI
* Children
* Smoker (yes/no)
* Region

After encoding, splitting the dataset and training the model, we got the **regressor coefficient** values:
>**4.84e+02  2.24e+02 -4.29e+02 -2.78e+02  2.54e+02 -1.55e+01  3.36e+02 4.37e+02  2.36e+04**

We had to apply encoding to *gender*, *smoker* and *region* features. On *gender* and *smoker* we applied Label Encoding because there are only two values possible (male/female, yes/no), but
on *region* feature we applied One Hot Encoding because there are four values possible (northwest, northeast, southwest, southeast). Therefore, southhwest is encoded as [1.0 1.0 0.0],
northwest as [1.0 0.0 0.0], southeast as [0.0 1.0 0.0], northeast as [0.0 0.0 0.0]. After encoding, the *gender* column will now contain three columns and won't be penultimate column anymore,
but the first (first three solumns).

Now we can define our equation:
>Insurance_charges = 4.84 * D1 - 2.24 * D2 - 4.29 * D3 -2.78 * D4 + 2.54 * Age - 1.55 * Sex + 3.36 * Bmi + 4.37 * Children + 2.36 * Smoker

D1, D2, D3 and D4 stand for dummy variables.

Regressor intercept value is -12311.913605650474. We see that the intercept is negative and that usually occurs when none of the X values are close to 0.


The dataset was taken from [kaggle](https://www.kaggle.com/mirichoi0218/insurance).
