---
layout: with-comments
title: "Simple Apache Access Log Analysis"
author: James Pearson
author_url: http://github.com/xiongchiamiov
summary: Sometimes you just want to quickly pull out a little information.
---

<i>This post was originally published on [It Broke And iFixit](http://itbrokeand.ifixit.com/2012/08/16/simple-apache-access-log-analysis.html).</i>

Although there exist [excellent tools][awstats] for doing full log analysis,
sometimes you just want to quickly pull out a little information.  I recently
found myself wanting to parse a section of our Apache access logs and find IPs
consistently hitting the same URLs over and over.  This lead to a line of
`awk`, `sort`, `uniq` and `grep` chained together with pipes; since that didn't
handle variations very well, it's now a line of `awk`, `sort`, `uniq` and
`grep` chained together with pipes and wrapped in a little bit of Ruby. :)

<script src="https://gist.github.com/3252053.js?file=analyze_access_log.rb"></script>
Here is [the Github gist][gist].

[awstats]: http://awstats.sourceforge.net/
[gist]: https://gist.github.com/3252053

