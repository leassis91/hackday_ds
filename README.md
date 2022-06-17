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
 
## 💡 Conclusions

  * Even though our data was imbalanced (only 14% did have a bank account), the strategies used always decreased the score. SMOTE seems only to be useful when applied at *extremely imbalanced data*
  * OneHotEncoding is the best approach for these type of dataset (few features, few unique labels);
  * For every Feature Engineering method I've tried, it seemed like it followed the rule: more features, more scores (eventually it breaks for like 50+ features);
  * OrdinalEncoder approach scored better than LabelEncoder (yet keep in mind that if you OneHotEncode the labels, it should score higher)
  * "Be Data-Centric", as Andrew Ng would say. Our solution which made it to the 3rd place was sent without any hyperparameter fine-tuning (a simply LGBMClassifier()).
  
<!--   ## References

- Statistics How To - [Interquartile Range](https://www.statisticshowto.com/probability-and-statistics/interquartile-range/#:~:text=The%20interquartile%20range%20(IQR)%20is,of%20that%20interval%20of%20space.&text=If%20you%20want%20to%20know,the%20first%20or%20lower%20quartile.)
- Blog [Seja um Data Scientist](https://sejaumdatascientist.com/os-5-projetos-de-data-science-que-fara-o-recrutador-olhar-para-voce/)
- Dataset from [Kaggle](https://www.kaggle.com/harlfoxem/housesalesprediction)
- Data Information from [Geocenter](https://geodacenter.github.io/data-and-lab/KingCounty-HouseSales2015/) -->

If you have any other suggestion or question, feel free to contact me via [LinkedIn](https://linkedin.com/in/leandrodestefani)


## 💪 How to contribute

1. Fork the project.
2. Create a new branch with your changes: `git checkout -b my-feature`
3. Save your changes and create a commit message telling you what you did: `git commit -m" feature: My new feature "`
4. Submit your changes: `git push origin my-feature`
  
