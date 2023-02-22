# Leader-Follower Futures Analysis

A trading company wants to investigate possible relationship between three different futures. They assume this relationship could take form of a leader-follower relation, i.e. movement of one futures defines trajectory of another with a time lag.

## Problem

We need to determine which futures is the leader and which is the follower, and establish its properties, e.g. duration, strength, nature etc., if such a relationship exists at all.

## Data

Dataset represents closing prices of minute bars (candlesticks) for three continuous futures:

* E-Mini S&P 500 
* FTSE China A50 
* 10 Year Treasury Note 

Timespan: Jan 2020 - Dec 2021.

## Analysis

1. Take a pair of indices
2. Assume one index to be a leader and another a follower
3. Start shifting leading index "back in time" by 1 day, calculate correlation between indices
4. Iterate the previous step for 650 days
5. Find the highest correlations (positive, negative or both)
6. Plot shifted index linecharts for these highest correlations respective time lags to visually assess the results
7. Check for potentially overlooked correlations by plotting timelag vs correlation 
8. Repeat steps 1-7 for other index pairs

## Results

* S&P is a leader relative to 10Y with a negative relationship for 2-3 months lag and with a positive relationship for 1.5 years lag
* 10Y and FTSE seemingly do not have any lag relationship
* S&P and FTSE have an alternating leader-follower relationship: FTSE is a leader for S&P with a positive relationship for a 6 months (and less) lag, S&P is a leader for FTSE with a negative relationship for a 6-12 months lag and a positive relationship with a 1.5 years lag. 

To additionally verify these findings one would need an inquiry into theoretical economic relationships between these futures, i.e. whether they are substitutes or complementary goods, their price elasticities, etc. Potential COVID-19 pandemic effects could also influence the results. However, these issues require more data and theoretical understanding to be properly examined, which is outside the scope of this  analysis.

## Links
**Code:** <a href='https://github.com/AntonBizyaev/index_lag_analysis/blob/main/index_lag_analysis.ipynb'>jupyter notebook</a>  
**Data:** <a href='https://github.com/AntonBizyaev/index_lag_analysis/blob/main/data.zip'>zip</a>  

