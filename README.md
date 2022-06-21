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

<br>

## 📌 Problem Statement

*Can you predict who is most likely to have a bank account?*

The purpose of this competition is to create a machine learning model to predict which individuals will and will not use a bank account. The models and solutions
developed should provide an indication of the state of financial inclusion in Kenya, Rwanda, Tanzania and Uganda.

<br>

## 💾 Data Understanding

### - Code Used:

* Python Version : 3.10
* Packages : Pandas, Numpy, Matplotlib, Seaborn, Scikit-Learn

### - Importing Dataset:

* Kaggle: https://www.kaggle.com/competitions/inclusao-financeira-na-africa/data

### - Data Dictionary

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
 
 
 ### - Data Exploration
 
   1. The train data is contains large number of categorical features that should be treated. For the 1º cicle run, we tried Ordinal Encoding, then proceed with LabelEncoding, and OneHotEncoding.
   2. The numeric columns are not normally distributed, which need to be standardized. 
   3. The target variable is kind of imbalanced (14% for 1-class), it might have to be treated.
   4. The outliers of the numeric column should be treated.

 
 <br>
 
## 🧾 Evaluation Metric
 
 The model evaluation metric for this competition was the "Mean F1-Score". The F1-Score can be interpreted as a harmonic average of "precision" and "recall".

 The F1 metric weights recall and accuracy equally, and a good ranking algorithm will maximize accuracy and recall simultaneously.
 
<br>

## 🔬 Solution Approach

The approach was divided in the following parts:

   1. Building the first model with a Logistic Regression Model, just to find a baseline score.
   2. Building the second model with Random Forest, then proceed with Gradient Boostings Models like LGBM and XGB.
   3. Balancing the data with SMOTE technique didn't seem very effective, so we dropped it.
   4. After trying Ordinal and LabelEncoding, Standardization combined with OneHotEncoding made the difference to reach top scores.
   5. Even though the final model in notebook is XGBClassifier (best score tested later), we managed to reach 3rd place with LGBM with **default parameters**.

You can check our final code [here](https://github.com/leassis91/hackday_ds/blob/master/bank-account-prediction-xgbclassifier-pipeline.ipynb) and in [Kaggle](https://www.kaggle.com/code/leandrodestefani/bank-account-prediction-xgbclassifier-pipeline).

<br>

## 💡 Conclusions

  * The big challenge of the competition was: to handle or not the imbalanced data. Still our data was imbalanced (only 14% did have a bank account), the strategies used always decreased the score. SMOTE does not take into consideration neighboring examples can be from other classes. This can increase the overlapping of classes and can introduce additional noise, and it seems only to be useful when applied at *extremely imbalanced data* (check references articles).
  * OneHotEncoding is the best approach for these type of dataset (few features, few unique labels);
  * For every Feature Engineering method I've tried, it seemed like it followed the rule: greater number of features equals higher scores (eventually it breaks for like 50+ features);
  * OrdinalEncoder approach scored better than LabelEncoder (yet keep in mind that if you OneHotEncode the labels, it should score higher)
  * "Be Data-Centric", as Andrew Ng would say. Our solution which made it to the 3rd place was sent without any hyperparameter fine-tuning (a simply LGBMClassifier()).
  
<br>
  
  ## 📖 References

- JAMIA - [The harm of class imbalance corrections for risk prediction models: illustration and simulation using logistic regression](https://academic.oup.com/jamia/advance-article/doi/10.1093/jamia/ocac093/6605096?searchresult=1&login=false)
- DataCamp - [Diving Deep with Imbalanced Data](https://www.datacamp.com/tutorial/diving-deep-imbalanced-data)
- Neptune.ai - [How to Deal With Imbalanced Classification and Regression Data](https://neptune.ai/blog/how-to-deal-with-imbalanced-classification-and-regression-data)
<br>

If you have any other suggestion or question, feel free to contact me via [LinkedIn](https://linkedin.com/in/leandrodestefani).


## 💪 How to contribute

1. Fork the project.
2. Create a new branch with your changes: `git checkout -b my-feature`
3. Save your changes and create a commit message telling you what you did: `git commit -m" feature: My new feature "`
4. Submit your changes: `git push origin my-feature`
  
