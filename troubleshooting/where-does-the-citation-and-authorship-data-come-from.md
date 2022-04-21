# Where does the citation and authorship data come from?

Currently data comes from [Microsoft Academic Graph](https://www.microsoft.com/en-us/research/project/academic/) (MAG). The data will come from [OpenAlex](https://openalex.org) in the future.&#x20;

There are a few different sources of this kind of data. We think MAG and OpenAlex are superior to the alternatives, and here's why. We think coverage is the most important factor when considering the Unsub use case. According to Harzing (2016) Coverage of MAG (and therefore OpenAlex as it's built on MAG) is better than WoS and at least as good as Scopus. Visser et al. (2020) found that MAG had the highest overall coverage of the set: MAG, WoS, Scopus, Dimensions and Crossref.&#x20;



References:&#x20;

Harzing, A.-W. (2016). Microsoft Academic (Search): a Phoenix arisen from the ashes? Scientometrics, 108(3), 1637–1647. [https://doi.org/10.1007/s11192-016-2026-y](https://doi.org/10.1007/s11192-016-2026-y)

Visser, M., van Eck, N. J., & Waltman, L. (2020). _Large_-_scale comparison of bibliographic data sources: Scopus, Web of Science, Dimensions, Crossref, and Microsoft Academic_. [https://doi.org/10.48550/arXiv.2005.10732](https://doi.org/10.48550/arXiv.2005.10732)



### What years are included in calculating the citations and authorships data in the single journal view popup?

As of right now (April, 2022) the years we are pulling from to get citations and authorships data are: 2014-2021

### How does Unsub model authorships and citations?

It’s a linear extrapolation of current data. That is, if there’s 10 authorships in the Journal of Current Chemistry in the last year of data we have, then each future year we’d forecast 10 authorships. Citations works the same way.
