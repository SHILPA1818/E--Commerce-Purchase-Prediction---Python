E- Commerce Purchase Prediction - Python

## E-commerce Customer buying prediction
This project creates a machine learning model that is used to indicate the likelihood of a customer purchasing an item after browsing online.
The mission is to assist companies in increasing the conversion rate, enhancing user experience, and optimization of marketing expenditure.

## Objective
This problem is a binary classification problem:
- 1 - customer will purchase
- 0 - customer will not purchase

The goal is to construct and optimize a model to predict the purchase intent well and aid in the making of business decisions.

## Dataset Overview
- 10,000 customer sessions
- 26 features
- 2,000 missing values
- Purchase rate: 51 percent (balanced dataset)
- The characteristics are behavioral (page views, cart activity), temporal (time, day) and categorical (device, traffic source).


## Methodology 
- Handled missing values, encoding, scaling, performed data preprocessing.
- Developed attributes that concentrate on customer interaction.
- Modeled various models: Logistic Regression, Random Forest, Gradient Boosting.
- Gradient Boosting Selected on best ROC-AUC.
- GridSearchCV Applied hyperparameter tuning.
- Assessed model with the help of confusion matrix, ROC curve and classification metrics.

## Exploratory Data Analysis

1) This plot shows the distribution of users who made a purchase versus those who did not. The dataset is relatively balanced, with a slightly higher number of purchases, which is beneficial for training a classification model without bias toward one class.

![image alt](https://github.com/shilpav1-ship-it/DS602/blob/88adaf106b0e25c8a2cd34a808553efec278c2cb/Midterm_project/purchase_distribution.png)


2) This plot shows that users who add more items to their cart are more likely to complete a purchase. Although there are some outliers, the overall trend indicates that cart activity is a strong indicator of buying intent.

![image alt](https://github.com/shilpav1-ship-it/DS602/blob/88adaf106b0e25c8a2cd34a808553efec278c2cb/Midterm_project/cart_items.png)


3) This plot shows how purchase probability varies across different hours of the day. There are noticeable fluctuations, suggesting that user purchasing behavior depends on time, with certain hours showing higher conversion rates.

![image alt](https://github.com/shilpav1-ship-it/DS602/blob/88adaf106b0e25c8a2cd34a808553efec278c2cb/Midterm_project/hour_purchase.png)


4) This histogram shows that most users have low page views, but users with higher page views are more likely to make a purchase. This suggests that higher engagement increases the likelihood of conversion.

![image alt](https://github.com/shilpav1-ship-it/DS602/blob/88adaf106b0e25c8a2cd34a808553efec278c2cb/Midterm_project/page_views.png)


5) This boxplot compares session duration for purchasers and non-purchasers. Users who make a purchase generally have higher session durations, indicating that increased time spent on the website is associated with higher purchase intent.

![image alt](https://github.com/shilpav1-ship-it/DS602/blob/88adaf106b0e25c8a2cd34a808553efec278c2cb/Midterm_project/session_duration.png)


6) This chart shows conversion rates across different traffic sources. Email and paid search have higher conversion rates, indicating they bring more high-intent users, while social media has a comparatively lower conversion rate.

![image alt](https://github.com/shilpav1-ship-it/DS602/blob/88adaf106b0e25c8a2cd34a808553efec278c2cb/Midterm_project/traffic_source.png)


## Performance 

**ROC-AUC:** 0.63
- Determines the efficiency of the model in separating buyers and non-buyers.
- A 0.63 is a moderate score indicating that the model does a moderate job in separating the two groups.
  
Precision: 0.60
Out of all the customers that were predicted to buy, 60% actually did.
This shows that the model has a moderate level of accuracy in selecting the correct customers.
Recall: 0.66
The model is able to select 66% of actual buyers.
This shows that the model is good at selecting the correct potential customers.
F1 Score: 0.63
The F1 Score is a measure that balances precision and recall.
Having a score of 0.63 shows that the model is well-balanced.
Accuracy: 0.60
The model has a high predictive accuracy of 60%.
This shows that the model has a moderate level of performance.
Overall:
The model has a high recall rate, meaning that it is good at selecting a majority of the potential customers.
This is good for maximizing the opportunities for conversion.
However, the moderate precision rate shows that there are some false positives, meaning that some marketing efforts may be going to waste for some customers who may not buy.




## Key Insight
The most predictive of purchase is customer engagement.
Such characteristics as the length of the session, cart activity, and page views play a crucial role in making purchases.


The most important feature is the number of items added to the cart, followed by time spent on the site, showing that more active users have a higher chance of making a purchase. This helps businesses identify high-intent customers and target them with personalized offers to improve conversion rates
![image alt](https://github.com/shilpav1-ship-it/DS602/blob/88adaf106b0e25c8a2cd34a808553efec278c2cb/Midterm_project/feature_importance.png)

## Business Recommendations
- Select high-probability users (e.g., larger than 0.7) to make marketing more efficient.
- Create groups of high, medium and low intent users.
- Personalized offers to high-intent customers.
- Cut expenses on low-intent users.
- Facilitate real time customization to maximize conversions.

## Conclusion
Gradient Boosting emerged as the best-performing model based on both test and cross-validation ROC-AUC scores, with further improvements after hyperparameter tuning. Key drivers of purchase behavior include session duration, page views, clicks, and items added to cart.

By leveraging predicted probabilities, businesses can identify high-intent customers and target them with personalized offers using a defined threshold (e.g., 0.5). This approach enables more efficient marketing spend, better customer targeting, and ultimately improved conversion rates.
