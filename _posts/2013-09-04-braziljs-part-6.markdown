---
layout: post
title:  "BrazilJS - Part 6"
date:   2013-09-04 23:13:00
categories: javascript
---

_Last post: [part 5]({% post_url 2013-09-03-braziljs-part-5 %}).
_

<a href="http://www.flickr.com/photos/96377435@N08/9604366014/" title="end por renatobesen, no Flickr"><img src="http://farm3.staticflickr.com/2810/9604366014_7ea5288a27.jpg" width="500" height="331" alt="end"></a>

This is the end! Here are my last impressions of the event.

###Reactive JavaScript ([Stoyan Stefanov](https://twitter.com/stoyanstefanov))
<a href="http://www.flickr.com/photos/96377435@N08/9604364302/" title="Stoyan Stefanov por renatobesen, no Flickr"><img src="http://farm4.staticflickr.com/3798/9604364302_16c042c616.jpg" width="500" height="331" alt="Stoyan Stefanov"></a>

Stoyan spoke about [React](https://github.com/facebook/react), a framework used at Facebook and Instagram to build user interfaces. You can read a good overview of the talk on [Stoyan's blog](http://www.phpied.com/remarkable-react/). React offers a way to write components in JS, but because it's tedious to write down all the tags, there is an XML-like markup language (JSX) which can be compiled to the JS counterpart. Besides generating HTML, React components automaticaly update when the data changes, and also manages event handlers, attaching and detaching them when necessary. It's a weird framework.

[Slides](http://www.phpied.com/files/react/slides.html)

###Programming Style and Your Brain ([Douglas Crockford](http://crockford.com/))
<a href="http://www.flickr.com/photos/96377435@N08/9604365432/" title="Douglas Crockford por renatobesen, no Flickr"><img src="http://farm4.staticflickr.com/3824/9604365432_e84a7e0d80.jpg" width="500" height="331" alt="Douglas Crockford"></a>

While most of the other speakers were proud to say that the spent the previous night doing the slides, Douglas Crockford gave a well rehearsed talk (I bet even his jokes and the audience reaction is timed). Douglas spoke about why programming style is important, specialy in JS. When the style choice is purely visual, there is no point in arguing, it's only subjective. The styles that are important to follow are the ones that prevent errors. Semicolons in JS are "optional" in most cases, but sometimes the missing punctuation causes the program to behave in an unexpected way. And there are other examples, like always putting braces on ifs, increment operators, etc. These styles were the motivation behind [JSLint](http://www.jslint.com/). He argues that by using this, we can avoid a lot of errors, and the people that don't follow this styles are in four categories: under educated, old school, thrill seeker or exhibitionist. Makes sense.

[Slides](http://www.slideshare.net/webdirections/douglas-crockford-programming-style-and-your-brain-14858206)

And [this is it](http://www.youtube.com/watch?v=93Awzbla0yc). I'm looking forward for next year edition.
