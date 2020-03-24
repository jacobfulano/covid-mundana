---
layout: post
title:  "Plotting a Covid-19 Dataset"
author: Jacob
categories: [ tutorial ]
image: assets/images/17.jpg
tags: [featured]
---
There are many open-source datasets for covid-19 data; some are more curated than others.


## How to access the datasets

We can download the csv file of cumulative cases, as curated by this group at Johns Hopkins (JHU):
[https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases](https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases)

## How to plot the data using matplotlib

```python
import numpy as np
import pandas as pd
```

We can then read the csv file into a dataframe and sort by country:
```python
df = pd.read_csv('time_series_2019-ncov-Confirmed-2020-3-18.csv')
df_italy = df[df['Country/Region'] == 'Italy']
```

In order to clean
```python
df_italy = df_italy.set_index('Country/Region', drop = True) # set pandas dataframe index to country
df_italy = df_italy.drop(columns=['Lat','Long'])

data_italy = df_italy.loc['Italy','2/2/20':'3/17/20']
```
