# Error Analysis

## Overview

The model was evaluated using a threshold of 0.40.

Errors fall into two categories:

- False Positives
- False Negatives

---

# False Positive Analysis

## Customer ID: CUST00044

Actual: Not Churn

Predicted: Churn

Probability: 0.484

Reason:

Customer showed inactivity signals that resembled churn behavior.

Business Risk:

Unnecessary retention cost.

---

## Customer ID: CUST00109

Actual: Not Churn

Predicted: Churn

Probability: 0.591

Reason:

Low purchase frequency and declining engagement increased predicted risk.

Business Risk:

Marketing resources spent unnecessarily.

---

## Customer ID: CUST00335

Actual: Not Churn

Predicted: Churn

Probability: 0.657

Business Risk:

Retention offer may be unnecessary.

---

## Customer ID: CUST00437

Actual: Not Churn

Predicted: Churn

Probability: 0.871

Business Risk:

High confidence but incorrect prediction.

---

## Customer ID: CUST00491

Actual: Not Churn

Predicted: Churn

Probability: 0.596

Business Risk:

Potential over-allocation of retention budget.

---

# False Negative Analysis

## Customer ID: CUST00184

Actual: Churn

Predicted: Not Churn

Probability: 0.078

Reason:

Customer exhibited healthy engagement metrics before unexpectedly churning.

Business Risk:

Lost opportunity for intervention.

---

## Customer ID: CUST00247

Actual: Churn

Predicted: Not Churn

Probability: 0.359

Business Risk:

Retention campaign not triggered.

---

## Customer ID: CUST00414

Actual: Churn

Predicted: Not Churn

Probability: 0.329

Business Risk:

Customer churned without warning.

---

## Customer ID: CUST00438

Actual: Churn

Predicted: Not Churn

Probability: 0.290

Business Risk:

Lost revenue opportunity.

---

## Customer ID: CUST00592

Actual: Churn

Predicted: Not Churn

Probability: 0.269

Business Risk:

Customer left without receiving retention outreach.

---

# Business Conclusion

False Negatives are more costly than False Positives because churned customers represent lost revenue.

For this reason, the model threshold was reduced to 0.40 to improve recall and identify more potential churners.