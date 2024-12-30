# Data

## The source and purpose of the datase
The data used for this analysis comes from two primary sources: the WACC data from Calcaterra et al. (2024) and historical fossi fuel(oil,coal, natural gas) price from the dataset of World Bank.

The purpose of using the historical price dataset is to predict the trend of fossil fuel price prices from 2025 to 2100. Specifically, it will be used as the input to the [LSTM and GRP modle](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/tree/main/code). Then, these predicted results will be integrated with the WACC (weighted average cost of capital) forecast results in Calcaterra et al. (2024), which represent the economic conditions under different energy transition scenarios.

The main goal of this analysis is to explore the impact of fossil fuel price fluctuations on future WACC of energy transition projects. By comparing the predicted prices with the estimated WACC results, we can analyze the potential impact of fossil fuel price fluctuations on capital costs, which is a key factor in energy infrastructure investment decision-making. This analysis will provide important insights to help us understand how oil price fluctuations affect the formulation of future energy transition strategies and changes in the financing environment.

## Preprocessing and harmonization step
1. Price Prediction

This study collect price sourses from dataset of World Bank, getting the historical price data for [oil](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_oil_price.xlsx),[coal](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_Coal_Price.xlsx), and [natural gas](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Average_Gas_price.xlsx). And use it for [price prediction](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/tree/main/code).And get the predicted [oil](https://raw.githubusercontent.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/refs/heads/main/data/oil-predictions_with_confidence_intervals.csv),[coal](https://raw.githubusercontent.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/refs/heads/main/data/coal_price_predictions_with_confidence_intervals.csv),and [natrual gas](https://raw.githubusercontent.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/refs/heads/main/data/natural_gas_price_predictions_with_confidence_intervals.csv) data from 2025 to 2100 with its 95% confidence interval.

2. Impact Evaluation

Then, this study combine the prediction reslt with Calcaterra et al. (2024)'s [WACC dataset](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/CalcaterraEtAl_2024_NatEner_data_ED_fig22.csv). Subsequently， after data processing, we get the  WACC values with its coresponding predicted fossil fuel data in [Europe](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Euope_WACC_And_Predicted_Price.xlsx), [Chinas+ regions](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/China%2B_WACC_And_Predicted_Price.xlsx), [Middel East](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Middle_EAST_WACC_And_Predicted_Price.xlsx), and [all transition countries](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Transition_WACC_And_Price.xlsx).

3. Result

Finally, we get [result](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/blob/main/data/Result.xlsx) which demosntrates the imapct of fossil fuel price on WACC of energy transition projects in specificaal regions.
