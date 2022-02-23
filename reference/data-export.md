---
description: >-
  Learn the details behind all the variables Unsub uses to forecast your costs
  and fulfillment
---

# Data export

The data fields in the Download as Spreadsheet are described here:

### Metadata <a href="#metadata" id="metadata"></a>

**issn\_l**

The primary ISSN we use for this journal (see issn.org [Linking ISSNs](https://www.issn.org/understanding-the-issn/assignment-rules/the-issn-l-for-publications-on-multiple-media/))

**title**

The title of this journal.

**subject**

The Elsevier-assigned Subject. Will be deleted soon, in favor of era\_subjects (below).

**era\_subject**

Subjects assigned to the journal by Excellence in Research for Australia (ERA) \[[source](https://www.arc.gov.au/excellence-research-australia/era-2018-journal-list)].

### Summary <a href="#summary" id="summary"></a>

**cpu**

This is the Cost per Use (CPU) of the journal. We use a more advanced variant of CPU (internally we call this Net Per Paid Use, or NCPPU). This CPU calculation is the net cost (subscription minus ILL), divided by Paid Use (Usage that can't be met with free sources). This is our most important measure of journal value--it summarizes the real value you're getting for your subscription dollar. This article has more details: [How do we calculate cost-effectiveness (Cost Per Use, CPU)](https://intercom.help/get-unsub/en/articles/4061107-how-do-we-calculate-cost-effectiveness-cost-per-use-cpu)

**cpu\_rank**

The journal's rank according to CPU, relative to other journals in this dataset. The most cost-effective journal has a rank of 1.\


**subscribed**

TRUE if you currently have the journal modeled as "subscribed" in your scenario, FALSE if the journal is currently "unsubscribed"

**cost**

The cost of this journal according to the Settings and Subscription status of the journals in this Scenario. It will be either Subscription Cost or ILL Cost (see next columns), depending on whether the journal is currently subscribed to or not in this scenario.

**usage**

The projected Usage of the journal by your institution. Usage is a measure of the journal's value to your institution. It is calculated as:

`Usage of a journal =`

`Downloads from the journal`

`+ (Citations to the journal by your authors) * (citation weight)`

`+ (Authored papers in the journal) * (authorship weight)`

**instant\_usage\_percent**

The percent of Usage that is available instantly -- available as Open Access, PTA, or Subscription.

**free\_instant\_usage\_percent**

The percent of Usage that can be fulfilled via Open Access or PTA. This excludes usage met only by ILL or Subscription.

\


### Costs <a href="#costs" id="costs"></a>

**subscription\_cost**

The title-by-title subscription cost of this journal. It includes a 'content fee' based on your settings, and annual price increases over the next five years (the cost shown is the average cost over the next five years). This data is based on public price lists unless you've uploaded a custom price list (available in a purchased account). This article has more details: [How do we calculate title-by-title subscription costs?](http://help.unsub.org/en/articles/4073469-how-do-we-calculate-title-by-title-subscription-costs)

**ill\_cost**

The ILL subscription cost of this journal. It is based on the ILL transaction cost and your ILL Request Rate, both of which are adjustable parameters. This article has more details: [How do we calculate ILL requests and ILL cost?](https://intercom.help/get-unsub/en/articles/4061177-how-do-we-calculate-ill-requests-and-ill-cost)

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

Percent of Usage that is fulfilled via ILL in this scenario. This is simply turnaways (Usage that can't be fulfilled by Open Access, PTA, or your title-by-title subscriptions) multiplied by your ILL Request Rate parameter. This article has more details: [How do we calculate ILL requests and ILL cost?](https://intercom.help/get-unsub/en/articles/4061177-how-do-we-calculate-ill-requests-and-ill-cost)

**use\_other\_delayed\_percent**

Percent of Usage that is fulfilled via Unknown paths in this scenario. This all Usage that isn't fulfilled by Open Access, PTA rights, title-by-title subscription or ILL. Instead, the user fulfills their information need some other way -- asks the author for a paper, asks a colleague, finds another similar paper that is good enough for their purposes, etc.

**perpetual\_access\_years**

The years when your institution has PTA (Post-Termination Access) to this title. Defaults to none.

\
**baseline\_access**

Optional text for those who have already left their Big Deals, to annotate which journals they'd previously subscribed to.

**bronze\_oa\_embargo\_months**

For some journals the publisher automatically makes the content free to read after a certain number of months. For those journals, this column lists the age of the articles (in months) when they will automatically become free to read on the publisher's site.

### OA Types <a href="#oa-types" id="oa-types"></a>

**use\_green\_percent**

The percent of Usage that can be fulfilled via Green OA. This is Open Access hosted on open repositories, like Harvard's institutional repository, arXiv, or PMC. Green OA that hasn't been peer-reviewed (preprints, submitted drafts, etc) can be excluded in the Parameters.

**use\_hybrid\_percent**

The percent of Usage that can be fulfilled via Hybrid OA. This is Open Access hosted on the publisher site with an open license in an otherwise subscription journal. Usually an APC was paid by the authors when they published this paper.

**use\_bronze\_percent**

The percent of Usage that can be fulfilled via Bronze OA. This is Open Access hosted on the publisher site in an otherwise subscription journal, but unlike Hybrid it does not have an open license. It is sometimes promotional material, and sometimes open after an embargo in a Delayed OA journal (like Elsevier's Open Archive content). Bronze OA can be excluded in the Parameters.

**use\_asns\_percent**

The percent of Usage that can be fulfilled via Academic Social Networks like ResearchGate and Academia.edu. These are not considered open repositories, so papers hosted here are not considered Open Access. These can be excluded in the settings.

**use\_peer\_reviewed\_percent**

Percent of Usage that can be fulfilled via a peer-reviewed full-text copy of the article. This includes all of Hybrid and Bronze, and the portion of Green OA that is an Accepted or Published version of the paper. Green OA that hasn't been peer-reviewed (preprints, submitted drafts, etc) can be excluded in the Parameters.\


### &#x20;Usage Components <a href="#usage-components" id="usage-components"></a>

**downloads**

The number of times people in your institution will download papers from this journal. We base this on your COUNTER statistics and literature on [download decay curves](https://www.biorxiv.org/content/10.1101/795310v1) (how often an article is to be downloaded based on how long ago it was published).

**citations**

The number of times that a paper authored by someone in your institution will cite a paper in this journal. This number is based on the citations patterns of the previous five years. The importance of this number to overall Usage is determined by the Citation Weight parameter.

**authorships**

The number of papers in this journal that have at least one author from your institution. This number is based on the authorship patterns of the previous five years. The importance of this number to overall Usage is determined by the Authorship Weight parameter.

### Fuzzed <a href="#fuzzed" id="fuzzed"></a>

#### **\*\_fuzzed** <a href="#fuzzed" id="fuzzed"></a>

We include a few "fuzzed" columns, in case you want to share this data approximately but not exactly. We've broken the values into three groups of approximately the same size, and labelled them low, medium, and high.\


\
