---
layout: post
title:  "Denodeify"
date:   2013-11-18 21:00:00
categories: javascript
---

[Promises](http://wiki.commonjs.org/wiki/Promises/A) are all the rage this year, so I tought I'd join the club and do a post about it.

Last week I teamed up with some friends for the [Node Knockout 2013](http://2013.nodeknockout.com/)
(with a [great submission](http://cinemafu.com/), by the way) and used a LOT of promises on the server side.

Since promises are not a part of the core implementation of Node.js, callbacks are common pattern for the
standard lib and for other libs that don't have dependencies. In our case, promises prevented
a lot of nesting, which would be much more difficult to avoid using pure callbacks.

We used [RSVP.js](https://github.com/tildeio/rsvp.js) as our promise implementation, and made a bunch of calls to
[the movie db API](http://www.themoviedb.org/documentation/api). Wrapping [all those callbacks](https://github.com/raqqa/node-tmdb) in promises became a chore, so I thought there should be a better way to do this. That's when I decided to take a look at the source code of RSVP, and noticed the function "denodeify".

Using [request](https://github.com/mikeal/request) as an example, this handy function helps you transform this:

{% gist besen/c0ef10765a93345cb88e old-way.js %}

into this:

{% gist besen/c0ef10765a93345cb88e denodeify.js %}

Much better! There is no documentation of this in the RSVP main page, but [Q](https://github.com/kriskowal/q)
also has this and other utilities for adapting functions that take callbacks.
