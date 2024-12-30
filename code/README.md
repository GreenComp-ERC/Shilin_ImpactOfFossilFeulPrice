## Overview 

The purpose of this code is to study the impact of future fossil fuel prices on the weighted average cost of capital (WACC) in the process of energy transition. By predicting fossil fuel prices in different scenarios and combining WACC calculation and analysis, the code provides a comprehensive approach to explore the relationship between market sentiment, historical data, and future capital costs in the energy economy. Specific tasks include: processing WACC and historical fossil fuel price , predicting future fossil fuel prices using LSTM and GRP model, building a  Stacking Regressor analysis to evaluate the impact.

## Files Included
1.[Average_Coal_Price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_Coal_Price.xlsx)

Functionality: Cotains the historical coal price, which is used to predict future coal price.

2.[Average_Gas_price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_Gas_price.xlsx)

Functionality: Cotains the historical natural gas price, which is used to predict future natural gas price.

3.[Average_oil_price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_oil_price.xlsx)

Functionality: Cotains the historical oil price, which is used to predict future oil price.

4. [Transition_WACC_And_Price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Transition_WACC_And_Price.xlsx)

Functionality: Cotains Both anual WACC data in transition countries and coresponding fossil fuel price data. It will be used to evluate the impactr of fossil fuel on the WACC of energy transition projects in transition countries, caculating the R^2,RMSE,and MAE.

5. [Euope_WACC_And_Predicted_Price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Euope_WACC_And_Predicted_Price.xlsx)

Functionality: Cotains Both anual WACC data in Europe and coresponding fossil fuel price data. It will be used to evluate the impactr of fossil fuel on the WACC of energy transition projects in Europe, caculating the R^2,RMSE,and MAE.

6. [China+_WACC_And_Predicted_Price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/China%2B_WACC_And_Predicted_Price.xlsx)

Functionality: Cotains Both anual WACC data in China+ regions and coresponding fossil fuel price data. It will be used to evluate the impactr of fossil fuel on the WACC of energy transition projects in China+ regions, caculating the R^2,RMSE,and MAE.

7. [Middle_EAST_WACC_And_Predicted_Price.xlsx](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Middle_EAST_WACC_And_Predicted_Price.xlsx)

Functionality: Cotains Both anual WACC data in Middle East and coresponding fossil fuel price data. It will be used to evluate the impactr of fossil fuel on the WACC of energy transition projects in Middle East, caculating the R^2,RMSE,and MAE.


## Usage Instructions

1. Data Processing

Generate the WACC data and historical fossil fuel data for furteher usage. Specifically, we [reorganize the predicted WACC data](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/WACC_Data_processing.ipynb) from Calcaterra et al. (2024) to find the reginal differences, and [calulate the average anual fossil fuel prices](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/Price_Data_Processing.ipynb).

2. Fossil Fuel Price Prediction

Use LSTM and GRP model to predicte the [oil](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/Oil_Price_Prediction.ipynb), [coal](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/coal_Prediction.ipynb), [natral gas](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/Natural_Gas_Prediction.ipynb) price from 2035 to 2100 based on historical fossil fuel price.

3. Evaluate The Impact

 Through Stacking Regressor analysis, this study evaluates how fluctuations in fossil fuel prices affect the WACC of diverse energy transition projects. Specifically, this study utilize concentrates on regional differences, evaluating the impactr of fossil fuel in [Europe](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/The_Impact_Of_Fossil_fuel_Europe.ipynb),[China+ regions](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/The_Impact_Of_Fossil_Fuel_In_China%2B.ipynb), [Middle East](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/The_Impact_Of_Fossil_fuel_In_Middle_East.ipynb), and [all transition countries](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/code/The_Impact_of_Fossil_fuel_In_Transition_Countris.ipynb).

 

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

## Expected Output

According to the model,  from 2025 to 2100, fossil fuel prices (natural gas, oil, and coal) are expected to follow distinct trends. Natural gas prices will likely fluctuate between 6 and 18 dollars per unit, reflecting market uncertainty. Oil prices are predicted to decline steadily from 76 dollars per barrel in 2025 to 62 dollars by 2100, with periodic short-term fluctuations. Coal prices are projected to rise initially from 125 to 130 dollars per unit before stabilizing at a relatively high level.

Europe shows a consistently high average R² value of 0.3297 in transition projects, indicating robust WACC responses to fossil fuel price fluctuations (\ref{Result_Europe}). Europe also has a higher proportion of non-zero R² projects, suggesting greater sensitivity to fossil fuel price variations. Additionally, lower RMSE and MAE values indicate smaller prediction errors, demonstrating higher stability and accuracy.

The mean R² value for the China+ region is 0.2195 (\ref{Result_China+}), lower than Europe's 0.3297  but still above the global average. Notably, the R² value for natural gas in solar projects within the China+ region reaches 0.8839, indicating an exceptionally strong model fit and robust correlation. Additionally, the China+ region has smaller RMSE and MAE values, suggesting higher accuracy and stability in predictive models.

Results from the Middle East region show a low model fit, with an average R² of 0.135 , lower than in other regions. Prediction errors (RMSE and MAE) are also higher, indicating that capital costs of energy transition projects in the Middle East are less influenced by fossil fuel price fluctuations.

## Contributors
1. Calcaterra et al. (2024): provide the dataset and evaluation modle of wacc.

2. World Band: Provide the historical data for fossil fuel price.

 


