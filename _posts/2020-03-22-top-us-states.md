---
layout: post
title:  "Update 3.22 // Predictions for New Jersey, Washington, California and New York"
categories: [ Analysis ]
image: assets/images/US.jpg
tags: [featured]
---

The spread of COVID19 is increasing rapidly across all 50 states. As of March 22nd, the states with the most confirmed cases are New Jersey, Washington, California, and New York.

The following data is through March 22, 2020, and downloaded from the [Novel Coronavirus (COVID-19) Cases Data](https://data.humdata.org/dataset/novel-coronavirus-2019-ncov-cases).

We can see the cumulative confirmed cases for these four states here:

![4 states]({{ site.baseurl }}/assets/plots/us-3-22/2020-03-25-0156-4statesv1.png "4 states")

Below is the same data but plotted with a different y-axis. New York tragically has many more cases than any other state, and is the center of the epidemic in this country.

![4 states]({{ site.baseurl }}/assets/plots/us-3-22/2020-03-25-0156-4statesv2.png "4 states")

## Predictions

We can make simple predictions for future cases by fitting exponential curves to the data. While this is likely inaccurate, it can give a rough estimate of the spread of coronavirus in each state.

#### New Jersey

The prediction is that New Jersey will have close to 15,000 cases by the end of March 27th.

![New Jersey]({{ site.baseurl }}/assets/plots/us-3-22/2020-03-25-0204-New Jersey.png "New Jersey")

#### Washington
This simple exponential fit predicts that Washington state will have more than 4,000 cases by March 27th.
![Washington]({{ site.baseurl }}/assets/plots/us-3-22/2020-03-25-0204-Washington.png "Washington")

#### California
This simple exponential fit predicts that California will have more than 4,000 cases by March 27th as well.
![California]({{ site.baseurl }}/assets/plots/us-3-22/2020-03-25-0204-California.png "California")

#### New York

I hope that this prediction is a gross overestimate. Fitting an exponential to the data for New York predicts that there will be more than 100,000 cases by the end of March 27th.

![New York]({{ site.baseurl }}/assets/plots/us-3-22/2020-03-25-0204-New York.png "New York")
