# Forecasting Net Profit

## Analysis of Hourly Google Search Traffic Patterns

### Objective
The objective of this phase is to discern noteworthy trends in Mercado Libre's hourly Google search traffic and establish correlations with key corporate financial events.

### Procedure
1. Ingest the search data into a DataFrame and filter it to encompass only the month of May 2020.
2. Utilize hvPlot to visually represent the outcomes and identify any anomalous patterns.
3. Compute the aggregate search traffic for May 2020, contrasting it with the monthly median. Evaluate whether there was an upswing in traffic during the release of quarterly financial results.

### Findings
__The Google search trend exhibited an 8.55% increase coinciding with Mercadolab's financial results release.__

## Analysis of Seasonality in Search Traffic Data

### Objective
This phase involves scrutinizing the search traffic data for discernible seasonal patterns related to the company, with a focus on hourly data.

### Procedure
1. Aggregate the hourly search data to plot the average traffic by the day of the week.
2. Visualize the traffic using hvPlot as a heatmap, referencing the hour and day of the week.
3. Group the data by the week of the year and observe if search traffic experiences an uptick during the winter holiday period.

### Findings

* __Search traffic peaks during midnight hours, particularly on weekdays.__
* __Contrarily, search traffic tends to decrease during the winter holiday period.__

## Correlation Between Search Traffic and Stock Price Patterns

### Objective
Investigate the relationship between Google search data and the stock price patterns of the company.

### Procedure
1. Ingest and plot the stock price data, concatenate it with the search data.
2. Filter the data to the first half of 2020 and visualize the time series. Assess whether both datasets indicate a common trend.
3. Introduce lagged search trends and additional columns for stock volatility and hourly stock return.
4. Examine the time series correlation to identify relationships.

### Findings

* __Search trends did not exhibit comparable or significant changes in the first half of 2020, while the stock closing price consistently increased, indicating a growth in customer numbers and revenue.__
* __Volatility spiked during the first half of 2020, a common characteristic in global stock returns where high volatility days tend to be followed by more high volatility days.__

## Development of a Time Series Model using Prophet

### Objective
Construct a time series model to analyze and forecast patterns in hourly search data.

### Procedure
1. Configure the Google search data for a Prophet forecasting model.
2. Estimate the model and visualize the forecast.
3. Analyze individual time series components to address specific inquiries regarding popularity and search traffic.

### Findings

* __The forecast model indicates a downward trend in the search trend for Mercado in the near term.__
* __The midnight hours, specifically 12 am, exhibit the highest popularity in the trends.__
* __Tuesdays attract the most traffic.__
* __October indicates the lowest point of search traffic in the calendar year.__

## Revenue Forecasting using Time Series Models

### Objective
Generate a forecast for total sales in the next quarter using historical revenue figures.

### Procedure
1. Ingest daily historical sales figures and apply a Prophet model.
2. Interpret the model output to identify seasonal patterns in company revenue.
3. Generate a sales forecast for the finance group, encompassing best- and worst-case scenarios.

### Findings

* __Wednesdays boast the highest revenue.__

---

We can confidently predict the total sales for the next quarter with 95% certainty as follows:

* ___Best case: $1.051 billion___
* ___Worst case: $888.23 million___
* ___Most likely: $969.63 million___
