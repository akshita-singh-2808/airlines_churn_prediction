# ✈️ Airline Loyalty Churn Intelligence

### Live Dashboard

https://airlines-churn-prediction-model.streamlit.app/

---

## The Business Challenge

Airlines invest heavily in loyalty programs to retain customers and encourage repeat travel. Yet many members quietly disengage long before they formally cancel their membership.

This creates a difficult business problem:

* Which customers are likely to leave?
* Which members are worth prioritizing for retention?
* What actions should the business take before valuable customers are lost?

To answer these questions, I analyzed airline loyalty and flight activity data and built a churn intelligence system that combines predictive analytics, customer segmentation, and retention recommendations.

---

## The Data

The analysis uses loyalty and flight activity data for approximately 16,700 airline loyalty members between 2012 and 2018.

The dataset includes:

* Customer demographics
* Loyalty program information
* Customer Lifetime Value (CLV)
* Monthly flight activity
* Distance traveled
* Loyalty points earned and redeemed
* Enrollment and cancellation history

---

## From Raw Data to Business Insights

The project began with extensive data cleaning and exploratory analysis to understand how customer behavior changes over time.

Several patterns quickly emerged:

### High-Risk Customers Show Declining Activity

Customers who gradually reduced their flight frequency were significantly more likely to churn.

### Formal Membership Doesn't Equal Engagement

Many members remained enrolled in the loyalty program despite showing little or no flight activity.

### Loyalty Status Matters

Higher-tier loyalty members generally displayed stronger retention behavior and lower churn rates.

### Redemption Behavior Signals Engagement

Members who actively redeemed rewards tended to remain more engaged with the program.

---

## Building a Churn Prediction Framework

Rather than relying only on cancellation records, churn was defined using a behavioral approach that captures both explicit and silent disengagement.

A customer was considered churned if they:

* Formally cancelled membership
* Became inactive for an extended period
* Never meaningfully engaged with the program

This allowed the model to identify risk before customers were officially lost.

---

## Feature Engineering

To better capture customer behavior, several business-focused features were created:

### Activity Features

* Total Flights
* Activity Rate
* Flight Trend
* Months Since Last Flight
* Seasonal Flight Activity

### Loyalty Features

* Redemption Ratio
* Loyalty Tier Encoding
* Promotion Enrollment Indicators

### Customer Value Features

* Customer Lifetime Value (CLV)
* Tenure
* Engagement Patterns

These features transformed raw transactional data into meaningful indicators of customer health.

---

## Customer Segmentation

Beyond churn prediction, members were grouped into actionable business segments:

* New At-Risk Members
* Dormant Members
* High Value Vulnerables
* Stable Regulars

Each segment represents a different retention challenge and requires a different intervention strategy.

---

## Retention Strategy Design

The goal was not simply to predict churn but to recommend actions that business teams could implement.

Examples include:

### New At-Risk Members

Early win-back campaigns with limited-time incentives.

### Dormant Members

Personalized route-based offers designed to reactivate travel behavior.

### High Value Vulnerables

Premium retention programs, upgrade vouchers, and proactive outreach.

### Stable Regulars

Tier-progression campaigns that deepen loyalty and increase lifetime value.

---

## Interactive Dashboard

To make the analysis accessible to non-technical stakeholders, a Streamlit dashboard was developed featuring:

* Executive KPI overview
* Churn risk monitoring
* At-risk member identification
* Individual customer lookup
* Segment-specific retention playbooks

The dashboard translates analytical outputs into decisions that marketing and loyalty teams can act on immediately.

---

## Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Streamlit
* Plotly

---

## Project Structure

```text
airlines_churn_prediction/
│
├── Dataset/
├── Notebooks/
├── images/
├── app.py
├── requirements.txt
└── README.md
```

---

## Future Enhancements

* Gradient Boosting and XGBoost models
* SHAP-based model explainability
* Automated retention recommendation engine
* Time-series churn forecasting
* Real-time dashboard integration
* Campaign impact measurement
