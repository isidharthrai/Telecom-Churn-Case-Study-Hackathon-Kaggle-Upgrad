# Telecom Churn Prediction

**Author**: [Sidharth_Rai](https://github.com/isidharthrai)  
**Competition Link**: [Telecom Churn Case Study Hackathon](https://www.kaggle.com/competitions/telecom-churn-case-study-hackathonc62/overview)

## Problem Statement
In the telecom industry, customers can choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

## Understanding Customer Behaviour During Churn
Customers usually do not decide to switch to another competitor instantly, but rather over a period of time (this is especially applicable to high-value customers). In churn prediction, we assume that there are three phases of the customer lifecycle:

1. **The ‘Good’ Phase**: The customer is happy with the service and behaves as usual.
2. **The ‘Action’ Phase**: The customer experience starts to decline, e.g., they receive a compelling offer from a competitor, face unjust charges, or become unhappy with service quality. During this phase, the customer usually shows different behavior than in the ‘good’ months. Identifying high-churn-risk customers in this phase is crucial since corrective actions can be taken (e.g., matching the competitor’s offer or improving service quality).
3. **The ‘Churn’ Phase**: The customer is said to have churned. Churn is defined based on this phase. It is important to note that at the time of prediction (i.e., the action months), data from this phase is not available for prediction. Thus, after tagging churn as 1/0 based on this phase, all data corresponding to this phase is discarded.

## Approach
This project uses a Random Forest model to predict customer churn based on a four-month window of data. The first two months are considered the ‘good’ phase, the third month is the ‘action’ phase, and the fourth month is the ‘churn’ phase.

## Model Results
The Random Forest model achieved a high ROC AUC score of **0.9351** during cross-validation, indicating strong predictive power in distinguishing between customers who are likely to churn and those who are not.

## Conclusion
The model's high ROC AUC score implies that it is highly effective in predicting customer churn, which is critical for the telecom company to implement proactive retention strategies. The optimal hyperparameters suggest that the model benefits from a balance between depth and the number of features considered, enhancing its generalizability to new, unseen data.

## Business Implications
- **Customer Retention**: By deploying this model in a production environment, the telecom company can identify high-risk customers and prioritize retention efforts. This can lead to significant cost savings and revenue protection by reducing the churn rate.
- **Targeted Interventions**: The model allows the company to tailor specific offers, promotions, or customer service interventions to at-risk customers, potentially improving customer satisfaction and loyalty.
- **Data-Driven Decision Making**: The success of this model underscores the importance of data-driven approaches in understanding and mitigating churn, providing a foundation for further analysis and continuous improvement in customer retention strategies.

## Next Steps
- **Model Deployment**: The next step is to deploy this model in a real-time environment to monitor and predict churn on an ongoing basis.
- **Continuous Monitoring**: It is essential to continuously monitor the model's performance and retrain it periodically to account for any changes in customer behavior or market conditions.
- **Further Analysis**: Additional analysis could focus on understanding the key drivers of churn by examining feature importance scores from the Random Forest model, allowing for more targeted business strategies.
