# ExploraBI: Marketing Analytics & Measurement

Notebooks on the questions marketing measurement starts with: **what drives sales, and how much did each channel really contribute?**

## Notebooks

| Notebook | What it covers |
|---|---|
| [MMM_Parameter_Recovery.ipynb](Marketing%20Analytics/MMM_Parameter_Recovery.ipynb) | **Bayesian marketing mix model, tested against a known truth.** Simulates 3 years of weekly sales with known adstock and saturation for two channels, fits a PyMC-Marketing MMM, checks convergence (R-hat, ESS, divergences), then compares recovered parameters, contributions and ROAS to the truth. |
| [Sales_Trend_and_Seasonality.ipynb](Marketing%20Analytics/Sales_Trend_and_Seasonality.ipynb) | Baseline first: Prophet forecasting with cross-validation, STL decomposition and STL + ARIMA forecasting on Walmart weekly sales. |

## Headline result from the MMM notebook

| Channel | True ROAS | Estimated ROAS | 94% HDI |
|---|---|---|---|
| TV (flighted) | 1.36 | 1.34 | 1.25 – 1.44 |
| Paid Social (always on) | 3.11 | 3.45 | 1.86 – 5.27 |

All four true adstock and saturation parameters fall inside their 94% posterior intervals (0 divergences, R-hat 1.00).
The contrast between the channels is the real lesson: TV's on/off flighting gives the model sharp variation to learn from, while always-on Social leaves a much wider interval. **Spend patterns decide what an MMM can learn**, which is the case for varying spend deliberately or calibrating with incrementality tests.

## Run it

```bash
pip install -r requirements.txt
jupyter lab
```

## Data

- `Marketing Analytics/data/Walmart_Sales.csv`: weekly store sales with holiday, temperature, fuel price, CPI and unemployment
- `Marketing Analytics/data/Horlicks Data.csv`: weekly GMV and media spend by channel
- The MMM notebook generates its own data, so its results are fully reproducible from the seed

## Further reading

Key papers behind these methods are listed in [READING.md](Marketing%20Analytics/READING.md).
