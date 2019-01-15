# Predicting Patient No Shows

When patients don't show up for their appointments, in capacity constrained clinics and hospitals, both the provider's time and physical space goes unused. This 1,557 feature model attempts to predict whether or not a patient will show up for an appointment.

## Getting Started

Consider this a template and a starting point for designing your own model. I did my own feature engineering represented in SQL, which required a combination of clinical process knowledge as well as automated appointment exclusion. Your features may vary, and you will need to adjust the one-hot encoding for your own project.

### Prerequisites

Numpy
SQLalchemy
Scipy

### Installing

This is run locally and scheduled to push data into a SSMS data warehouse. This model on a high-availability server with an automated push to the data warehouse. You can then leverage and the P-value, F1 score, and AUC to gauge backtesting. 

## Running the tests

Tests are contained within the cells; RandomForestClassifier, GradientBoostingClassifier, and AdaBoostClassifier are all represented and executable.

Due to the lengthy training duration and lack of GPU acceleration, this model is re-trained monthly. Automated model selection was explored with several regression models, however stakeholders required clear documentation of this prediction process; making automated model selection impossible. By way of automated feature selection based on F-score, the total runtime was reduced 72%. 

In production, I selected RandomForestClassifier as it returns the highest P-value and AUC score. YMMW.

## Built With

Python,
Conda,
Jupyter Notebook

## Authors

Galen Busch
