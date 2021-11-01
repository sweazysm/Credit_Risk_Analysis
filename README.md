# Credit Risk Analysis

Credit Cards, Credit Score, Credit Limits, the list goes on! Your credit is important, and analysis of credit is also very important. Through the use of Machine Learning it was taked to assess several machine learning tests in regards to Credit Card Risk. Using libraries such as imbalanced-learn and scikit-learn, as well as aalgorithms such as RandomOverSample and SMOTE, machine models were trained to assess Credit Card Risk to determine which model gave the best results. 

# Results

Balance and Accuracy scores were assessed for six machine learning models in our analysis of Credit Risk Analysis. The first machine learning models were on Resampling.

<img width="1072" alt="Screen Shot 2021-10-31 at 7 32 13 PM" src="https://user-images.githubusercontent.com/86274124/139606372-f1b6e184-4bb0-4c9a-9d5a-393a1c4016ca.png">
<img width="810" alt="Screen Shot 2021-10-31 at 7 32 22 PM" src="https://user-images.githubusercontent.com/86274124/139606377-3f291c3a-c71a-4b56-9e9c-be297eee14de.png">

The first step taken was splitting the data into features and targets. For the purpose of this analysis the focus was on "Loan Status." From basic assessments it was found that there are 347 high risk credit accounts. Through the machine learning with train test splits, the high risk account numbers went from 347 to 260 (as shown above).

<img width="636" alt="Screen Shot 2021-10-31 at 7 32 40 PM" src="https://user-images.githubusercontent.com/86274124/139606979-a1fd71a9-48a8-4901-adc2-e0bbef7ea9ab.png">
<img width="798" alt="Screen Shot 2021-10-31 at 7 32 49 PM" src="https://user-images.githubusercontent.com/86274124/139606983-a427df34-f88e-42f6-802d-04b09e7f28d0.png">

The first model used reseampling with RandomOverSampler. After training the logistical regression model with the resampled data, calculating the balanced accuracy score, and printing the classification report we found a Balanced Accuracy Score of 0.649 and a Recall score of 0.62 for high_risk accounts and a Recall score of 0.68 for low_risk accounts with an average of 0.68.

<img width="635" alt="Screen Shot 2021-10-31 at 7 32 58 PM" src="https://user-images.githubusercontent.com/86274124/139607855-85ec84ed-acec-44f1-a675-a45737d12acb.png">
<img width="799" alt="Screen Shot 2021-10-31 at 7 33 06 PM" src="https://user-images.githubusercontent.com/86274124/139607861-7a2d8e3e-4d6c-4eeb-a298-c564c7b64e1d.png">

Following oversampling with RandomOverSampler, we then tested the machine learning model with SMOTE. The data was trained with SMOTE, the logisitical regression moodel was retrained with the resampled data, the balanced accuracy score was calculated, a confusion matrix was made, and an imbalanced classification report was printed. SMOTE yieled a Balanced Accuracy score of 0.644 and a Recall score of 0.63 for high_risk accounts and a Recall score of 0.66 for low_risk accounts with the average being 0.66.

Between RandomOverSample and SMOTE, RandomOverSample performed slightly better with an average score of 0.68 as opposed to SMOTE's 0.66

<img width="772" alt="Screen Shot 2021-10-31 at 7 33 18 PM" src="https://user-images.githubusercontent.com/86274124/139608002-e5e6841d-d5da-4895-a629-406b23d859aa.png">
<img width="794" alt="Screen Shot 2021-10-31 at 7 33 28 PM" src="https://user-images.githubusercontent.com/86274124/139608008-c251d349-a0b2-4bae-bc71-195043be676a.png">

With Oversampling done we now move onto our Undersampling. With undersampling we used the CluserCentroids resampler. This resampler was loaded in and our data resampled. The resampled data was then trained with a logistic regression model, a confusion matrix was generated, a balanced accuracy score was generated, and an imbalanced classification report was printed.

The results generated showed that the Cluster Centroids method has a balanced accuracy score of 0.529 with a Recall score of 0.61 for high_risk accounts and a Recall score of 0.45 for low_risk accounts. The average total Recall score was a 0.45. From this we can tell that both RandomOverSampler and SMOTE performed better than the ClusterCentroids method.

<img width="702" alt="Screen Shot 2021-10-31 at 7 33 39 PM" src="https://user-images.githubusercontent.com/86274124/139608300-bffc3cac-ff2b-4650-9ebe-8e437f65819e.png">
<img width="731" alt="Screen Shot 2021-10-31 at 7 33 50 PM" src="https://user-images.githubusercontent.com/86274124/139608301-7ba22f8b-1de2-491d-929a-c2d4ca2f35f0.png">

With Oversampling and Undersampling performed we then moved on to a combination of Over and Under sampling. For this the SMOTEENN algorithm was used. The data was retrained with SMOTEENN, the resampled data was then trained into a logistical regression model, a confusion matrix was generated, a balanced accuracy score was generated, and an imbalanced classification report was printed.

The balanced accuracy score generated using SMOTEEN yieled a score of 0.637. The Recall score for high_risk accounts was found to be 0.70, and the Recall score for low_risk accounts was found to be 0.57. The average for these was found to be 0.57.

While this method yieled better results than Cluster Centroids, it is still not better than RandomOverSample or SMOTE.


<img width="613" alt="Screen Shot 2021-10-31 at 7 36 21 PM" src="https://user-images.githubusercontent.com/86274124/139608455-56071134-4131-4b89-8b02-6796d2f049b9.png">
<img width="729" alt="Screen Shot 2021-10-31 at 7 36 30 PM" src="https://user-images.githubusercontent.com/86274124/139608493-95f0ddfa-d4e8-4143-9fc7-ebbc46027993.png">

Here we are testing out the Balanced Random Forest Classifier (BRFC) algorithm. The data was retrained with BRFC, a confusion matrix was generated, a balanced accuracy score was generated, and an imbalanced classification report was printed.

BRFC's accuracy score yieled a score of 0.563. The Recall score for high_rusk accounts was found to be 0.49 and the Recall score for low_risk accounts was found to be 0.63. The average of these was found to be 0.63.

While better than SMOTEEN and Cluster Centroids, so far RandomOverSample and SMOTE have come out on top with the best scores.


<img width="536" alt="Screen Shot 2021-10-31 at 7 37 23 PM" src="https://user-images.githubusercontent.com/86274124/139608599-78d9da5c-34c2-4161-91e8-8f9ddd6c3706.png">
<img width="721" alt="Screen Shot 2021-10-31 at 7 37 29 PM" src="https://user-images.githubusercontent.com/86274124/139608602-93e9bbd7-f238-4f13-ad58-f45a1e2b3a44.png">

Last, but not least, we tested out the sixth algorithm which is the Easy Ensemble AdaBoost Classifier (EEC). The data was retrained with EEC, a confusion matrix was generated, a balanced accuracy score was generated, and an imbalanced classification report was printed.

EEC's balanced accuracy report yielded a score of 0.925. The Recall score for high_risk accounts was found to be 0.91 and the Recall score for low_risk accounts was found to be 0.94. The average for these was calculated out at 0.94.

These results put EEC far above the other algorithms tested in this Credit Risk Analysis.

Almost all models yieled a precision score of 0.01 for high_risk accounts and a precision score of 1.00 for low_risk accounts. The only exception is that EEC has a precision score of 0.07 for high_risk accounts and a precision score of 1.00 for low_risk accounts.

# Summary

From the models shown, the algorithms tested, and the results yielded the answer is clear: In this analysis with this data, EEC performed the best. Coming in with a Balanced Accuracy score of 0.925, a Recall Score of 0.91 for high_risk and a score of 0.94 for low_risk, and a higher precision score for high_risk than all other models, EEC seems to be the most truthworthy option of the six. It was disheartening to see precision scores for high_risk accounts being so low across the board, however. Perhaps an algorithm and/or model can be performed to give more accuracy to these scores. Other than that, from the scores presented I would recommend the EEC model be used.



