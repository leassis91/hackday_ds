<!-- # hackday_ds
Hackday Competition by Comunidade DS -->

# <p align="center">🐱‍💻 HACKDAY CDS - BANK ACCOUNT PREDICTION 🏦 </p> 
<p align="center"><img src="https://github.com/leassis91/hackday_ds/blob/master/financial-inclusion.png"></p>

## 📖 Background

Financial inclusion continues to be one of the main efforts for economic and human development in Africa. For example, in Kenya, Rwanda, Tanzania and Uganda, only 9.1 million adults (14% of adults) have access to or use a business bank account.

In 2008, the level of financial inclusion in Sub-Saharan Africa was just over 23%. In 2018, that number almost doubled. In Togo, Mazamesso Assih, finance minister, coordinates a financial inclusion strategy with partner banks. He states that ensuring access to basic financial services for the population is critical to boosting the African economy.

In 2022, as highlighted in the latest report by the Central Bank of West Africa, one of the highest rates of financial inclusion in the region was reached, close to 82%. A significant portion of this increase came from the rise of digital financial services.

Assih also states that there are three main reasons why African nations should focus on financial inclusion:

  1. Making financial services more accessible promotes the empowerment of the most vulnerable people, especially women.
  2. Fighting criminal networks moving from an exclusively cash economy to a digital financial infrastructure makes it easier for authorities to track transactions and 
  deal with smugglers and traffickers.
  3. Boost public and private sector connectivity for sustainable growth by supporting African start-ups.


## 📌 Problem Statement

*Can you predict who is most likely to have a bank account?*

The purpose of this competition is to create a machine learning model to predict which individuals will and will not use a bank account. The models and solutions
developed should provide an indication of the state of financial inclusion in Kenya, Rwanda, Tanzania and Uganda.



## 💾 Data Understanding

### Code Used:

* Python Version : 3.9
* Packages : Pandas, Numpy, Matplotlib, Seaborn, Scikit-Learn

### Importing Dataset:

* Kaggle: https://www.kaggle.com/competitions/inclusao-financeira-na-africa/data

### Data Dictionary

Variable | Definition
------------ | -------------
 |  country                               | Origin country.
 |  year                                  | Year of financial inclusion. 
 |  uniqueid                              | User Id.
 |  bank_account                          | Target Value: whether user has a bank account or not .
 |  location_type                         | Type of user's location: rural or urban.
 |  cellphone_access                      | Whether user has a cellphone or not
 |  household_size                        | Number of persons in a private household related to user.
 |  age_of_respondent                     | User age.
 |  gender_of_respondent                  | User gender.
 |  relationship_with_head                | Status with account owner.
 |  marital_status                        | User civil status.
 |  education_level                       | User education level.
 |  job_type                              | Kind of work.
 
 ## 🧾 Evaluation Metric
 
 The model evaluation metric for this competition was the "Mean F1-Score". The F1-Score can be interpreted as a harmonic average of "precision" and "recall".

 The F1 metric weights recall and accuracy equally, and a good ranking algorithm will maximize accuracy and recall simultaneously.
 
