---
layout: post
title:  "BrazilJS - Part 1"
date:   2013-08-26 21:20:00
categories: javascript
---

I had the pleasure of going to the [BrazilJS 2013 conference](http://braziljs.com.br) last week. After 5 hours inside a car with my friends [Munhoz](http://twitter.com/fnmunhoz) and [Ragonha](http://twitter.com/pirelenito), we got to see a nice sunrise, but that was the last time we saw the sun in Porto Alegre.

<a href="http://www.flickr.com/photos/96377435@N08/9601145487/" title="Sunrise @ Porto Alegre por renatobesen, no Flickr"><img src="http://farm4.staticflickr.com/3810/9601145487_073b8cda89.jpg" width="500" height="375" alt="Sunrise @ Porto Alegre"></a>

Even with the bad weather, BrazilJS was one of the best technology conferences I've ever attended. Outstanding organization, good infrastructure, amazing speakers. The only thing that comes to my mind that can be improved is the Internet connection, but many of the speakers made sure the the organizers ought to fix this next year, so I don't need to stress this point.

<a href="http://www.flickr.com/photos/96377435@N08/9604377150/" title="Sem título por renatobesen, no Flickr"><img src="http://farm8.staticflickr.com/7420/9604377150_7c3fe7d8d8.jpg" width="500" height="331" alt="Sem título"></a>

I will post my impressions about the talks. More will follow on the coming days.

###Utilizando node.js para automação de build e deploy ([Mauricio Wolff](https://twitter.com/bitbonsai))
<a href="http://www.flickr.com/photos/96377435@N08/9601141007/" title="Sem título por renatobesen, no Flickr"><img src="http://farm8.staticflickr.com/7402/9601141007_c2c4e3e31a.jpg" width="500" height="331" alt="Sem título"></a>

Mauricio showed a dell.com case, where they built a internal tool to automate some development and deployment tasks. One of the most interesting aspects of this talk for me was the tool [jshint-inline](https://github.com/bitbonsai/jshint-inline), that does static analysis of javascript even if it is inside of a script tag in a HTML file. For executing tasks, instead of using an existing tool (a.k.a. [grunt](http://gruntjs.com/)) they decided to develop their own tool, a decision which was questioned by a lot of people. The answer during the Q&A part of the talk was that grunt has a steep learning curve. Yeah, right. Anyway, the tool solves their problem, and that was the message of the talk: it is easy to automate stuff with node.js.

[Slides](http://bitbonsai.com/braziljs2013/)

###Learning to fly - Twitter Flight and mixin ([Angus Croll](https://twitter.com/angustweets))
<a href="http://www.flickr.com/photos/96377435@N08/9601142151/" title="Sem título por renatobesen, no Flickr"><img src="http://farm8.staticflickr.com/7381/9601142151_b30d678c79.jpg" width="500" height="331" alt="Sem título"></a>

This talk was on the dense side of the spectrum (and that is good). Angus explained some ways to share behavior between objects in javascript, and finally spoke about what he called functional mixins. A very interesting concept, that is used on the [flightjs](http://flightjs.github.io/) project, a library used to map behavior to DOM nodes on multiple twitter products. This one deservers deeper studies.

[Slides](https://speakerdeck.com/anguscroll/learning-to-fly-twitter-flight-and-mixins-1)

###Performance as a Twitter feature ([Marcel Duran](https://twitter.com/marcelduran))
<a href="http://www.flickr.com/photos/96377435@N08/9604378320/" title="Sem título por renatobesen, no Flickr"><img src="http://farm3.staticflickr.com/2806/9604378320_9b8d942ebf.jpg" width="500" height="331" alt="Sem título"></a>

Continuing with the twitter personnel, Marcel spoke about how to deal with performance as a feature. Instead of only monitoring performance in production, he shows how to measure it in development time, and break builds if any degradation is detected. With this purpose in mind, some tools were showed, like the [webpagetest](https://code.google.com/p/webpagetest/). Marcel also created a [wrapper](https://github.com/marcelduran/webpagetest-api) for this project that can be installed through a npm package. The wrapper provides some command line tools, and can be easily used with a number of CI tools.

[Slides](http://www.slideshare.net/marcelduran/brazijs-2013-performance-as-a-feature)