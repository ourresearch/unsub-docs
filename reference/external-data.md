---
description: Details about external data used in Unsub
---

# External data

The following is a list of the external data sources used, including what they are used for, and how often the data is updated.

### Citations

Data source: [OpenAlex](https://docs.openalex.org/)

Update frequency: Quarterly (4x per year)

Used in Unsub: Journal level [Cost Per Use](cost-per-use-cpu.md) calculation (if you include citations in your [scenario parameters](scenarios/scenario-parameters.md#citation-and-authorship)). Citations data shown in [single journal view](single-journal-view.md) or in the table view in a scenario. Institutional level [APC Report](../how-to-guides/apc-report.md).

### Authorships

Data source: [OpenAlex](https://docs.openalex.org/)

Update frequency: Quarterly (4x per year)

Used in Unsub: Journal level [Cost Per Use](cost-per-use-cpu.md) calculation (if you include authorships in your [scenario parameters](scenarios/scenario-parameters.md#citation-and-authorship)). Authorships data shown in [single journal view](single-journal-view.md) or in the table view in a scenario. Institutional level [APC Report](../how-to-guides/apc-report.md).

### Journal metadata

This includes journal title, ISSNs, publisher, open access status, and whether title is currently publishing (based on date of last DOI published).

Data source: [OpenAlex](https://docs.openalex.org/)

Update frequency: Daily

Used in Unsub: Determine whether a journal should be included in Unsub dashboards or not (see [Why don't I see a certain title in my dashboard?](../troubleshooting/why-dont-i-see-a-certain-title-in-my-dashboard.md)), and as the source of truth to link together journals, user uploaded data, and any external journal level data.

### Journal embargo periods

Data source: Manually collected. We will soon switch over to using data from [oa.works](https://oa.works/)

Update frequency: Not currently updated

Used in Unsub: Shown in [single journal view](single-journal-view.md) in Unsub dashboards, and used in calculating [Cost Per Use](cost-per-use-cpu.md)

### Publisher societies

Data source: Manually collected.

Update frequency: Not currently updated

Used in Unsub: Shown in [single journal view](single-journal-view.md) in Unsub dashboards

### Number of papers

Data source: [OpenAlex](https://docs.openalex.org/)

Update frequency: Daily

Used in Unsub: Journal level usage forecast.

### ROR and Grid identifiers

Data source: Microsoft Academic Graph

Update frequency: Not currently updated; we'll switch to OpenAlex in the near future.

Used in Unsub: Used to link together many kinds of data (journals, authors, etc.) to institutions.

### APC prices

Data source: [We get these from publisher websites](../how-it-works/where-do-the-apc-prices-come-from.md).

Update frequency: Not updated

Used in Unsub: For the institutional [APC Report](../how-to-guides/apc-report.md) for the big five publishers (Elsevier, Wiley, Springer Nature, Taylor & Francis, SAGE) only.

### Unpaywall

Data source: [Unpaywall](https://unpaywall.org/)

Update frequency: Every 6 hours (4x/day)

Used in Unsub: xxx
