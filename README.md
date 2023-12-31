
# Airbnb Perfect Rating Score Prediction

## Business Understanding  
 
### The business case: 
 
The predictive model we built can be beneficial to real estate firms planning to expand their current business by investing in buying new properties and rolling out a rental business model, similar to Airbnb. 
 
Our model can act as a core profit driver for the firms as they plan to invest in select properties that have a promising return on investment (ROI). And our model predicts just the right indicator of profitability, i.e., perfect_rating_score which predicts whether or not a particular property listing is likely to have a high chance of getting a perfect rating score. Therefore the predictive model will act as a great guide in the business decision-making process of investing only in those properties that will have a high ROI. 
 
### Business actions: 
 
On the other hand, the predictive model will also provide further insights into the specific features of different properties that translate into the company’s profits. For instance, if we find out that ‘host_is_superhost’ predictor has a significant weightage in predicting the accurate perfect_rating_score for a given listing, then the firm can translate the same into their business decisions. That is, they can ensure that the owners of their property listings follow a certain protocol that aligns with the objective of turning them into a super host, and overall, driving the company’s profits. 
 
### Value of the predictions: 
 
By utilizing the power of our predictive model, Airbnb, and similar firms can further expand their businesses in new geographical locations across the world. They don’t have to take the risk of a failed expansion resulting from uncertainty of various factors pertaining to the new location. By augmenting more variables relating to these factors, we can make the current predictive model adjust to the new location and therefore drive those predictions with a high perfect_rating_score to exactly find those properties that have a high probability of resulting in a perfect rating score in the future; if bought and rented out as a listing. 
  
However, it is to be noted that since the model’s True positive rate (TPR) is not very significant we cannot entirely rely on the positive ‘Yes’ predictions to make a decision of buying out a property. We would need to consider a lot of other market factors as well. However, since our model has a low False positive rate (FPR) of < 10%, it significantly reduces the risk of buying out those properties that would otherwise result in a bad rating score and thereby result in a potential loss for the company.  This means that our model can support a risk-averse business strategy for incumbent firms that are trying to survive in the market. 
 
In addition to the model acting as a guide in driving a higher ROI, it can also aid in the process of pinpointing the necessary steps that need to be taken to improve the current listings that are not receiving higher ratings. This implies that we can specifically target certain aspects of the listings and alter them by just the right amount via investing in underperforming areas to drive a higher number of perfect rating scores. 


## Data Understanding and Data Preparation 
 
 
| ID | Feature Name | Brief Description | R Code Line Numbers |
|----|--------------|---------------------|----------------------|
| 1 | accommodates | Original feature from dataset | 1-5 |
| 2 | availability_365 | Original feature from dataset | 200-204 |
| 3 | bed_type | Original feature from dataset | 131 |
| 4 | availability_30 | Original feature from dataset | 200-204 |
| 5 | availability_90 | Original feature from dataset | 200-204 |
| 6 | bathrooms | Original feature from dataset | 141 |
| 7 | bedrooms | Original feature from dataset | 101 |
| 8 | beds | Original feature from dataset | 104 |
| 9 | cancellation_policy | Original feature from dataset | 95 |
| 10 | cleaning_fee | Original feature from dataset | 96 |
| 11 | extra_people | Original feature from dataset | 84 |
| 12 | guests_included | Original feature from dataset | 200-204 |
| 13 | host_listings_count | Original feature from dataset | 98 |
| 14 | instant_bookable | Original feature from dataset | 200-204 |
| 15 | ppp_ind | New feature | 126 |
| 16 | has_min_nights | New feature | 146 |
| 17 | host_is_superhost | Original feature from dataset | 106 |
| 18 | host_identity_verified | Original feature from dataset | 107 |
| 19 | has_extra_fee | New feature | 115 |
| 20 | host_response | Original feature from dataset | 143 |
| 21 | room_type | Original feature from dataset | 130 |
| 22 | is_location_exact | Original feature from dataset | 200-204 |
| 23 | is_available | New feature | 102 |
| 24 | no_rules | New feature | 103 |
| 25 | market | Modified feature | 158 |
| 26 | maximum_nights | Original feature from dataset | 200-204 |
| 27 | minimum_nights | Original feature from dataset | 200-204 |
| 28 | monthly_available | New feature | 157 |
| 29 | price | Original feature from dataset | 97 |
| 30 | require_guest_phone_verification | Original feature from dataset | 200-204 |
| 31 | require_guest_profile_picture | Original feature from dataset | 200-204 |
| 32 | requires_license | Original feature from dataset | 200-204 |
| 33 | weekly_available | New feature | 156 |
| 34 | Amenities | Modified feature as dummy | 76-79 |
| 35 | transit_available | New feature | 155 |
| 36 | square_feet | New feature (from external dataset)* | 192-196 |
| 37 | is_available | New feature | 98 |
| 38 | is_available_60 | New feature | 99 |
| 39 | is_available_90 | New feature | 100 |
| 40 | is_available_365 | New feature | 101 |
| 41 | no_rules | New feature | 103 |
| 42 | beds | Modified feature | 104 |
| 43 | host_is_superhost | Modified feature | 105 |
| 44 | host_identity_verified | Modified feature | 106 |
| 45 | zipcode | Modified feature | 107 |
| 46 | smart_location | New feature | 108 |
| 47 | state | Modified feature | 109 |
| 48 | per_day_price_weekly | New feature | 111 |
| 49 | per_day_price_monthly | New feature | 113 |
| 50 | host_total_listings_count | New feature | 114 |
| 51 | host_info_available | New feature | 116 |
| 52 | guests_included | New feature | 118 |
| 53 | has_cleaning_fee | New feature | 126 |
| 54 | has_deposit | New feature | 128 |


## Graphs Demonstrating Useful and Interesting Insights

### 1. Accommodates
- Original feature indicating the number of guests that can stay.
- Cleaned by limiting the maximum number of accommodates to 9.
- The chart below depicts the improved distribution across YES and NO categories.
  
![Accommodations](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/frequency_accomodations.jpg?raw=true)


![Accommodations](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/pr_accommodations.jpg?raw=true)

### 2. Bedrooms
- Original feature from the dataset.
- Limited the number of bedrooms to 6 for a more balanced distribution.


![Bedrooms](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/bedrooms.png?raw=true)


### 3. ppp_ind
- New feature indicating 1 if the price per person (price/accommodates) is greater than the median value, otherwise 0.
- Instances with ppp_ind as 1 have a greater number of perfect_rating_score instances classified as YES.

  
![PPP](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/ppp_ind.jpg?raw=true)

### 4. No_rules
- Added feature with a value of YES if there are no rules in the listing and NO otherwise.
- Listings with no_rules as YES have a greater number of perfect rating scores.

  
![No Rules](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/no_rules.jpg?raw=true)

### 5. Market
- Market feature categorized into: "Los Angeles," "New Orleans," "Boston," "Chicago," "Denver," "San Diego," "San Francisco," "Nashville," "Portland," "Seattle," and "Other" to address dataset bias.

  
![Market](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/market.jpg?raw=true)

### 6. Transit_available
- Modified feature indicating YES if there’s transit available near the listing’s location and NO otherwise.
- Higher NO ratings for listings if there’s no transit available nearby.

  
![transit](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/transit.jpg?raw=true)

### 7. Square_feet (External Data)
- Taken from [External Data](https://www.kaggle.com/datasets/yasserh/housing-prices-dataset?resource=download).
- Imputed square feet area based on the number of bedrooms, filling in 90% missing/NA values.

  
![square_feet](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/square_feet.jpg?raw=true)

### 8. Weekly_available
- Modified feature indicating YES if a listing is rented out on a weekly basis and NO otherwise.
- Better ratings for listings rented out weekly.

  
![weekly](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/weekly.jpg?raw=true)


### 9. Price
- Original feature from the dataset.

  
![Price](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/price.jpg?raw=true)

### 10. Amenities (Dummy Variable)
- Cleaned and converted into dummy variables for better control.
- Chart shows the number of amenities.

  
![Amenities](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/amenities.jpg?raw=true)

### 3) Additional Comments
- Augmented 'square_feet' from external dataset to fill in missing values in the original dataset.
- Improved model performance.
- [Link to external housing data source](https://www.kaggle.com/datasets/yasserh/housingprices-dataset?resource=download).


## Winning Model: Gradient Boosting

The winning model in our case is the Gradient Boosting model. The variables included in the model are:

- accommodates
- availability_365
- bed_type
- availability_30
- availability_90
- bathrooms
- bedrooms
- beds
- cancellation_policy
- cleaning_fee
- extra_people
- guests_included
- host_listings_count
- instant_bookable
- ppp_ind
- has_min_nights
- host_is_superhost
- host_identity_verified
- has_extra_fee
- host_response
- room_type
- is_location_exact
- instant_bookable
- is_available
- no_rules
- market
- maximum_nights
- minimum_nights
- monthly_available
- price
- require_guest_phone_verification
- require_guest_profile_picture
- requires_license
- weekly_available
- TV
- X.Cable.TV.
- Internet
- X.Wireless.Internet.
- X.Air.conditioning.
- Kitchen
- X.Free.parking.on.premises.
- Heating
- X.Family.kid.friendly.
- X.Family.Kid.Friendly.
- Washer
- X.Carbon.Monoxide.Detector.
- Essentials
- Shampoo
- Hangers
- X.Hair.dryer.
- Iron
- X.Laptop.friendly.workspace.
- X.Self.Check.In.
- Keypad
- X.Safety.card.
- X.Hot.water.
- X.Cooking.basics.
- X.Lock.on.bedroom.door.
- Gym
- X.Pets.allowed.
- transit_available
- square_feet.

Based on the relative generalization performance of different models on the validation dataset, the boosting model significantly outperformed the other models with a high accuracy of 0.757 or approximately 75%, TPR of 0.376~ 37%, and FPR of 0.084~ 8%. In addition, it also significantly improved the baseline model performance having a 71% accuracy. Therefore, we went ahead and decided that this was our winning model.

Line numbers in R code: 786-800

## All Models

### 1. Logistic Regression

The first type of model used is Logistic regression. Logistic regression is performed using glm( ) function. Estimated training performance & generalization performance is as below:

#### Training performance:

- Training Accuracy for the logistic model: 0.7298174
- Training TPR: 0.28310524521502
- Training FPR: 0.0847066912017471

#### Generalization performance:

- Validation Accuracy for the logistic model: 0.7299217
- Validation TPR: 0.285039901090255
- Validation FPR: 0.0824722722532941

The best performing set of features in the model include:

- availability_365
- availability_30
- bathrooms
- bedrooms
- beds
- cancellation_policymoderate
- cancellation_policystrict
- cleaning_fee
- extra_people
- guests_included
- instant_bookableTRUE
- ppp_ind1
- has_min_nightsMIN
- has_min_nightsMO
- host_is_superhostTRUE
- marketSeattle
- price
- Internet

Line numbers in the R code where we trained the model: 266 to 306.

### 2. Ridge-Lasso model for logistic regression

The second type of model we used is the Ridge-Lasso model to compensate for the large values of coefficients obtained using the first logistic regression model used. Ridge and lasso models can be implemented by incorporating a new argument while training the logistic regression model.

Estimated training performance & generalization performance is as below:

#### For Ridge:

#### Training performance:

- Training Accuracy for the Ridge model: 0.7297602
- Training TPR for ridge model: 0.273705741976331
- Training FPR for ridge model: 0.080884880593695

#### Generalization performance:

- Generalization Accuracy for the Ridge model: 0.7295883
- Generalization TPR for Ridge model: 0.276385298415196
- Generalization FPR for Ridge model: 0.0792966157929662

  
![ridge](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/ridge.jpg?raw=true)

#### For Lasso:

#### Training performance:

- Training Accuracy for the Lasso model: 0.7297602
- Training TPR for Lasso model: 0.27243948765402
- Training FPR for Lasso model: 0.080359128869836

#### Generalization performance:

- Generalization Accuracy for the Lasso model: 0.7296883
- Generalization TPR for Lasso model: 0.276160503540519
- Generalization FPR for the Lasso model: 0.079059626504882

The best performing set of features include:

- Bathrooms
- X.Air.conditioning.
- X.Free.parking.on.premises.
- Essentials
- X.Laptop.friendly.workspace.
- X.Self.Check.In.
- transit_available.YES (dummy)

Line numbers in the R code where we trained these models:

- Ridge model: 347 to 427
- Lasso model: 438 to 518

The hyperparameters used in these 2 models were a set of 100 values, ranging from 0.0001 to 0.1.


![Lasso](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/lasso.jpg?raw=true)

### 3. Decision Trees

The third type of model we used is the Decision Trees. The library we need to import is ‘trees’ in order to use the tree( ) function. The estimated training performance & generalization performance is as below:

#### Training performance:

- Training Accuracy for the Decision Tree model: 0.7129712
- Training TPR: 0.252325524765012
- Training FPR: 0.0957676986229349

#### Generalization performance:

- Validation Accuracy for the Decision Tree model: 0.7091849
- Validation TPR: 0.248285939080589
- Validation FPR: 0.0964546402502607

The best performing set of features include:

- "availability_365"
- "Internet"
- "host_is_superhostTRUE"
- "host_listings_count"
- "price"
- "host_response.MISSING"
- "monthly_available.YES"
- "instant_bookableTRUE"
- "availability_90"
- "availability_30"
- "minimum_nights"
- "Washer"
- "cancellation_policy.strict"
- "extra_people"
- "X.Wireless.Internet."
- "ppp_ind.1"
- "transit_available.YES"

Line numbers in the R code where we trained these models: 638 to 675


![tree](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/tree.jpg?raw=true)

#### Fitting curve for decision tree:

#### [Insert fitting curve image here]

### 4. Gradient Boosting Model (Winning model)

The fourth type of model we used is the Gradient Boosting model which belongs to the family of ensemble methods in machine learning. The library we need to import is ‘gbm’ in order to use the gbm( ) function. The estimated training performance & generalization performance is as below:

#### Training performance:

- Training Accuracy for the Boosting Model: 0.7576515
- Training TPR for Boosting model: 0.376710660887352
- Training FPR for Boosting model: 0.0841809394778881

#### Generalization performance:

- Validation Accuracy for the Boosting Model: 0.7385898
- Validation TPR for the Boosting Model: 0.346521299314376
- Validation FPR for the Boosting Model: 0.096075457389326

The best performing set of features include:

- Availability_365
- price
- host_listings_count
- Internet
- host_is_superhostTRUE
- minimum_nights
- weekly_available.YES
- cleaning_fee
- availability_30
- maximum_nights

Line numbers in the R code where we trained these models: 722 to 778


![GB](https://github.com/deepakdhole777/airbnb-perfect-rating-score-prediction/blob/main/images/gradient_boosting.jpg?raw=true)


### 5. Random Forest

The last type of model we used is the Random Forest model which belongs to the family of ensemble methods in machine learning. The library we need to import is ‘randomForest’ in order to use the randomForest( ) function. The estimated training performance & generalization performance is as below:

#### Training performance:

- Training accuracy for the Random Forest model: 0.9998428
- Training TPR for the random forest model: 0.999512979106804
- Training FPR for the random forest model: 2.0221220148442e-05

#### Generalization performance:

- Validation Accuracy for the Random Forest model: 0.7311219
- Validation TPR for the Random forest model: 0.313813645048893
- Validation FPR for the Random forest model: 0.092899800928998

The best performing set of features include:

- Availability_365
- price
- market
- cleaning_fee
- availability_90
- square_feet
- maximum_nights
- availability_30
- extra_people

Line numbers in the R code where we trained these models: 523 to 573


