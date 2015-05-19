# CGSL Prototype

A proof-of-concept **discovery interface for richly-annotated media**. 


## Overview 

Behavioral datasets for the sign/gesture research community typically consist of recorded video samples of subjects signing/gesturing.  These behavioral samples are then supplemented with "inline annotations", a running commentary on the sign/gesure behavior exhibited in the recording using a controlled vocabulary.

In the context of behavioral research, observational recordings are often
"coded" with multiple tiers of annotations, each tier encoding instances of a particular type of behavior: specific syntactic, semantic, or pragmatic features exhibited.  In other words, beyond simple captioning or sub-titling, behavioral recordings are supplemented with a tiered set of timestamped annotations.

These media samples and their annotations can be converted into a format for web-based playback.  Further, the annotations can be indexed so as to enable interactive querying and immediate playback of particular behavorial patterns.  This would enable sign/gesture researchers to isolate instances of a particular sign or gesture (or any other coded behavior or attribute of interest), not just within a given sample, but across the overall collection/corpus.  By enabling linked playback based on the timestamp of a given instance, a researcher could quickly find a specific range of targeted behaviors and easily view instances of such behaviors in context, iteratively refining the query parameters as needed.  The envisioned query interface will let researchers specify the particular attributes of study subjects and their behaviors they'd like to isolate and view in context.

In sum, we'd like to build a working demonstration of a discovery interface for
richly annotated media.   This will be of particular value to the behavioral
research community, enabling interactive exploration of the underlying content
of their data collections.  


## Statement of Work

For the proposed project, we'll be utilizing sample video recordings provided by
the [Center for Gesture, Sign, and Language](https://gslcenter.uchicago.edu/): recordings of subjects that have been annotated for their signing and gestural behavior.

In addition to the inline annotations, each sample recording contains a small
set of metadata attributes: subject ID, session ID, subject gender, subject age, etc.  We would like to enable search/querying of both the annotation codes and metadata attributes (age, gender, etc.) of the provided video samples.

To accomplish this, we'll need to ...

* convert the sample video recordings to [an appropriate media format](https://developer.mozilla.org/en-US/docs/Web/HTML/Supported_media_formats) for web playback (viz., the MP4 container format with the H.264 video codec and the AAC audio codec)

* convert the video annotations to [WebVTT](https://developer.mozilla.org/en-US/docs/Web/API/Web_Video_Text_Tracks_Format) format 

* utilize WebVTT's [metadata tracks](https://docs.webplatform.org/wiki/concepts/VTT_Captioning#Metadata_Tracks) to preserve the structured/tiered annotation accompanying each recording

* create an appropriate [analyzer](https://github.com/blevesearch/bleve/wiki/Text-Analysis#text-analysis-in-bleve) for the provided sign/gesture annotations

* use our custom analyzer to index the annotations

* develop a web-based interface for interactive querying/playback of annotation codes and metadata attributes (age, gender, etc.), which should permit both [faceted searching](https://github.com/blevesearch/bleve/wiki/Result-Faceting) and [multi-dimensional filtering](http://square.github.io/crossfilter/).

Video content will be hosted on the RCC Midway cluster in the CGSL's dedicated
storage space.  We'll transcode the video samples on Midway scratch space,
converting the media files in parallel; similarly, for the conversion of
accompanying annotations to WebVTT format and subsequent indexing.

A virtual-machine on the Midway cluster will be allocated for hosting a dedicated MySQL database, needed for persisting and querying the metadata
accompanying each video recording.  This VM will also host a dedicated web
server and the [query engine](http://www.blevesearch.com/) for our annotation indices.


## Resources

* video annotation and playback (with WebVTT and track elements)
  * [track demo](http://simpl.info/track/)
  * [track basics](http://www.html5rocks.com/en/tutorials/track/basics/)
  * [video basics](http://www.html5rocks.com/en/tutorials/video/basics/)
  * [vtt captioning - I](https://docs.webplatform.org/wiki/concepts/VTT_Captioning)
  * [vtt captioning - II](https://developer.mozilla.org/en-US/Apps/Build/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video)

* [bleve](http://www.blevesearch.com/) is a text indexing library
  supporting custom analyzers and flexible querying
  * [bleve-explorer](https://github.com/blevesearch/bleve-explorer) is an example
    app providing an HTTP/REST/JSON front-end to bleve

* [crossfilter](http://square.github.io/crossfilter/) enables fast multidimensional filtering with coordinated views (multiple visualizations that summarize data along different dimensions, where filtering in one dimension updates the others)

* [various examples](demos.md) of data-discovery web apps

