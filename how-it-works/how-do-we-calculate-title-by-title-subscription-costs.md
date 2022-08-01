---
description: >-
  Learn where Unsub gets its journal price data, and how that data is used to
  forecast your future costs of subscription
---

# How do we calculate title-by-title subscription costs?

A key data source for Unsub is the title-by-title price for each journal--the actual real-world cost you'll pay, should you choose to subscribe to that journal individually outside any Big Deal.

For any given journal, there are three possible **price sources** for the title-by-title price. There are also two **price modifiers** Unsub uses to fine-tune the forecast. Putting all that together lets us predict the annual price you'll pay over the next five years, _if_ you to subscribe to a given journal.

### Price sources: <a href="#price-sources" id="price-sources"></a>

**1. Public list price:** this is the title-by-title subscription price from the publisher's website. This is the default source of price information. Here are some examples of public pricelists that we use:

* [Elsevier](https://www.elsevier.com/books-and-journals/journal-pricing/print-price-list) (2021)
* [Wiley](https://onlinelibrary.wiley.com/library-info/products/price-lists) (Academic, Medium FTE Tier, Online only prices, 2021)
* [Springer Nature](https://www.springernature.com/gp/librarians/licensing/journals-price-list) (online only plus Carriage Charges, 2021)
* [SAGE](https://us.sagepub.com/en-us/nam/institutional-subscriptions-to-individual-journal-titles) (Electronic+Backfile Lease, 2021)
* [Taylor & Francis](https://taylorandfrancis.com/journals/price-lists/) (FTE 40000 - 49999, 2021)

**2. Custom uploaded price:** you can [upload a simple spreadsheet with custom prices for each journal](../how-to-guides/upload-title-prices.md). Any custom prices you upload will override the default list prices. This is also how to provide prices for journals without a default price.

**3. No price:** If we couldn't find a public list price for a journal, and you haven't uploaded a custom price for it, then the price is unknown. In that case, this journal will be _omitted from forecasting,_ because we don't know how they will affect the financial side of the model. Your scenario will show a warning.

### Price modifiers: <a href="#price-modifiers" id="price-modifiers"></a>

Once you've got prices, there are also two ways those prices can be modified.

**1. Title-by-title subscription cost growth**: Unsub is designed to _forecast_ your costs and fulfillment, not just report them. To do that, we need to be able to take into account changes in subscription pricing over time. That's what this parameter does: it simply describes the percentage price increase expected every year. The default, based on industry averages, is 8%, but you can change this in your scenario's menu, under "Parameters ➞ Costs ➞ Title-by-title subscription cost growth."

**2. Title-by-title content fee:** There's also a second parameter that modifies journals subscription prices, and that's the "Title-by-title content fee." This is an extra (read: hidden) fee that publishers often charge on top of their quoted subscription costs, and so it's important to account for in order to get an accurate cost estimate. By default this is set to 5.7% (a recently-reported fee for Elsevier) but again, you can edit this in the scenario's menu, under "Parameters ➞ Costs ➞ Title-by-title 'content fee.'"

### Putting it all together <a href="#putting-it-all-together" id="putting-it-all-together"></a>

Let's look at an example of how this all fits together; we'll call it _Journal X_. First, we'll find the current price of a title-by-title subscription by looking it up in our price table. Let's say you've uploaded your own price of $1000, overriding the default publisher list price.

For year one of the five-year forecast, we'd predict you'll pay $1000 plus the 5.7% "content fee" of $57, for a total of $1,057.

For year two, we also add in the 8% increase in subscription cost, giving us $1,080 for the subscription. Adding in the content fee ($61.56 now), we estimate a total of $1,141.56.

For years three, four, and five, we do the same. Finally, we average all five years together to get the estimated average annual cost of title-by-title subscription.
