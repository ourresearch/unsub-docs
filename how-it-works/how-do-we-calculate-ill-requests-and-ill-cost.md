---
description: >-
  Learn how Unsub predicts your library's post-cancellation Interlibrary Loan
  activity and costs
---

# How do we calculate ILL requests and ILL cost?

Interlibrary Loan (ILL) is a key consideration in forecasting the effects of cancellation on fulfillment and cost. So naturally it's also an important part of Unsub's five-year forecasting approach, and is prominently displayed on your Scenario Overview page. To understand how we handle ILL, let's look at two parts of the equation: the expected number of **ILL requests** and the expected **ILL cost**.

## Forecasting ILL requests <a href="#forecasting-ill-requests" id="forecasting-ill-requests"></a>

We'll start by looking at how we forecast ILL requests for a single journal--let's call it _Journal X_. The approach has a few steps:

1. We start with the number of views _Journal X_ received last year, using data from [your uploaded COUNTER report](../how-to-guides/upload-counter-usage-data.md).
2. We predict the usage of _Journal X_ on your campus for each of the next five years. To do this we use an algorithm to forecast the growing (or shrinking) of interest in this journal, based on recent publication and readership trends.
3. For each of the next five years, we now generate a breakdown of how much of _Journal X's_ viewership can be fulfilled instantly, via your PTA (Post-Termination Access) rights and via open access. Whatever's left over after that is a turnaway (unless of course you have chosen to subscribe title-by-title to _Journal X_).
4. We _could_ naively assume that every turnaway creates an ILL request. But we know that readers often procure paywalled articles by other means, or simply find replacements. In fact, [the literature suggests](https://arxiv.org/abs/2009.04287) that (conservatively) around 5% of turnaways generate ILL requests. This 5% figure is your ILL Request Rate. So, to determine your ILL usage, Unsub simply your turnaways times your ILL Request Rate; this estimates the number of ILL requests expected for _Journal X_ each year. Be default, the ILL Request Rate is 5%; you can change this figure in the scenario menu under "Parameters ➞ ILL ➞ ILL Request Rate"

That's it! Using these steps for _Journal X_ we can predict the number of ILL request in each of the next five years. By giving all of the journals in your scenario this same treatment, we can estimate ILL requests across the whole package. Generally we'll display the results as a five-year average (rather than year-by-year) in order to simplify the report.

## Forecasting ILL cost <a href="#forecasting-ill-cost" id="forecasting-ill-cost"></a>

It's pretty easy to estimate the cost of ILL, once we have the number of ILL requests. We just need an estimate of the cost per request, and use that as a multiplier. Of course, this estimate needs to be the _overall_ cost per request, averaging in both variable costs (eg. transaction fees) and continuing fixed costs like staff salaries.

Helpfully, there is a large body of literature estimating the the overall cost-per-request of ILL, [which is summarized here](https://arxiv.org/abs/2009.04281). From that, we find that $17 per request is the most-cited figure, and so that's the value Unsub uses by default. Of course, if you know your own library's cost per request is different from this, you can change that $17 figure via the scenario menu ("Parameters ➞ ILL ➞ ILL transaction cost.")

Now that we have an average cost per ILL request, we just multiply that number by the number ILL requests forecasted for each of the next five years; that gives us forecasted ILL costs for each of the next five years. Again, we'll generally report the _average_ annual cost over the next five years for simplicity's sake.
