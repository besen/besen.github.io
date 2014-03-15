---
layout: post
title:  "BrazilJS - Part 5"
date:   2013-09-03 23:13:00
categories: javascript
---

_Last post: [part 4]({% post_url 2013-09-02-braziljs-part-4 %})._

<a href="http://www.flickr.com/photos/96377435@N08/9601140433/" title="hall por renatobesen, no Flickr"><img src="http://farm4.staticflickr.com/3740/9601140433_ecff9b906f.jpg" width="500" height="331" alt="hall"></a>


###O fantástico mundo do JavaScript ([Jean Carlo Emer](https://twitter.com/jcemer))
<a href="http://www.flickr.com/photos/96377435@N08/9604362806/" title="Jean Carlo Emer por renatobesen, no Flickr"><img src="http://farm6.staticflickr.com/5332/9604362806_61a9c2db4b.jpg" width="500" height="331" alt="Jean Carlo Emer"></a>

This talk caused a stir, showing some code without semicolons while Douglas Crockford was present in the room. What an outrage! That said, some nice concepts were presented, but I felt the content was too disconnected. Some parts looked like an introduction to javascript, and at the same time there was [CoffeScript](http://coffeescript.org/) code and mentions to [ES6](http://people.mozilla.org/~jorendorff/es6-draft.html), [AMD](https://github.com/amdjs/amdjs-api/wiki/AMD), transpilers, etc. Among the subjects of the talk were how JS supports OOP and functional programming, code modularization and some new features that are coming to the language. A lot to digest.

[Slides](https://speakerdeck.com/jcemer/o-fantastico-mundo-do-javascript)

###Workers of the web ([Thibault Imbert](https://twitter.com/thibault_imbert))
<a href="http://www.flickr.com/photos/96377435@N08/9601127743/" title="Thibault Imbert por renatobesen, no Flickr"><img src="http://farm4.staticflickr.com/3702/9601127743_889147e9d6.jpg" width="500" height="331" alt="Thibault Imbert"></a>

Thibault gave a primer on <s>Brazilian disco-funk</s> [WebWorkers](http://dev.w3.org/html5/workers/), showing how and why to use them. The slides are pretty detailed, and there is also a [companion post for the talk](http://typedarray.org/concurrency-in-javascript/). WebWorkers come in handy when you need to perform some computation and doesn't want to block UI rendering. Currently there are two communication models to work with them (message cloning and transfer of ownership), but neither are suitable to do paralelization. It's also nice to know that they are widely supported, and easy to detect and fallback to other strategies if necessary.

[Slides](https://dl.dropboxusercontent.com/u/7009356/Workers%20of%20the%20web%20-%20BrazilJS.pdf)

###NodeJS, the good, the bad and the ugly([Caridy Patiño](https://twitter.com/caridy))
Besides being subject of presentations, [node.js](http://nodejs.org/) has other more practical uses. Caridy showed for what kind of applications node is a good fit, and gave some tips on what to do and what not to do when using node. For web applications, debugging is hard to do (I guess the problem here is the tooling is not there yet). The GC also poses a problem, and object creation should be minimized. Session, authorization and caching are tricky to do on node, and should also be avoided. On the other hand, server and client can share code, it's easy to package JS applications for the web and there are loads of new libs being created for node every day. Another class of application for node are CLI tools. In this case, the advantages are the async nature of the plataform (which can provide some speed with the non-blocking APIs), support for multiple platforms and the [NPM](https://npmjs.org/).

[Slides](https://dl.dropboxusercontent.com/u/31422156/braziljs-2013.pdf)
