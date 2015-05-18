# Prototype

A proof-of-concept **discovery interface for annotated media**. 

---

Behavioral datasets for the sign/gesture research community typically consist of recorded samples (videos) of subjects signing and/or gesturing.  These behavioral samples are then supplemented with "inline annotations", a running commentary on the sign/gesure behavior exhibited in the recording using a controlled vocabulary.  

These media samples and their time-stamped annotations can be converted into a format for web-based playback.  Further, the annotations can be indexed so as to enable interactive querying and immediate playback of particular behavorial patterns within a web browser.

This would effectively enable sign/gesure researchers to isolate instances of a particular sign, gesture, or any other behavior of interest, not just within a given sample, but across the overall collection/corpus.  By enabling linked playback at the timestamp of a given instance, a researcher could quickly find and view targeted behaviors.  

In other words, we want to show how to web-enable the interactive exploration of the underlying content (the annotated behavioral samples) of behavioral data collections.


## Objectives

* convert video samples to a standard format for web-based playback
* utilize current web-standards for timestamped video annotations
* index the annotations to enable interactive querying and playback
* develop a web-based interface for interactive querying/playback


## Resources

* [various examples](demos.md) of data-discovery web apps

* video/annotation playback (with web.vtt and track elements)
  * [demo](http://simpl.info/track/)
  * [track basics](http://www.html5rocks.com/en/tutorials/track/basics/)
  * [video basics](http://www.html5rocks.com/en/tutorials/video/basics/)
  * [`video.js` polyfill](https://github.com/videojs/video.js/blob/stable/docs/index.md)
  * [adding captions and subtitles](https://developer.mozilla.org/en-US/Apps/Build/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video)

* [crossfilter](http://square.github.io/crossfilter/) enables fast multidimensional filtering with coordinated views (multiple visualizations that summarize data along different dimensions, where filtering in one dimension updates the others).  

* [reductio](https://github.com/esjewett/reductio) is a nice complement to crossfilter, providing dependent aggregations.  
