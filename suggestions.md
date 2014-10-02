# Suggestions

A few suggestions for the alpha-phase of the CGSL archive:

* establish a set of conventions for curating gesture/sign-focused research
  collections
* curate a collection to serve as paradigm, illustrating those conventions
* design a custom interface for the databrary-backed collections you aim to curate
* contact databrary team to discuss collaboration on data deposit/sharing
  APIs, along the lines of the [dataverse APIs](http://thedata.harvard.edu/guides/dataverse-api-main.html)


#### How do we specify conventions for organizing data collections?

* use the [databrary planning guide](http://databrary.org/user-guide/contributing.html) as a starting point
* focus on one initial collection to serve as a paradigm
* define and document a data model for this target collection
* define and document a data model for future collections
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
* study
* measure


## Misc

* take advantage of all the thought and planning that went into the [databrary
  design docs](https://github.com/databrary/design)

* consider using databrary for authentication/permissions
  * [user-permissions](https://github.com/databrary/design/blob/master/wireframes/user-permissions-management-tree.png)
  * [study-permissions](https://github.com/databrary/design/blob/master/wireframes/study-permissions-management-tree.png)

* transcode video to [H.264/AAC format](video-formats.md)

* obtain a dedicated domain name (`archive.gslcenter.uchicago.edu`)
