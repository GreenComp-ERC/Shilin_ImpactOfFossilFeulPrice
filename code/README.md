# Code

## Overview 

The purpose of this code is to study the impact of future fossil fuel prices on the weighted average cost of capital (WACC) in the process of energy transition. By predicting fossil fuel prices in different scenarios and combining WACC calculation and analysis, the code provides a comprehensive approach to explore the relationship between market sentiment, historical data, and future capital costs in the energy economy. Specific tasks include: processing WACC and historical fossil fuel price , predicting future fossil fuel prices using LSTM and GRP model, building a  autoML analysis to evaluate the impact.

## Files Included
1.[Average_Coal_Price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_Coal_Price.xlsx)

Functionality: Cotains the historical coal price, which is used to predict future coal price.

2.[Average_Gas_price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_Gas_price.xlsx)

Functionality: Cotains the historical natural gas price, which is used to predict future natural gas price.

3.[Average_oil_price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_oil_price.xlsx)

Functionality: Cotains the historical oil price, which is used to predict future oil price.

4. [Euope_WACC.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Euope_WACC.xlsx)

Functionality: Cotains Both anual WACC data in Europe and coresponding fossil fuel price data. It will be used to evluate the impactr of fossil fuel on the WACC of energy transition projects in Europe, caculating the R^2,RMSE,and MAE.

5. [China_WACC.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/China_WACC.xlsx)

Functionality: Cotains Both anual WACC data in China+ regions and coresponding fossil fuel price data. It will be used to evluate the impactr of fossil fuel on the WACC of energy transition projects in China+ regions, caculating the R^2,RMSE,and MAE.

6. [Middle_EAST_WACC.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Middle_EAST_WACC.xlsx)

Functionality: Cotains Both anual WACC data in Middle East and coresponding fossil fuel price data. It will be used to evluate the impactr of fossil fuel on the WACC of energy transition projects in Middle East, caculating the R^2,RMSE,and MAE.

7. [comprehensive_economic-data](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/comprehensive_economic_data.xlsx)

  Functionality: Used to caculate the inflation rate.  

## Usage Instructions

1. Data Processing

Generate the WACC data and historical fossil fuel data for furteher usage. Specifically, we [reorganize the predicted WACC data](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/WACC_Data_processing.ipynb) from Calcaterra et al. (2024) to find the reginal differences, and [calulate the average anual fossil fuel prices](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/Price_Data_Processing.ipynb).


2. Fossil Fuel Price Prediction

Use LSTM and GRP model to predicte the [fossil fuel price](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/Price_Prediction.ipynb)  from 2026 to 2035 based on historical fossil fuel price.

3. [inflation rate](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/Prediction_Inflation.ipynb)
   

5. Evaluate The Impact

 Through [alutoMl analysis](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/Impact_FossilFuel.ipynb), this study evaluates how fluctuations in fossil fuel prices affect the WACC of diverse energy transition projects. 

 

## Prerequisites

**Python Version:**  
Python 3.9 or higher is recommended for compatibility with all libraries.

**Required Libraries:**  
- **pandas:** 1.3.0 or higher  
- **numpy:** 1.21.0 or higher  
- **matplotlib:** 3.4.0 or higher  
- **scikit-learn:** 0.24.0 or higher  
- **tensorflow:** 2.5.0 or higher  
- **scipy:** 1.6.0 or higher  
- **keras:** 2.4.3 or higher  
- **openpyxl:** 3.0.0 or higher  
- **requests:** 2.25.0 or higher  
- **datetime:** Python standard library (no installation required)  

You can install the required libraries with the following `pip` command:

```bash
pip install pandas numpy matplotlib scikit-learn tensorflow scipy keras openpyxl requests

 ```

## [System Configuration](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/System%20Configuration%20Report.ipynb)

## Contributors
1. Calcaterra et al. (2024): provide the dataset and evaluation modle of wacc.

2. World Band: Provide the historical data for fossil fuel price.

 


