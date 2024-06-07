# SyriaTel-Churn-Predictor
# Customer Churn Prediction for SyriaTel

## Overview
In this project, I developed a classifier to predict customer churn for SyriaTel, a telecommunications company. Customer churn refers to customers who are likely to discontinue their services in the near future, posing a significant financial impact on the company. By utilizing predictive modeling techniques, I aimed to identify patterns and trends within customer behavior and usage data to forecast whether a customer is at risk of churning. This analysis seeks to discover predictable patterns that can empower the telecom business to optimize customer retention efforts and enhance overall profitability.

![Churn Output](Images/churn_out.jpg)

## Business Understanding
SyriaTel is struggling with a substantial challenge: customer churn, which directly impacts their financial performance. To address this issue, they've initiated a predictive analytics project aimed at identifying customers at risk of churn in the near future. Leveraging historical customer data encompassing demographic information, usage patterns, and service interactions, I constructed a binary classifier model. This model, iteratively refined using various machine learning algorithms, provides real-time predictions of churn likelihood, enabling SyriaTel to proactively engage with at-risk customers through personalized retention strategies. Ultimately, this predictive approach empowers SyriaTel to optimize marketing efforts, enhance customer retention initiatives, and drive overall profitability.

![Exploration](Images/exploration.jpg)

## Data Understanding
The dataset used in this project includes a wide range of features related to customer demographics, usage patterns, and service interactions. Key features include account length, number of voicemail messages, total day minutes, total day calls, total evening minutes, total evening calls, total international minutes, total international calls, total night minutes, total night calls, customer service calls, and the churn target variable.

## Data Analysis
![Baseline ROC Curve](SyriaTel-Churn-Predictor/baseline%20roc.png)

![Optimized Logistic Regression ROC Curve](SyriaTel-Churn-Predictor/optimized%20logreg.png)

![Random Forest ROC Curve](SyriaTel-Churn-Predictor/randomforest.png)

![Optimized Random Forest ROC Curve](SyriaTel-Churn-Predictor/optimised%20randomforest.png)





## Evaluation
I developed and evaluated four models: a baseline logistic regression model, an optimized logistic regression model, a baseline random forest model, and an optimized random forest model. 

The baseline logistic regression model, with an F1 score of 0.29 and an accuracy of 0.86, showed good performance in predicting non-churning customers but struggled with identifying customers likely to churn. The optimized logistic regression model improved significantly, achieving a weighted average F1 score of 0.91 and an overall accuracy of 0.91. This improvement was achieved through hyperparameter tuning and addressing class imbalance using SMOTE.

Moving to ensemble methods, the baseline random forest model achieved an impressive F1 score of 0.97 and an accuracy of 0.97. The model's AUC of 1.0 suggested perfect discriminatory power, though it raised concerns about potential overfitting. The optimized random forest model maintained this high performance with a more generalizable solution, showing an AUC of 0.99, precision and recall of 0.97 for both classes, and a mean cross-validation weighted F1 score of 0.95.

## Conclusion and Recommendation
 
 ![Customer Churn](Images/acha%20kuchurn%20macusto.jpg)

The evaluation of the four models revealed significant improvements in predictive performance through model optimization techniques. The optimized logistic regression model showed enhanced accuracy and F1-scores, while the optimized random forest model demonstrated superior performance with high precision, recall, and a robust AUC of 0.99. Based on this comprehensive evaluation, I recommend deploying the optimized random forest model to predict customer churn. This model offers a balanced and highly accurate solution with consistent performance across various metrics. It effectively handles class imbalance and leverages feature selection to enhance predictive capabilities.

The top features driving customer churn include total day minutes, number of voicemail messages, total evening minutes, account length, total day calls, and total evening calls. To maintain and further improve model performance, I recommend regularly evaluating the model with new data, periodically retraining the model to capture changes in customer behavior, exploring additional features or external data sources, and deploying the model in a real-time environment to enable proactive customer retention strategies.

By following these recommendations, I believe SyriaTel can effectively predict and mitigate customer churn, ultimately enhancing customer retention and business performance.

