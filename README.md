# Predicting Patient No Shows

When patients don't show up for their appointments, in capacity constrained clinics and hospitals, both the provider's time and physical space goes unused. This 1,557 feature model attempts to predict whether or not a patient will show up for an appointment.

## Getting Started

Consider this a template and a starting point for designing your own model. I did my own feature engineering represented in SQL, which required a combination of clinical process knowledge as well as automated appointment exclusion. Your features may vary, and you will need to adjust the one-hot encoding for your own project.

### Prerequisites

Numpy
SQLalchemy
Scipy

```
Give examples
```

### Installing

This is run locally and scheduled to push data into a datawarehouse. Deploying this model on a high-availability server and automating the model to push data in your data warehouse is the best route. You can then abstract and the P-value and use it however you see fit.

## Running the tests

Tests are contained within the cells; RandomForestClassifier, GradientBoostingClassifier, and AdaBoostClassifier are all represented and executable.

In production, I selected RandomForestClassifier as it returns the highest P-value and AUC score. YMMW.

## Built With

Python
Conda
Jupyter Notebook

## Contributing

Chris Jackson

## Authors

Galen Busch
