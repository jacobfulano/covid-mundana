---
layout: post
title:  "Open Source COVID-19 Datasets"
author: jacob
categories: [ resources ]
image: assets/images/covid_rect.jpg
tags: [sticky]
---
There are many open-source datasets for COVID-19 data; some are more curated than others. Here is a running list:

### Novel Coronavirus (COVID-19) Cases Data

The [Novel Coronavirus (COVID-19) Cases Data](https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases) is curated by the [Center for Systems Science and Engineering (CCSE)](https://systems.jhu.edu) at Johns Hopkins University (JHU) hosts multiple `csv` files of **cumulative confirmed cases** and **confirmed deaths**. The data is collected from various sources including the World Health Organization (WHO), China CDC (CCDC), and the [United States Center for Disease Control and Prevention (CDC)](https://www.cdc.gov/coronavirus/2019-ncov/cases-updates/cases-in-us.html). This project is led by Professor Lauren Gardner in collaboration with others.

* The New York Times uses this data for its [Daily Tracker](https://www.nytimes.com/interactive/2020/03/21/upshot/coronavirus-deaths-by-country.html?action=click&module=Top%20Stories&pgtype=Homepage) of Coronavirus Deaths by U.S. State and Country:

### The COVID Tracking Project

[The Covid Tracking Project](https://covidtracking.com/) focuses on coronavirus **testing data** in the US.

![The COVID Tracking Project]({{ site.baseurl }}/assets/images/covid-tracking-project.png "The COVID Tracking Project")

This includes **positive and negative results**, **pending tests**, and **total people tested** for each state. This is particularly important, since the CDC is currently not publishing complete testing data.[^fn1] This was created in part by Robinson Meyer and Alexis Madrigal, reporters at _The Atlantic_, and is currently maintained by a group of reporters and data scientists. The data is curated by hand and double checked manually. As they state on their website:

> All our information comes from state/district/territory public health authorities—or, occasionally, from trusted news reporting, official press conferences, or (very occasionally) tweets or Facebook updates from state public health authorities or governors.

* This data can be explored easily on [_The Atlantic_ tracker](https://www.theatlantic.com/health/archive/2020/03/how-many-people-tested-sick-coronavirus-covid-each-state-america/608413/)

### COVID-19 Open Research Dataset (CORD-19)

![kaggle]({{ site.baseurl }}/assets/images/kaggle.png "kaggle")

The [COVID-19 Open Research Dataset (CORD-19)](https://pages.semanticscholar.org/coronavirus-research) is a free resource of 44,000+ research articles about COVID-19 and the coronavirus "family" of viruses. It is a dataset curated for data mining and natural language processing (NLP). It is updated weekly.

This dataset is also part of a [Kaggle competition](https://www.kaggle.com/allen-institute-for-ai/CORD-19-research-challenge) hosted by the [Allen Institute for AI (AI2)](https://duckduckgo.com/?q=Allen+Institute+For+AI&t=osx)

### Government Websites

![cdc]({{ site.baseurl }}/assets/images/cdc.png "cdc")

* [The United States Center for Disease Control and Prevention](https://www.cdc.gov/coronavirus/2019-ncov/cases-updates/cases-in-us.html) maintains data on cases in the US in the form of a web report updated regularly at noon Mondays through Fridays.

* NY State has a [county by county breakdown of positive cases](https://coronavirus.health.ny.gov/county-county-breakdown-positive-cases), which seems to be updated hourly. However, this data is not in `csv` format

* World Health Organization (WHO)

[^fn1]: https://covidtracking.com
