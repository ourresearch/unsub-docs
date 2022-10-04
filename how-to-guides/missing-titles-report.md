# Missing titles report

Your Unsub dashboard may not include all the titles you uploaded in your COUNTER reports files. See our [Why don't I see a certain title in my dashboard?](../troubleshooting/why-dont-i-see-a-certain-title-in-my-dashboard.md) page, which details the four major reasons why a title could be missing.

In your package Setup tab, under the **Diagnostic data** section, you will find a Missing Titles page which allows you to download a spreadsheet.

In the spreadsheet there are two informational columns (issn\_l, publisher), and four columns for the four reasons a title could be excluded from a scenario. The columns are:

* **issn\_l**: The linking ISSN, or ISSN-L
* **publisher**: The publisher, according to [OpenAlex](https://openalex.org/)
* **gold\_oa**: `True` if OpenAlex thinks the journal is Gold Open Access (OA), otherwise `False`. We can not include titles that are Gold OA because there is no subscription access route, and we currently require that
* **not\_currently\_publishing**: `True` if we think the journal is no longer publishing, otherwise `False`. This determination is based on data from OpenAlex
* **price\_not\_available**: `True` if there is not title price, otherwise `False`. You can fix this by [uploading title prices](upload-title-prices.md). We require title prices for a title to be included in the dashboard
* **filtered\_out**: `True` if you filtered the title out using the optional Journal Filter setup step, otherwise `False`. Read the docs for [journal filter](upload-journal-filter.md)



Here's an example of four rows of the report you'll download:

| issn\_l   | publisher | gold\_oa | not\_currently\_publishing | price\_not\_available | filtered\_out |
| --------- | --------- | -------- | -------------------------- | --------------------- | ------------- |
| 2053-9711 | OUP       | True     | False                      | False                 | False         |
| 0007-0912 | Elsevier  | False    | False                      | True                  | False         |
| 1473-6691 | SAGE      | False    | False                      | True                  | False         |
| 0024-6093 | Wiley     | False    | True                       | False                 | False         |



A few notes about the data:

* A title can be missing for more than one reason. For example, it can be Gold OA and missing a title price.
* For some titles you can change something so it appear in your dashboard. For example, if a title price is missing you can get a title price; if you've filtered the title out you can remove the title from your filtered titles upload. However, if the title is Gold OA or is no longer publishing, nothing can be done to make it appear in your dashboard.
* Check out the [OpenAlex documentation](https://docs.openalex.org/) for more about OpenAlex.



After looking at the report [email us (support@unsub.org)](mailto:support@unsub.org) if you think any of the titles should be included in your scenarios for this package, and we'll have a look.
