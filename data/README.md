# Data

## The source and purpose of the datase
The data used for this analysis comes from two primary sources: the WACC data from Calcaterra et al. (2024) and historical fossi fuel(oil,coal, natural gas) price from the dataset of World Bank.

The purpose of using the historical price dataset is to predict the trend of fossil fuel price prices from 2025 to 2100. Specifically, it will be used as the input to the [LSTM and GRP modle](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/tree/main/code). Then, these predicted results will be integrated with the WACC (weighted average cost of capital) forecast results in Calcaterra et al. (2024), which represent the economic conditions under different energy transition scenarios.

The main goal of this analysis is to explore the impact of fossil fuel price fluctuations on future WACC of energy transition projects. By comparing the predicted prices with the estimated WACC results, we can analyze the potential impact of fossil fuel price fluctuations on capital costs, which is a key factor in energy infrastructure investment decision-making. This analysis will provide important insights to help us understand how oil price fluctuations affect the formulation of future energy transition strategies and changes in the financing environment.

## Preprocessing and harmonization step
1. Price Prediction
This study collect price sourses from dataset of World Bank, getting the historical price data for [oil](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md),[coal](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md), and [natural gas](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md). And use it for [price prediction](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/tree/main/code).And get the predicted [oil](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md),[coal](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md),[natrual gas](https://raw.githubusercontent.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/refs/heads/main/data/natural_gas_price_predictions_with_confidence_intervals.csv) data from 2025 to 2100 with its 95% confidence interval.
2. Impact Evaluation

Then, this study combine the prediction reslt with Calcaterra et al. (2024)'s [WACC dataset](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md). Subsequently， after data processing, we get the  WACC values with its coresponding predicted fossil fuel data in [Europe](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md), [Chinas+ regions](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md), [Middel East](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md), and [all transition countries](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md).

3. Result
Finally, we get [result](https://github.com/GreenComp-ERC/Shilin_ImpactOfFossilFeulPrice/edit/main/data/README.md) which demosntrates the imapct of fossil fuel price on WACC of energy transition projects in specificaal regions.
