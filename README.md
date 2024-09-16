# 5G Energy Consumption Modelling with Lasso Regression

## Description
This project focuses on predicting energy consumption at 4G/5G cell sites using a dataset provided by the International Telecommunication Union (ITU) as part of a global challenge for data scientists. The dataset contains cell-level traffic statistics collected on different days. I apply Lasso Regression to model and predict the energy consumption based on traffic and other site-related features.

## Dataset
This dataset contains the following features:
- **Date**: date and time which the measurement was collected
- **BS**: name of the base station
- **Energy**: enery consumption measurement
- **load**: load of the cell. It takes a value in [0-1]
- **ESMODE**: Intensity of the activation of different energy-saving modes. It takes value in [0-1]
- **TXpower**: Maximum transmit power of the cell

### Data Preprocessing
To ensure that the dataset is clean and ready for modelling, the followin steps were taken:
1. Handling outliers
Outliers in the numerical features were identified using boxplots and handled using the Interquartile Range (IQR) method.
2. Encoding categorical columns
Since the BS column (representing base stations) was categorical, it was encoded using Target Encoding, which takes into account the relationship between the base station and the energy consumption.
The time column was split to extract time-based features such as:
- Hour of the day
- Month
- Year
- Day of the week
- Weekends

Since time-based features like hour, day, and month have a cyclical nature (e.g., hours repeat every 24 hours, and months every 12 months), these features were encoded cyclically.This ensured that the model could capture the periodic nature of time.

3. Dropped unnecessary columns: `Time`, `BS`, and `Date`.
4. Selected `Energy` as the target variable for prediction.
5. Split the dataset into training and testing sets using an 80/20 split.
6. Normalized the feature data using `StandardScaler` for better model performance.

## Requirements
To run the project, you'll need the following Python libraries:
- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`
- `ydata-profiling`

Install the required packages using pip:
```bash
pip install numpy pandas matplotlib scikit-learn ydata-profiling



