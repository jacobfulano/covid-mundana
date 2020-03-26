---
layout: post
title:  "I Know an Exponential When I See One"
author: jacob
categories: [ Analysis ]
image: assets/images/exp.jpg
tags: [featured]
---

It is easy to see that coronavirus has exponential spread.

I first began worrying about the spread of COVID-19 in the US after playing around with some open source confirmed cases data. At the time - March 8th (it seems so long ago!) - the US had just  over 600 confirmed cases _in the entire country_.

A quick glance at the early data from South Korea, Italy, and Iran seemed to indicate that they all had similar initial spread, with an exponential growth rate between 0.22 and 0.29. I made the simplifying assumption that the early rate of spread in the United States would be similar.

I averaged the exponential growth for South Korea, Italy, and Iran, and then fit this to the measly US data. This predicted that by March 18th, there would be more than 7,500 confirmed cases in the US.

This is the plot I generated:
![exponential]({{ site.baseurl }}/assets/plots/exponential.png "exponential")

At the time - again, March 8th - I was incredulous that I would see the numbers rise from ~600 to 7,500 in the span of a week and a half. I sent the plot around to a few friends and family members, and we winced and grimaced at this worst case scenario. But we somehow convinced ourselves that things would be different in the US.

Tragically, by March 18th Italy was above 30,000 cases and the US was squarely above 7,500 cases.

When asked about the sad state of affairs the other day, my advisor sighed with resignation

> I know an exponential when I see one
