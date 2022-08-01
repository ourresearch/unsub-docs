---
description: >-
  Learn the details behind all the variables Unsub uses to forecast your costs
  and fulfillment
---

# Data export

The data fields in the Download as Spreadsheet are described here:

### Metadata <a href="#metadata" id="metadata"></a>

**issn\_l\_prefixed**

The primary ISSN we use for this journal (see issn.org [Linking ISSNs](https://www.issn.org/understanding-the-issn/assignment-rules/the-issn-l-for-publications-on-multiple-media/)) prefixed with "issn:"

**issn\_l**

The primary ISSN we use for this journal (see issn.org [Linking ISSNs](https://www.issn.org/understanding-the-issn/assignment-rules/the-issn-l-for-publications-on-multiple-media/))

**title**

The title of this journal.

**issns**

A JSON array of ISSNs for this journal

**subject**

A single OpenAlex subject. The subject is selected by filtering to level zero OpenAlex subjects, then selecting those with the maximum score. If there's more than one subject we then select one subject alphabetically, starting from "A". You may also want to look at **subject\_top\_three** due to this alphabetical selection. See [OpenAlex docs](https://docs.openalex.org/about-the-data/venue#x\_concepts) for more information.

**subject\_top\_three**

The top three OpenAlex subjects. Selected using the top three level zero subjects based on their score for strength of association between the journal and the subject. See [OpenAlex docs](https://docs.openalex.org/about-the-data/venue#x\_concepts) for more information.

**subjects\_all**

All level zero OpenAlex subjects and their IDs in a JSON array. With the IDs one can look up more information on each subject by appending the ID to `https://openalex.org` (e.g., [https://openalex.org/C185592680](https://openalex.org/C185592680)). See [OpenAlex docs](https://docs.openalex.org/about-the-data/venue#x\_concepts) for more information.



{% hint style="info" %}
OpenAlex uses the term "concept" - which is equivalent to "subject" here
{% endhint %}

### Summary <a href="#summary" id="summary"></a>

**subscribed**

`True` if you currently have the journal modeled as "subscribed" in your scenario, `False` if the journal is currently "unsubscribed"

**is\_society\_journal**

`True` if the journal is a society journal; `False` if not.

**usage**

The projected Usage of the journal by your institution. Usage is a measure of the journal's value to your institution. It is calculated as:

`Usage of a journal =`

`Downloads from the journal`

`+ (Citations to the journal by your authors) * (citation weight)`

`+ (Authored papers in the journal) * (authorship weight)`

**cpu**

This is the Cost per Use (CPU) of the journal. We use a more advanced variant of CPU (internally we call this Net Per Paid Use, or NCPPU). This CPU calculation is the net cost (subscription minus ILL), divided by Paid Use (Usage that can't be met with free sources). This is our most important measure of journal value--it summarizes the real value you're getting for your subscription dollar. This article has more details: [How do we calculate cost-effectiveness (Cost Per Use, CPU)](https://intercom.help/get-unsub/en/articles/4061107-how-do-we-calculate-cost-effectiveness-cost-per-use-cpu)

**cpu\_rank**

The journal's rank according to CPU, relative to other journals in this dataset. The most cost-effective journal has a rank of 1.\


**cost**

The cost of this journal according to the Settings and Subscription status of the journals in this Scenario. It will be either Subscription Cost or ILL Cost (see next columns), depending on whether the journal is currently subscribed to or not in this scenario.

****

**instant\_usage\_percent**

The percent of Usage that is available instantly -- available as Open Access, PTA, or Subscription.

**free\_instant\_usage\_percent**

The percent of Usage that can be fulfilled via Open Access or PTA. This excludes usage met only by ILL or Subscription.

\


### Costs <a href="#costs" id="costs"></a>

**subscription\_cost**

The title-by-title subscription cost of this journal. It includes a 'content fee' based on your settings, and annual price increases over the next five years (the cost shown is the average cost over the next five years). This data is based on public price lists unless you've uploaded a custom price list (available in a purchased account). This article has more details: [How do we calculate title-by-title subscription costs?](../how-it-works/how-do-we-calculate-title-by-title-subscription-costs.md)

**ill\_cost**

The ILL subscription cost of this journal. It is based on the ILL transaction cost and your ILL Request Rate, both of which are adjustable parameters. This article has more details: [How do we calculate ILL requests and ILL cost?](../how-it-works/how-do-we-calculate-ill-requests-and-ill-cost.md)

**subscription\_minus\_ill\_cost**

The net cost of the subscription, which is the Subscription cost above minus the ILL cost (since almost all universities will offer a journal by ILL if they didn't subscribe). For some journals with very high Usage and low subscription prices this number is actually negative -- subscribing is \*cheaper\* than filling all the anticipated ILL requests.

### Fulfillment <a href="#fulfillment" id="fulfillment"></a>

**use\_oa\_percent**

The percent of Usage that can be fulfilled via as Green, Hybrid, or Bronze Open Access. Some of this content can be excluded in the settings (see the Open Access page for more info).

**use\_backfile\_percent**

The percent of Usage that can be fulfilled via your PTA (Post-Termination Access) rights.

\
**use\_subscription\_percent**

Percent of Usage that can be fulfilled ONLY via title-by-title subscription in this scenario--after fulfilling requests via Open Access and PTA fulfillment wherever possible.

**use\_ill\_percent**

Percent of Usage that is fulfilled via ILL in this scenario. This is simply turnaways (Usage that can't be fulfilled by Open Access, PTA, or your title-by-title subscriptions) multiplied by your ILL Request Rate parameter. This article has more details: [How do we calculate ILL requests and ILL cost?](../how-it-works/how-do-we-calculate-ill-requests-and-ill-cost.md)

**use\_other\_delayed\_percent**

Percent of Usage that is fulfilled via Unknown paths in this scenario. This all Usage that isn't fulfilled by Open Access, PTA rights, title-by-title subscription or ILL. Instead, the user fulfills their information need some other way -- asks the author for a paper, asks a colleague, finds another similar paper that is good enough for their purposes, etc.

**perpetual\_access\_years\_text**

The years when your institution has PTA (Post-Termination Access) to this title. Default: empty.

\
**baseline\_access\_text**

Optional text for those who have already left their Big Deals, to annotate which journals they'd previously subscribed to.

**bronze\_oa\_embargo\_months**

For some journals the publisher automatically makes the content free to read after a certain number of months. For those journals, this column lists the age of the articles (in months) when they will automatically become free to read on the publisher's site.

### &#x20;Usage Components <a href="#usage-components" id="usage-components"></a>

**downloads**

The number of times people in your institution will download papers from this journal. We base this on your COUNTER statistics and literature on [download decay curves](https://www.biorxiv.org/content/10.1101/795310v1) (how often an article is to be downloaded based on how long ago it was published).

**citations**

The number of times that a paper authored by someone in your institution will cite a paper in this journal. This number is based on the citations patterns of the previous five years. The importance of this number to overall Usage is determined by the Citation Weight parameter.

**authorships**

The number of papers in this journal that have at least one author from your institution. This number is based on the authorship patterns of the previous five years. The importance of this number to overall Usage is determined by the Authorship Weight parameter.

### Fuzzed <a href="#fuzzed" id="fuzzed"></a>

#### **\*\_fuzzed** <a href="#fuzzed" id="fuzzed"></a>

We include a few "fuzzed" columns, in case you want to share this data approximately but not exactly. For each column that's fuzzed, we ranked all the values in a column, then separated the values into three equal sized groups, and labelled them low, medium, and high. Low refers to the lowest value by rank, high refers to the highest value by rank, and medium in the middle. Where there is no value for the un-fuzzed value, we use a dash ("-").

If you want more fine grained resolution among titles you can refer to the un-fuzzed columns.\


\
