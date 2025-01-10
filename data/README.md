# Data

## The Source And Purpose Of The Datase
The data used for this analysis comes from two primary sources: the WACC data from Calcaterra et al. (2024) and historical fossi fuel(oil,coal, natural gas) price from the dataset of World Bank.

The purpose of using the historical price dataset is to predict the trend of fossil fuel price prices from 2025 to 2100. Specifically, it will be used as the input to the [LSTM and GRP modle](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/tree/main/code). Then, these predicted results will be integrated with the WACC (weighted average cost of capital) forecast results in Calcaterra et al. (2024), which represent the economic conditions under different energy transition scenarios.

The main goal of this analysis is to explore the impact of fossil fuel price fluctuations on future WACC of energy transition projects. By comparing the predicted prices with the estimated WACC results, we can analyze the potential impact of fossil fuel price fluctuations on capital costs, which is a key factor in energy infrastructure investment decision-making. This analysis will provide important insights to help us understand how oil price fluctuations affect the formulation of future energy transition strategies and changes in the financing environment.

## Dataset And Preprocessing Step

1. [Test](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Predicted_vs_Real_Results_Improved.xlsx)

Initially, this study use the real WACC and fossil fuel price in 2018 to test the accuracy of the modle
  
2. Price Prediction

This study collect price sourses from dataset of World Bank, getting the historical price data for [oil](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_oil_price.xlsx),[coal](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_Coal_Price.xlsx), and [natural gas](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_Gas_price.xlsx). And use it for [price prediction](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/tree/main/code).And get the predicted [oil](https://raw.githubusercontent.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/refs/heads/main/data/oil-predictions_with_confidence_intervals.csv),[coal](https://raw.githubusercontent.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/refs/heads/main/data/coal_price_predictions_with_confidence_intervals.csv),and [natrual gas](https://raw.githubusercontent.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/refs/heads/main/data/natural_gas_price_predictions_with_confidence_intervals.csv) data from 2025 to 2100 with its 95% confidence interval.

3. Impact Evaluation

Then, this study combine the prediction reslt with Calcaterra et al. (2024)'s [WACC dataset](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/CalcaterraEtAl_2024_NatEner_data_ED_fig22.csv). Subsequently， after data processing, we get the  WACC values with its coresponding predicted fossil fuel data in [Europe](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Euope_WACC_And_Predicted_Price.xlsx), [Chinas+ regions](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/China%2B_WACC_And_Predicted_Price.xlsx), [Middel East](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Middle_EAST_WACC_And_Predicted_Price.xlsx), and [all transition countries](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Transition_WACC_And_Price.xlsx).

4. Result

Finally, we get [result](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Result.xlsx) which demosntrates the imapct of fossil fuel price on WACC of energy transition projects in specificaal regions.



## Data Dictionary

| **Variable Name**                         | **Data Type** | **Description**                                  | **Source File**           | **Unit** | **Range**                  | **Remarks**                                      |
|-------------------------------------------|---------------|--------------------------------------------------|---------------------------|----------|----------------------------|--------------------------------------------------|
| Year_month                                | String        | Time period in Year-Month format                 | Average_Coal_Price.xlsx   | N/A      | 1960 to 2024        | Time period of coal price data                  |
| Coal, Australian Coal                     | Float         | Price of Australian Coal                         | Average_Coal_Price.xlsx   | $/mt     | Varies by month and year   | Coal price in Australian market                 |
| South African ** Average Coal Price       | Float         | Price of South African Coal                      | Average_Coal_Price.xlsx   | $/mt     | Varies by month and year   | Coal price in South African market              |
| Year_Month                                | String        | Time period in Year-Month format                 | Average_Gas_price.xlsx    | N/A      | 1960M01 to present         | Time period of gas price data                   |
| Natural gas, US                           | Float         | Natural gas price in the US                      | Average_Gas_price.xlsx    | $/mmbtu  | Varies by month and year   | Price of natural gas in US market               |
| Year_Month                                | String        | Time period in Year-Month format                 | Average_oil_price.xlsx    | N/A      | 1960M01 to present         | Time period of oil price data                   |
| Oil Price, US                             | Float         | Price of oil in the US                           | Average_oil_price.xlsx    | $/bbl    | Varies by month and year   | Price of oil in US market                       |
| Date                                      | String        | Date of prediction                               | coal_price_predictions_with_confidence_intervals2.xlsx | N/A      | Future dates starting from 2025 | Monthly predictions of coal prices              |
| Prediction                                | Float         | Predicted coal price                             | coal_price_predictions_with_confidence_intervals2.xlsx | $/mt     | Varies based on prediction date | Predicted price of coal                         |
| CI Lower                                  | Float         | Lower bound of the 95% confidence interval for coal price | coal_price_predictions_with_confidence_intervals2.xlsx | $/mt     | Varies based on prediction date | Lower bound of the confidence interval for the prediction |
| CI Upper                                  | Float         | Upper bound of the 95% confidence interval for coal price | coal_price_predictions_with_confidence_intervals2.xlsx | $/mt     | Varies based on prediction date | Upper bound of the confidence interval for the prediction |
| Date                                      | String        | Date of prediction                               | natural_gas_price_predictions_with_confidence_intervals.xlsx | N/A      | Future dates starting from 2025 | Monthly predictions of natural gas prices       |
| Prediction                                | Float         | Predicted natural gas price                      | natural_gas_price_predictions_with_confidence_intervals.xlsx | $/mmbtu  | Varies based on prediction date | Predicted price of natural gas                  |
| CI Lower                                  | Float         | Lower bound of the 95% confidence interval for natural gas price | natural_gas_price_predictions_with_confidence_intervals.xlsx | $/mmbtu  | Varies based on prediction date | Lower bound of the confidence interval for the prediction |
| CI Upper                                  | Float         | Upper bound of the 95% confidence interval for natural gas price | natural_gas_price_predictions_with_confidence_intervals.xlsx | $/mmbtu  | Varies based on prediction date | Upper bound of the confidence interval for the prediction |
| Date                                      | String        | Date of prediction                               | oil-predictions_with_confidence_intervals.xlsx | N/A      | Future dates starting from 2025 | Monthly predictions of oil prices               |
| Prediction                                | Float         | Predicted oil price                              | oil-predictions_with_confidence_intervals.xlsx | $/bbl    | Varies based on prediction date | Predicted price of oil                          |
| CI Lower                                  | Float         | Lower bound of the 95% confidence interval for oil price | oil-predictions_with_confidence_intervals.xlsx | $/bbl    | Varies based on prediction date | Lower bound of the confidence interval for the prediction |
| CI Upper                                  | Float         | Upper bound of the 95% confidence interval for oil price | oil-predictions_with_confidence_intervals.xlsx | $/bbl    | Varies based on prediction date | Upper bound of the confidence interval for the prediction |
| Region                                    | String        | Geographical region for the scenario             | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | Africa, etc.                | Region for each scenario                        |
| Scenario                                  | String        | Scenario type for the model                      | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | CoC-reference, etc.         | Scenario type for each region                  |
| Variable                                  | String        | Model variable                                   | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | Onshore, etc.               | The variable for each region and scenario       |
| Year                                      | Integer       | Year of the prediction                           | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | Year     | 2020, 2025, 2030, etc.      | Year for which the data is predicted           |
| scengroup                                 | String        | The grouping of the scenario                     | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | NDC, etc.                   | The scenario group                              |
| IMACLIM                                   | Float         | Prediction based on the IMACLIM model            | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | Varies by year and scenario | Prediction from the IMACLIM model              |
| IMAGE                                     | Float         | Prediction based on the IMAGE model              | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | Varies by year and scenario | Prediction from the IMAGE model                |
| WITCH                                     | Float         | Prediction based on the WITCH model              | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | Varies by year and scenario | Prediction from the WITCH model                |
| maxwacc                                   | Float         | Maximum value for the weighted average cost of capital | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | Varies by year and scenario | Maximum value for the weighted average cost of capital |
| minwacc                                   | Float         | Minimum value for the weighted average cost of capital | CalcaterraEtAl_2024_NatEner_data_ED_fig22.xlsx | N/A      | Varies by year and scenario | Minimum value for the weighted average cost of capital |
| Region                                    | String        | Region where the energy project is located       | Result.xlsx               | N/A      | Transition Countries, etc.  | Geographical region for energy project evaluation |
| Energy                                    | String        | Type of energy                                   | Result.xlsx               | N/A      | Oil, Gas, Coal              | Type of energy for the project                  |
| Project                                   | String        | Type of energy project                           | Result.xlsx               | N/A      | Onshore, CCS, Nuclear, etc. | Type of energy project                          |
| R²                                        | Float         | Coefficient of determination (R squared) for the energy project | Result.xlsx               | N/A      | 0 to 1                     | Goodness of fit for the model                   |
| RMSE                                      | Float         | Root Mean Square Error for the energy project    | Result.xlsx               | N/A      | Positive values            | Measures the accuracy of the model              |
| MAE                                       | Float         | Mean Absolute Error for the energy project       | Result.xlsx               | N/A      | Positive values            | Measures the average magnitude of errors        |
| Year                                      | Integer       | Year of prediction                               | China+_WACC_And_Predicted_Price.xlsx | Year     | 2020, 2025, 2030, etc.      | Year for which the data is predicted           |
| Scenario                                  | String        | Scenario type for the model                      | China+_WACC_And_Predicted_Price.xlsx | N/A      | CoC-reference, etc.         | Scenario type for each region                  |
| Onshore                                   | Float         | WACC or predicted price for onshore projects     | China+_WACC_And_Predicted_Price.xlsx | N/A      | Varies by year and scenario | WACC or predicted price for onshore projects   |
| Offshore                                  | Float         | WACC or predicted price for offshore projects    | China+_WACC_And_Predicted_Price.xlsx | N/A      | Varies by year and scenario | WACC or predicted price for offshore projects  |
| Nuclear                                   | Float         | WACC or predicted price for nuclear projects     | China+_WACC_And_Predicted_Price.xlsx | N/A      | Varies by year and scenario | WACC or predicted price for nuclear projects    |
| CCS                                       | Float         | WACC or predicted price for CCS projects         | China+_WACC_And_Predicted_P

