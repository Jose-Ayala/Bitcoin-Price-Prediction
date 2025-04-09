# Bitcoin Price Prediction Using Chainlet Data and Ridge Regression

This project predicts Bitcoin prices for December 2017 using chainlet data (amount and occurrence) and historical price information. A Ridge Regression model was employed, and SHAP analysis was used to explain the model's predictions.

## Project Overview

This project aims to demonstrate the application of machine learning techniques for time series forecasting, specifically predicting Bitcoin prices. It utilizes historical price data and chainlet features, which represent transaction patterns on the Bitcoin network.

## Files

* `pricedBitcoin2009-2018.csv`: Bitcoin price data from 2009 to 2018.
* `AmoChainletsInTime.txt`: Amount chainlet data from 2009 to 2018.
* `OccChainletsInTime.txt`: Occurrence chainlet data from 2009 to 2018.
* `Bitcoin_Price_Prediction.ipynb`: Jupyter Notebook containing the code for data preprocessing, model training, prediction, and evaluation.
* `price_predictions_ridge.csv`: CSV file containing the predicted Bitcoin prices for December 2017.
* `Bitcoin Price Prediction.pdf` : Report detailing the project.

## Dependencies

* `pandas`
* `scikit-learn`
* `numpy`
* `matplotlib`
* `shap`

## Setup and Installation

1.  Clone the repository:

    ```bash
    git clone [repository_url]
    ```

2.  Install the required packages:

    ```bash
    pip install pandas scikit-learn numpy matplotlib shap
    ```

3.  Ensure that the data files (`pricedBitcoin2009-2018.csv`, `AmoChainletsInTime.txt`, `OccChainletsInTime.txt`) are in the same directory as the Jupyter Notebook.

## Usage

1.  Open the `Bitcoin_Price_Prediction.ipynb` Jupyter Notebook.
2.  Run the cells sequentially to execute the data preprocessing, model training, and prediction steps.
3.  The predicted prices for December 2017 will be saved to `price_predictions_ridge.csv`.
4.  The notebook also generates plots and SHAP analysis to visualize and explain the model's predictions.

## Methodology

1.  **Data Preprocessing:**
    * Loaded and merged the Bitcoin price and chainlet data.
    * Created a lagged price feature.
    * Filtered the data for the year 2017.
    * Selected relevant chainlet features.
    * Split the data into training and testing sets.

2.  **Model Training:**
    * Trained a Ridge Regression model.

3.  **Prediction and Evaluation:**
    * Generated predictions for December 2017.
    * Evaluated the model's performance using Root Mean Squared Error (RMSE).

4.  **SHAP Analysis:**
    * Used SHAP decision plots to explain the model's predictions.

## Results

* The Ridge Regression model achieved an RMSE of 1110.05.
* SHAP analysis revealed that the 'price\_lag1' feature was consistently the most influential in predicting Bitcoin prices.
    * On 2017-12-01, 'price\_lag1' increased the predicted price by approximately 7577 USD.
    * On 2017-12-03, 'price\_lag1' increased the predicted price by approximately 8517 USD.
    * On 2017-12-05, 'price\_lag1' increased the predicted price by approximately 9040 USD.
    * The '1:1\_amo' and '1:1\_occ' chainlet features had a smaller, but still noticeable, impact on the predictions.

## Report

The report, `Bitcoin Price Prediction.pdf`, provides a detailed overview of the project, including the methodology, results, and challenges encountered.

## Author

Jose Ayala
