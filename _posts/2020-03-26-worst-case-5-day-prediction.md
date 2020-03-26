---
layout: post
title:  "Update 3.26 // US Surpasses China + Worst Case 5-day Prediction"
categories: [ Analysis ]
image: assets/images/US.jpg
tags: [featured]
---


As of 6:00 pm, Thursday March 26, the United States has more confirmed coronavirus cases than China.[^fn1]

The US has more than 83,000 confirmed cases - and this is with woefully inadequate testing.

We can predict the worst case scenario for the rest of the month of March by fitting the JHU data with an exponential function. The worst case scenario is shown below:

![US]({{ site.baseurl }}/assets/plots/us-3-26/2020-03-26-1903-US.png "US")

#### The numbers do not paint a pretty picture.

| Date: | Predicted Total Cases |
| ---- | ---------------- |
| 3-25: | 68,764 (data) |
| 3-26: | 89,473 |
| 3-27: | 116,420 |
| 3-28: | 151,482 |
| 3-29: | 197,103 |
| 3-30: | 256,464 |
| 3-31: | 333,703 |

Note that the last data point is from yesterday, March 25, with 68,764 cases. It predicts that by the evening of March 26 (today), there will be 89,000+ cases.

Comparing this to Italy, France, Spain, and Germany, we see that the US has a much larger rate of exponential growth, with `b=0.263`

![US]({{ site.baseurl }}/assets/plots/us-3-26/2020-03-26-1859-5countries.png "US")

Let's hope that this trend slows down...tomorrow.


[^fn1]: [NYT, accessed 7:15 pm, March 26](https://www.nytimes.com/2020/03/26/world/coronavirus-news.html?)
