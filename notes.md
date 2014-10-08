## What makes behavioral research collections unique?

In the variegated area of infrastructure for behavioral research, we need to think through the practices and conventions for organizing collections of research studies.

In the behavioral sciences, significant emphasis is placed on observation.  A behavioral scientist aims to confirm their hypothesis with behavioral evidence.  Given this observational imperative, a research study typically requires capturing phenomenal streams (video recordings) of the behavior of study participants, which must be observed and annotated in accordance with a rigorous specification of observational criteria.

* phenomenal streams (continuous / unstructured)
* observations / annotations (segmented / structured)

In other words, the data collected in the course of a study consists in part of **annotated streams** of participant behavior.  For cohort studies, these annotated streams are often called **sessions**.  This is typically supplemented with various attributes and measures collected for each **participant**.  These attributes and measures permit various participant and session **groupings**.

Note that the captured video of partipant behavior is an information channel that
requires filtering, segmentation, and decoding on the part of the researcher, whose observations are re-encoded in the form of annotations.

Once a behavioral stream has been annotated, the researcher can then use those
annotations to query, filter, and transform particular slices of observed
behaviors.

This may all seem very obvious to the behavioral researcher, but I think it's
important to highlight how behavioral research data is actually collected and
annotated, because this is what makes behavioral datasets unique.


## What should the CGSL undertake with its limited grant funding?

We would suggest that you focus on ...

* interactive explorability rather than dataset discoverabilty
* a simple and secure media access API
* basic curation standards for the GSL research community (dataset packaging
  conventions)

To elaborate ...

The CGSL should focus on developing a discovery interface for annotated media, in particular the ability to identify particular behavioral patterns within a collection of annotated media streams, with immediate playback. (This would be achieved by indexing typed annotations and the use of crossfilter for interactive filtering.)

Databrary should serve as the primary catalog for collection discovery and basic access. The CGSL repository could then provide enhanced access to these contributed collections in the form of the aforementioned interface for exploratory data analysis, which will enable researchers to do fast multidimensional filtering of annotation types via coordinated views (multiple visualizations that summarize observations along different annotation dimensions, where filtering in one annotation dimension updates the others.)

The CGSL repository should also provide an http-based media interface, a simple and secure API for dynamically accessing the repositories annotated media: i.e., media access points specified via url path and query parameter encoded timestamps. 


## How to specify the structure (data model) of behavioral datasets?

Two suggestions:

* [dspl](https://developers.google.com/public-data/docs/tutorial#overview) -
  Google's Dataset Publishing Language
* [tabular data packages](http://dataprotocols.org/tabular-data-package/) - JSON-based spec

We would recommend the latter, because it is more lightweight and developer
friendly.


## How should behavioral datasets be packaged?

Recommendation: as [tidy data]() encapsulated as [dat]() databases with
[datapackage]() manifests.


## How to query behavioral datasets?

Use [Lucene-style indexing](https://github.com/fergiemcdowall/search-index) and
http search API via [forage.js](http://fergiemcdowall.github.io/norch/#search-api)


## How to interactively explore behavioral datasets?

Via [crossfilter](http://square.github.io/crossfilter/), which enables fast
multidimensional filtering for coordinated views (multiple visualizations that summarize data along different dimensions, where filtering in one dimension updates the others).  Note that [reductio](https://github.com/esjewett/reductio) is a nice complement to crossfilter, providing dependent aggregations.  

