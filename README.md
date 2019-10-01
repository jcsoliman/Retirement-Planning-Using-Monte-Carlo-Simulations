# Financial Report
In this report, we analyzed the personal finance data pulled from Plaid and historical security prices from IEX. With the data, we ran some analyses to link banking and investment accounts. In particular, this report aims to determine whether a portfolio could yield the income requirement of a customer. 

## Income Data
Looking at the income data, we find that the client has the following:

| Prev year's gross income | Current monthly income | Projected yearly income |
| :---: | :---: | :---: |
| 7,285 | 500 | 6,085 |

## Budget Analysis

We also looked at spending in the past 90 days and found:

| Spending Category | Amount |
| :---: | :---: |
| Food and Drink | 3,317.19 |
| Payment | 6,310.50 |
| Recreation | 235.50 |
| Shops | 1,500.00 |
| Transfer | 20,537.34 |
| Travel | 35.19 |

![Spending_Pie_Chart](spending_last_90_days.png)

In this period, he spent 10,645.24 each month.

![Spending_Bar_Chart](spending_by_month.png)


## Retirement Planning

Using a portfolio consisting of stocks and bonds, we built a retirement plan simulating historical data to project returns over time.

### Methodology
In running the simulation, we performed the following steps:
1. Take the historical closing prices of SPDR S&P 500 ETF (SPY) and iShares Core U.S. Aggregate Bond ETF (AGG) from the previous year.
2. Calculate average daily returns and volatility using standard deviation.
3. Assuming normal probability distribuition and taking into consideration average daily return and volatility, project portfolio cumulative returns from the last closing price and run 500 simulations over the 30 years (252 * 30 trading days), with portfolio weightage of 60% stocks ans 40% bonds.
4. Analyze results of simulations.

### Analysis
![500Sims](monte_carlo_simulation_30_years.png)

On the very last day, we find that the ending cumulative return is in the range of 0.5175- 15.9342.

Narrowing it to a 90% confidence interval, the portfolio could yield 1.2713 to 8.1076.

![90CI](90_percent_conf_interval.png)

Calculating the return at 10th, 50th, and 90th percentiles and an initial investment of $50,000, we get:

| Percentile | Ending Cumulative Return | $ Portfolio Return |
| :---: | :---: | :---: |
| 10th | 1.6936 | 84,679.87
| 50th | 3.2378 | 161,888.23
| 90th | 6.4913 | 324,562.81

Charting these percentile portfolio cumulative returns over the life of the investment, we get:

![Overtime](optional_challenge.png)

Now assuming a 4% withdrawal rate at retirement, we find that the 10th percentile retirement income of 3,387.19 is less than the projected income of 6,085.00, suggesting not enough confidence to determine whether the portfolio return could meet the annual income requirement.

If however, we increased the initial investmemt by 50%, we get find that the portfolio yields a 10th percentile retirement income of 7,621.19, greater than the projected income of 6,085. Given that 90% of expected returns will yield greater results, we can take comfort on the higher probability that the portfolio could meet the annual income requirement.

### Changing The Variables

Retiring earlier than 30 years could mean a shortened period for the portfolio to grow. Could tweaking the other variables to allow for a retirement in 5 years result in viable yields?

#### Higher risk

Increasing the stock to bond ratio to sa 70:30, we find:

Increasing further to 80:20, we get:



#### Higher initial investment

Investing more by 50%, we get:

Investing more by 75%, we get:


