# Temperature Trends for Proposed Oahu Surf Shop

## Project Overview
The purpose of this project is to analyze the temperature trends in Oahu, Hawaii for a hypothetical client seeking to open a surf shop. Specifically, the temperature trends during the months of June and December are analyzed so that the client can make a more informed decision.

## Resources and Software

- Starting File: [hawaii.sqlite](https://github.com/eric-blankinshp/Surfs-Up-/blob/main/hawaii.sqlite)
- Python 3.7.10
- psycopg2-binary 2.8.6
- SQLAlchemy 1.4.1

## Results

- The average temperature in Oahu during December is only 3.9°F cooler than June.
- The lowest temperature in December is 8°F colder than the lowest temperature in June.
- There are 10.7% less data points in December than June.

Below is a statistical summary for the month of June:  
![june_temp](https://github.com/eric-blankinshp/Surfs-Up-/blob/main/Resources/june_temp.png)

Below is a statistical summary for the month of December:  
![december_temp](https://github.com/eric-blankinshp/Surfs-Up-/blob/main/Resources/december_temp.png)

## Summary

Based on the results above, it can be expected that a surf shop in Oahu will have less customers in December than in June due to the slight decrease in average daily temperature.

It is important to have the most relevant results when conducting analysis on a potential business venture. For this reason, I would perform two additional queries on June and December to obatin more weather data about precipitation during those months.

The query below will find precipitation scores in June:
```python
session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 6).all()
```
If you would like to view the output of June precipitation statistics, please [click here](https://github.com/eric-blankinshp/Surfs Up-/blob/main/Resources/june_prec.png.) 


The query below will find precipitation scores in December:
```python
session.query(Measurement.date, Measurement.prcp).filter(extract('month', Measurement.date) == 12).all()
```
If you would like to view the output of December precipitation statistics, please [click here](https://github.com/eric-blankinshp/Surfs-Up-/blob/main/Resources/december_prec.png).

