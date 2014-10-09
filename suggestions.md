# Suggestions

In light of the [context](context.md) and [funding](funding.md) situation, here
are a few suggestions for the alpha-phase of the proposed CGSL project:

* establish a set of conventions for curating gesture/sign-focused research
  collections
* curate a collection to serve as paradigm, illustrating those conventions
* contact databrary team to determine availability of data deposit/sharing
  APIs (whether something exists along the lines of the [dataverse](http://thedata.harvard.edu/guides/dataverse-api-main.html) or [ckan](http://docs.ckan.org/en/latest/api/index.html) APIs) and data packaging conventions
* utilize databrary for dataset publishing/discoverability and controlled
  access to dataset resources
* develop a [prototype](prototype.md) demonstrating enhanced access to contributed collections that's focused on enabling [interactive explorability](https://github.com/joyrexus/rcc/blob/master/services/demos.md) (described below) rather than dataset discoverabilty
* develop a simple and secure media access API
  
To elaborate on a few of these points ...

The CGSL should focus on developing a proof-of-concept **discovery interface for annotated media**, in particular an interface that enables researchers to interactively explore particular behavioral patterns within a collection of annotated media streams, with immediate playback. (This could be achieved by indexing typed annotations and the use of [crossfilter](http://square.github.io/crossfilter/)/reductio for interactive filtering/aggregating.)

Databrary should serve as the primary catalog for collection discovery and basic access. The CGSL repository could then provide **enhanced access** to these contributed collections in the form of the aforementioned interface for exploratory data analysis, which will **enable researchers to do fast multidimensional filtering of annotation types via coordinated views** (multiple visualizations that summarize observations along different annotation dimensions, where filtering in one annotation dimension updates the others.)

In conjunction with the above, the CGSL repository could provide an http-based media interface, a simple and secure API for dynamically accessing the repository's annotated media: i.e., media access points specified via url path and query parameter encoded timestamps. 


#### How to specify conventions for organizing data collections?

* use the [databrary planning guide](http://databrary.org/user-guide/contributing.html) as a starting point
* focus on one initial collection to serve as a paradigm
* define and document a data model for this target collection
* define and document a data model template for future collections
* again, the [data model suggestions](http://databrary.org/user-guide/contributing/definitions.html) provided by databrary might be a good starting point


#### What is a "data model"?

Rather than provide a simple, flat-file storage service, a data repository like databrary can represent the **structure of the studies**. 

> Databrary's "back end" is a relational database that allows researchers to store and share research data in a structured way. Most developmental scientists, indeed most research psychologists, take measures from participants at particular places and times. Databrary's data model enables researchers to upload information about the settings (place, time, who conducted the study), participants (age, sex, race, ethnicity, and other person-specific variables), and measures (tasks, behaviors, questionnaires, physiological recordings, etc.) that are involved in behavioral research. Databrary keeps that information intact and structures it for visualization and for search. This means that we have to build ways for researchers to upload their data in ways that are familiar to them, like spreadsheet-like interfaces or multi-track timelines for temporally dense data streams like videos or eye-tracking. It also means we have to store the relationships between data elements, including their temporal relations -- what happened when -- in powerful and flexible ways that will enable others to use the data in the future. (See [full blog post](http://rick-gilmore.org/lets-get-relational.html), which describes how the Databrary team is attempting to build "a system that does what no other data sharing service I know about does -- **understands experimental design**.") 

So, a "data model" for a study is just a way of specifying the types of "things" included in your study, their attributes and relationships.  E.g., ...

* investigator
* participant
* collection
* session
* visit
* video
* group
* measure


#### How to specify the structure (data model) of behavioral datasets?

Utilize one of the following protocols:

* [dspl](https://developers.google.com/public-data/docs/tutorial#overview) -
  Google's Dataset Publishing Language
* [tabular data packages](http://dataprotocols.org/tabular-data-package/) - JSON-based spec

We would recommend the latter (more lightweight and developer-friendly).


#### How to package a behavioral dataset?

As [tidy data](https://github.com/jtleek/datasharing#the-tidy-data-set) encapsulated as a [dat](http://dat-data.com/) database with a
[tabular data package](http://dataprotocols.org/tabular-data-package/) manifest.

Standardised packaging formats have the ability to drastically simplify the
process of discovering, retrieving, and managing data.

See brief intro to data packaging [here](https://github.com/nickstenning/put-it-in-a-box/blob/master/talk.md#introducing-the-data-package).


#### How to query behavioral datasets?

Use [Lucene-style indexing](https://github.com/fergiemcdowall/search-index) and
http search API via [forage.js](http://fergiemcdowall.github.io/norch/#search-api)


#### How to interactively explore behavioral datasets?

Via [crossfilter](http://square.github.io/crossfilter/), which enables fast
multidimensional filtering for coordinated views (multiple visualizations that summarize data along different dimensions, where filtering in one dimension updates the others).  Note that [reductio](https://github.com/esjewett/reductio) is a nice complement to crossfilter, providing dependent aggregations.  


## Misc

* use the [tabular data package](http://dataprotocols.org/tabular-data-package/)
  format as a convention for packaging collections (resources and metadata)

* consult this concise [data sharing guide](https://github.com/jtleek/datasharing), with useful suggestions for coding variables and documenting your schema

* consider and take advantage of all the thought and planning that went into the [databrary design docs](https://github.com/databrary/design)

* determine whether databrary supplies an authentication API for
  determining permission level status on contributed dataset resources

* transcode video to [H.264/AAC format](video-formats.md)
