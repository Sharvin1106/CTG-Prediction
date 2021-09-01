# Machine-Learning-and-Fuzzy-Logic-Module

<p align="center"><i>We wanted to build a Machine Learning and Fuzzy Logic Module to classify fetal states based on the CTG data.</i></p>


## Introduction

<p> Cardiotocography (CTG) is a medical procedure that records the fetal heartbeat and uterine contractions during pregnancy. CTG reading will be very important in order to determine the condition of the baby and prevent any mortality whether to the baby or mother. The fetal heart rate is given more importance in the CTG because it reveals if the fetal is going through hypoxia or any distress which can lead to severe complications in delivery.  Hence, CTG comes in handy in conditions where the women who are going to labour is in high-risk category or if the fetal heartrate is too low, too high or abnormal. It is a very controversial and problematic task. It because there are so many things that we need to look out in a CTG to correctly understand the fetal heart rate activity in accordance to the uterine contraction. Errors and pitfalls can cause doctors to receive incorrect reading which can endanger the fetus.There are few things we need to give importance on when interpreting the CTG such as the fetal heart rate, number of accelerations in the fetal heart rate, uterine contraction per second, variability in fetal heart rate and decelerations. The fetal is in normal condition if the heartbeat rate is between 110-160 beats per minute, there are accelerations present which lasts long for more than 15 seconds with a rise of 15 beats per minute in the fetal heart rate and there is a variability in the fetal heart rate more than 5 beats per minute. However, there must not be any deceleration present in the fetal heart rate. If it happened so, then the fetal is categorized as in the pathological state. There are 5 requirements for a fetal’s conditions to be categorized as normal. If one of the conditions is not met, then fetal condition will be categorized as suspect. If more than 2 condition is not met, then fetal condition will be categorized as pathological.</p>

<img src="https://github.com/Katheeravan305/Machine-Learning-and-Fuzzy-Logic-Module/blob/main/images/1.png" 
     width = 600px
     height = 400px
     />

## Aim

<p>The above pair plot shows all the features available in this dataset. All these features are part of CTG readings. In this project, we were very interested in building a predictive modal for cardiotocography. Our goal was to make a modal that can classify fetal heart rate reading into three categories which are Normal, Suspect and Pathologic.</p>
 
 
## Problem Definition
- To reduce human interpretation error in CTG.
- To build a cohesive computerised algorithm to interpret CTG readings with no human intervention.
- To determine the best and optimal number of features to be used in the modal.
- To choose the best modal for CTG reading interpretation.
- To find the best parameters for each modal which are suitable for imbalance dataset. Then pick the best modal out of them. 


## Feature Selection
In this experiment there are total of 23 features and 2126 CTG records. It is computationally expensive to build, train and test models with 23 features. Hence, to reduce the feature space we have performed feature selection to select relevant features in building the machine learning model. However, there are some data cleanings has been carried out before selecting the features.
<ol> 
  <li>Data Cleaning</li>
    <ul>
      <li> Firstly, we have removed the columns that have least unique values. The reason why we do so is, because with least unique values the columns have, it is most probably not contributing much to predicting but just increase the feature space. Hence, we removed the DS, DP and NZeros.</li>
         <img src="https://github.com/Katheeravan305/Machine-Learning-and-Fuzzy-Logic-Module/blob/main/images/2.0.png" />
      <li>Secondly, we have removed all the duplicated rows that are present in the data because it paves the chance for information leak where the same record may present in both train set and test set. We have discovered a total of 12 duplicated rows, and we removed all of them.</li>
         <img src="https://github.com/Katheeravan305/Machine-Learning-and-Fuzzy-Logic-Module/blob/main/images/3.png" />
       <li>Thirdly, we have imputed the missing data in the dataset instead of removing them, the reason why we do this is because every data matters. Hence, we perform KNNImputer to impute the missing values because it is a faster and efficient way to impute missing values instead of other statistical measures. Finally, we also removed the outliers that are present in the dataset or just introduced by previous imputation method as it can disrupt the prediction of model which will eventually lead to poorer results.</li>
    </ul>
 </ol>
