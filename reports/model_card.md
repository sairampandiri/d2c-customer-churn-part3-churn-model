# Model Card

## Model Name

Customer Churn Prediction Model

## Intended Use

This model predicts whether a customer is likely to churn within the next 60 days.

The model is intended to support:

- Retention campaigns
- Customer success interventions
- Marketing prioritization
- Churn monitoring

## Data Used

Dataset:

rfm_modeling_snapshot.csv

Snapshot Date:

2025-09-30

Features Included:

- Customer demographics
- Purchase behavior
- Engagement behavior
- Support interactions
- Marketing engagement

Target:

churn_next_60d

## Leakage Prevention

Only information available on or before the snapshot date was used.

The target variable and split column were excluded from model features.

## Model Approach

Baseline Model:

- Logistic Regression

Final Model:

- Random Forest Classifier
- 300 Trees
- Maximum Depth = 8

## Performance

### Validation Metrics

Accuracy: 0.8006

Precision: 0.7985

Recall: 0.7279

F1 Score: 0.7616

ROC-AUC: 0.8761

### Test Metrics

Accuracy: 0.8214

Precision: 0.7903

Recall: 0.8750

F1 Score: 0.8305

ROC-AUC: 0.8873

Selected Threshold: 0.40

## Key Drivers

Most Important Features:

1. recency_days
2. last_visit_days_ago
3. monetary_180d
4. frequency_180d
5. product_views_30d

## Business Interpretation

Customers who have not purchased recently and have declining engagement are more likely to churn.

High-value customers with reduced activity should be prioritized for retention campaigns.

## Limitations

- Historical behavior may not predict future behavior perfectly.
- Customer preferences can change over time.
- External factors are not captured.

## Ethical Considerations

This model should not be used for:

- Service denial
- Discriminatory targeting
- Customer exclusion

The model should only support retention and engagement decisions.

## Monitoring Requirements

Monitor:

- Data drift
- Feature drift
- Recall degradation
- Campaign effectiveness
- Prediction stability

Retraining should occur periodically as customer behavior evolves.