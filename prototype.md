# Prototype

**Create a searchable collection with video/annotation playback.**

By indexing the annotation associated with a video, you could enable searching
of annotation codes or keywords in order to isolate instances within the overall collection that are of particular interest.  By enabling linked playback at the timestamp of a given instance, a researcher could quickly view targeted behaviors.


## Suggestions

* focus on one clean, small, open collection
* use a simple data model
* use a simple authentication scheme (full access once authenticated)


## Resources

Demos and resources related to the proposed features:

* video/annotation playback (with web.vtt and track elements)
  * [demo](http://simpl.info/track/)
  * [track basics](http://www.html5rocks.com/en/tutorials/track/basics/)
  * [video basics](http://www.html5rocks.com/en/tutorials/video/basics/)
  * [`video.js` polyfill](https://github.com/videojs/video.js/blob/stable/docs/index.md)
  * [adding captions and subtitles](https://developer.mozilla.org/en-US/Apps/Build/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video)

* simple query interface to search for instances of specified annotation
  with constraints
  * [indexing of annotation](https://github.com/dominictarr/level-inverted-index#level-inverted-index)
