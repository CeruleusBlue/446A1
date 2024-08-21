#Report Draft

## Problem Analysis

The NewChic dataset includes product data from a retail website primarily dealing with Fashion and Lifestyle product but also contains brand new merchandise as well. The retailer as a stakeholder will be interested in the popularity of the products among the customers. From the perspective of analysts working for the stakeholder, our problem should be to observer and record any relationships between the product features and determine a metric for the products with the best 'performance' in each category and comparing the 'performance' of categories with each other.



###Definition of Top 10 metric


The column 'likes_count' is an effective metric for determining 'performance'. The top 10 metric for this dataset will involve the popularity of the products among customers. The feature 'like_count' can considered to be directly affect to the sales of the product as customers will usually like a product if they purchase it or wish to purchase it.
From a preliminary analysis of the dataset, we can infer the following:
- 'discount' has a slightly negative relationship with 'likes_count'.
- 'raw_price' has an ambiguous relationship with 'likes_count'.
- 'current_price' is derived from the two other features, 'raw_price' and 'discount' and has an ambiguous relationship with 'likes_count'.
\begin{equation}
  current\_price = raw\_price * (1 - \frac{discount}{100})
\end{equation}

###Definition of Best Category

The 'best' category of products can be derived from the Top 10 metrics. However, the top 10 metric, i.e., the 'likes_count' alone may not yield the most accurate comparisons. To optimize the metric further we can include the 'raw_price' and 'discount'. <br>

\begin{equation}
  score_m = \frac{\sum_{i=1}^{n}{\frac{raw\_price_i*total\_likes_i}{discount_i}}}{n}
\end{equation}
where, <br>
&emsp;$n$: total products in $m$ <br>
&emsp;$m$: category

        



