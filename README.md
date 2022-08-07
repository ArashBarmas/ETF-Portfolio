# ETF-Portfolio
Constructing Smart Beta/EFT Portfolio Project


<img src="https://user-images.githubusercontent.com/41276263/183271149-4031ef8d-b874-460f-9019-0f003cf808a2.jpeg" width="1000" height="300">

In this project, I constructed two ETF portfolios using data of 100 large volume stocks from 2013 till 2018.

### Index 1: 

based on dollar volume. (multiplying close price of a stock to its volume and normalizing cross sectionally).

### ETF 1: 

based on cumulative dividend. (cumulative sum of total dividend paid by a stock with cross sectional normalization).

<img src="https://user-images.githubusercontent.com/41276263/183270948-134301de-bec7-4f73-8a95-a4c6038b027e.jpg" width="1000" height="400">



### Index 2: 

The benchmark used for the second ETF is market cap index. 

### ETF 2: 

the weights are optimized based on the following formula. The portfolio is constructed in-sample with no rebalancing. 



$Minimize \left [\sigma^2_p + \lambda\sqrt{\sum{1}^{m}(weight_i-indexWeight_i)^2} \right]$ for fully invested and long-only portfolio


<img src="https://user-images.githubusercontent.com/41276263/183271018-c835ce84-77e3-4aca-839c-e9e6bc85bbdf.jpg" width="1000" height="400">



### Turnover

I rebalanced the portfolio every year(252 trading days), the annualized turnover was 0.32914.


AnnualizedTurnover = $\frac{SumTotalTurnover}{NumberOfRebalanceEvents} * NumberofRebalanceEventsPerYear $

SumTotalTurnover = $\sum_{t,n}{\left | x_{t,n} - x_{t+1,n} \right |} $ Where $ x_{t,n} $ are the weights at time $ t $ for equity $ n $.

 SumTotalTurnover is just a different way of writing  $\sum \left | x_{t_1,n} - x_{t_2,n} \right |$


