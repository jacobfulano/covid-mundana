---
layout: post
title:  "Plotting a COVID19 Dataset in Python"
author: jacob
categories: [ tutorial ]
image: assets/images/python.jpg
tags: [featured]
---
There are many open-source datasets for covid-19 data; some are more curated than others.


## How to access the datasets

We can download the csv file of cumulative cases, as curated by the Center for Systems Science and Engineering (JHU CCSE) at Johns Hopkins (JHU):
[https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases](https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases)

The data has been collected since January 22 2020. On their website, they state that the data is curated from various sources including the World Health Organization (WHO), DXY.cn. Pneumonia. 2020, BNO News, National Health Commission of the People’s Republic of China (NHC), China CDC (CCDC), and others.

## How to plot the data using python

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

We can then read the `csv` file into a `pandas` dataframe and sort by country:
```python
df = pd.read_csv('time_series_covid19_confirmed_global.csv')
df_italy = df[df['Country/Region'] == 'Italy']
```

We can see what's in the dataframe:
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
![Italy Plot](assets/images/italy_example.jpg "Italy")
