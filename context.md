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

The CGSL should focus on developing a proof-of-concept **discovery interface for annotated media**, in particular an interface that enables researchers to interactively explore particular behavioral patterns within a collection of annotated media streams, with immediate playback. (This would be achieved by indexing typed annotations and the use of crossfilter/reductio for interactive filtering/aggregating.)

Databrary should serve as the primary catalog for collection discovery and basic access. The CGSL repository could then provide **enhanced access** to these contributed collections in the form of the aforementioned interface for exploratory data analysis, which will **enable researchers to do fast multidimensional filtering of annotation types via coordinated views** (multiple visualizations that summarize observations along different annotation dimensions, where filtering in one annotation dimension updates the others.)

In conjunction with the above, the CGSL repository could provide an http-based media interface, a simple and secure API for dynamically accessing the repository's annotated media: i.e., media access points specified via url path and query parameter encoded timestamps. 

