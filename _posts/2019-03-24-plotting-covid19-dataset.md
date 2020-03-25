---
layout: post
title:  "Plotting COVID-19 Data in Python"
author: jacob
categories: [ tutorial ]
image: assets/images/python2.jpg
tags: [featured]
---
This introductory tutorial explains how to extract and plot the COVID-19 confirmed cases data from a curated dataset.

## How to access the data

We can download a straightforward dataset constructed by the Center for Systems Science and Engineering (CCSE) at Johns Hopkins (JHU): [https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases](https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases)

The data has been collected since January 22, 2020, and is organized into two `csv` files. These files are updated twice daily:
* `time_series_covid19_confirmed_global.csv`
* `time_series_covid19_deaths_global.csv`

We will be using the first file to look at cumulative cases, which can be downloaded [here](https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases).

## How to plot the data

We will use the `numpy`, `pandas` and `matplotlib` libraries in python.

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

We can then read the `csv` file into a `pandas` dataframe and sort by country (e.g. Italy):
```python
df = pd.read_csv('time_series_covid19_confirmed_global.csv')
df_italy = df[df['Country/Region'] == 'Italy']
```

We can see what's in the dataframe using `.head()`:
```python
df_italy.head()
```

In order to simplify the dataframe, we can set the index to 'Country/Region' and drop the unnecessary columns:

```python
df_italy = df_italy.set_index('Country/Region', drop = True) # set pandas dataframe index to country
df_italy = df_italy.drop(columns=['Lat','Long','Province/State'])

data_italy = df_italy.loc['Italy','2/20/20':'3/23/20']
```

Finally, we can plot the data and label the axes using `matplotlib`
```python
plt.plot(data_italy.index,data_italy.values,'.-')
plt.xticks(rotation=90) # rotate the xticks
plt.xlabel('calendar date')
plt.ylabel('cumulative cases')
plt.title('Italy Cumulative Cases')
plt.tight_layout()
```
![Italy Plot]({{ site.baseurl }}/assets/plots/italy_example.jpg "Italy")

We can do the same thing for the US:

```python
df_us = df[df['Country/Region'] == 'US']
df_us = df_us.set_index('Country/Region', drop = True) # set pandas dataframe index to country
df_us = df_us.drop(columns=['Lat','Long','Province/State'])

data_us = df_us.loc['US','2/28/20':'3/23/20']
```

![US Plot]({{ site.baseurl }}/assets/plots/us_example1.jpg "US")

Plotting these together is quite alarming:

```python
plt.plot(data_italy.index,data_italy.values,'.-',label='Italy')
plt.plot(data_us.index,data_us.values,'.-',label='US')
plt.xticks(rotation=90) # rotate the xticks
plt.xlabel('calendar date')
plt.ylabel('cumulative cases')
plt.title('Italy and US Cumulative Cases')
plt.legend()
plt.tight_layout()
```

![Italy + US Plot]({{ site.baseurl }}/assets/plots/italy+us_example.jpg "Italy and US")

It is clear from these plots that both countries have experienced an astronomical increase in confirmed cases between the end of February and mid-March. Both plots also seem to have "bumps" or "elbows." In the US, this appears after March 18, and is mostly likely due to a sharp increase in testing as reported by CBS on March 19:

> Officials expect the number of confirmed coronavirus cases to surge in the next few days as labs rush to process a massive backlog of tests that number in the tens of thousands. ([Confirmed coronavirus cases will jump as testing ramps up](https://www.cbsnews.com/news/coronavirus-confirmed-cases-rise-tests/))
