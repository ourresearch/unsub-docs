# Where do we get Year of Publication data for PTA and open access calculations?

We get Year of Publication data from two sources: your COUNTER 5 TR\_J4 file, and the Unpaywall browser extension usage data patterns.

Where possible we use your COUNTER 5 TR\_J4 file to get Year of Publication data. Unfortunately, usage is often too sparse for a given journal to understand a robust pattern of usage by article-age.

When necessary, we supplement your COUNTER data with anonymized data from the Unpaywall browser extension (with its more than 250,000 active users) to understand the age and OA status of journal usage.

Our approach is specified in great detail in [this preprint](https://doi.org/10.1101/795310), but to summarize we use aggregated statistics about journal-level year of publication usage derived from usage of people with the Unpaywall browser extension installed. From their (aggregated) usage calls to our API (for OA papers and also paywalled papers), we can see what the age is of the papers that the 250,000 active users of the extension are reading in each journal. From there we can derive a "download decay curve" for each journal, and what % of the actual uses are OA at the time of access.

We've done testing and determined that although the interest in a journal may vary across universities, the relative interest of older vs newer papers within a given journal doesn't -- the shape of this curve is pretty constant. This let us get going before COUNTER 5 was in widespread use, works well even for low-usage journals and small schools, and also allows us to correlate this year of publication with green OA for example -- something that COUNTER 5's year of publication stats don't handle.
