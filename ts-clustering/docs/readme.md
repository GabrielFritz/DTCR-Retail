# Time series clusterization for customer segmentation: A retail application 

## Problem description

One of the most important steps for a business to achieve and mantain success is to perform
high-quality market research. If you don't understand the various aspects that affect your
business, you can't make the right decisions, and if you can't make the right decisions,
your company's success would be attained to luck. Best of it to you.

There are many analysis you need to perform to understand exactly where your business stands
in the market: Is your target customer well discovered and accessible? Are your products
necessary? Are your products good, so the customer is compeled to buy it? How's the competition
going? [1]

From the former paragraph, you might notice that most of the market analysis revolves around
customer research, and this is expected: In order to sell something to someone, you must understand
who "someone" actually is and more: You must understand the differences between your customers' necessities.
This is where customer segmentation plays a role.

There are many ways to segment customers: The RFM clustering segments the clients based on their recency,
frequency and monetary value, all this values are summaries of the customer's consumption time series [2]. Other
way to segment them is to predict, for each customer, their churn probability and clustering based on this value [2].
Demographic segmentation segments clients based on demographics such as age, location, marital status, race,
income, education, and more [3].

One problem wih all this approaches is that they fail to leverage the time series data available. In RFM clustering,
the time series data is summarized in three quantities before clustering, in churn segmentation, you must, first,
generate a probability before segmenting. In Demographic segmentation, the time series data don't even play a role.
This problem repeats in most approaches for customer segmentation, which leads to lack of fine-grained understanding
about customer consumption behavior.

In this proposal, I present a possible way to leverage from time series data for customer segmentation.
By combining the DTCR [4] approach, which is SOTA for time-series clustering, and USSL [5] approach, less efficient
but with interesting sub products (i.e. _shapelets_), I believe it is possible to use better use of customer
consumption time series data.

## Challenges

The main challenges is to implement both algorithms from scratch and, at the same time, find ways to
combine them into one architecture. After that, it is necessary to find ways to gain insights from the results:
Discovering the clusters is just one part of the problem, understanding the clusters is the other.

### Datasets

In the first moment, I will be using the research benchmark proposed by [5], in order to compare results
with the papers. After that, I will use the market basket analysis Instacart Kaggle competition [6] as an application for retail.

## Evaluation

To evaluate my architecture approach, I will use the benchmark datasets proposed in previous research [5], by calculating
the metrics Rand Index (RI) and Normalized Mutual Information (NMI). To evaluate the retail application, I will perform
multiple segmentation techiniques on my data and compare with the proposed approach.


## References

[1] MIT course: 15.390 New Enterprises Notes from 7th lecture, https://ocw.mit.edu/courses/sloan-school-of-management/15-390-new-enterprises-spring-2013/lecture-notes/MIT15_390S13_lec07.pdf
[2] https://towardsdatascience.com/data-driven-growth-with-python-part-2-customer-segmentation-5c019d150444
[3] https://marketing.toolbox.com/blogs/reubenyonatan/comparing-the-4-types-of-customer-segmentation-approaches-122418
[4] http://papers.nips.cc/paper/8634-learning-representations-for-time-series-clustering.pdf
[5] https://ieeexplore.ieee.org/document/8386690
[6] https://www.kaggle.com/psparks/instacart-market-basket-analysis
