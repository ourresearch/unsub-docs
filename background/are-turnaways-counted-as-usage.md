---
description: Titles with only turnaways may show up in your dashboard
---

# Are turnaways counted as usage?

Unsub modeling uses many parameters, [many of which are user-configurable](../reference/scenario-parameters.md). One of the many parameters we use is turnaways data.

COUNTER 5 includes turnaways data in the TR\_J2 file (named "Journal Access Denied").

We include all titles in the TR\_J2 file that have data for the metric **No\_License** unless they fall into one of the [exceptions explained here](why-dont-i-see-a-certain-title-in-my-dashboard.md).

We include those titles because they are cases of people attempting to access the full-text of an article that were redirected to the abstract.

In Unsub we want to account for what people want to read - regardless of whether they have access to full-text or not. This is why we include turnaways: to better account for everything users want to read.

Note**:** If you’re using COUNTER 4 we do not count turnaways because they are not included in COUNTER 4. However, if you use COUNTER 5 we do count turnaways.
