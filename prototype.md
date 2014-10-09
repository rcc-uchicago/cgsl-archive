# Prototype

A proof-of-concept **discovery interface for annotated media** demonstrating how behavioral data collections could be interactively explored.

The objective would be to develop an interface that enables sign/gesture researchers a way to interactively explore particular behavioral patterns within a collection of annotated media streams, with immediate playback. (This would be achieved by indexing typed annotations and the use of crossfilter/reductio for interactive filtering/aggregating.)

> [crossfilter](http://square.github.io/crossfilter/) enables fast multidimensional filtering for coordinated views (multiple visualizations that summarize data along different dimensions, where filtering in one dimension updates the others).  [reductio](https://github.com/esjewett/reductio) is a nice complement to crossfilter, providing dependent aggregations.  

By indexing the annotation associated with a video, you could enable
interactive exploration of annotation codes or keywords in order to isolate behavioral instances within the overall collection that are of particular interest.  By enabling linked playback at the timestamp of a given instance, a researcher could quickly find and view targeted behaviors.


## Resources

Demos and resources related to the proposed features:

* [various examples](demos.md) of data-discovery web apps

* video/annotation playback (with web.vtt and track elements)
  * [demo](http://simpl.info/track/)
  * [track basics](http://www.html5rocks.com/en/tutorials/track/basics/)
  * [video basics](http://www.html5rocks.com/en/tutorials/video/basics/)
  * [`video.js` polyfill](https://github.com/videojs/video.js/blob/stable/docs/index.md)
  * [adding captions and subtitles](https://developer.mozilla.org/en-US/Apps/Build/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video)

