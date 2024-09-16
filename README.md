# 5G Energy Consumption Modelling with Lasso Regression

## Description
This project focuses on predicting energy consumption at 4G/5G cell sites using a dataset provided by the International Telecommunication Union (ITU) as part of a global challenge for data scientists. The dataset contains cell-level traffic statistics collected on different days. We apply Lasso Regression to model and predict the energy consumption based on traffic and other site-related features.

## Dataset
This dataset contains the following features:
- **Date**: date and time which the measurement was collected
- **BS**: name of the base station
- **Energy**: enery consumption measurement
- **load**: load of the cell. It takes a value in [0-1]
- **ESMODE**: Intensity of the activation of different energy-saving modes. It takes value in [0-1]
- **TXpower**: Maximum transmit power of the cell

### Data Preprocessing
