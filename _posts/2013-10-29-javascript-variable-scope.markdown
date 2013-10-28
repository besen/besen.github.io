---
layout: post
title:  "Javascript variable scope"
date:   2013-10-28 21:00:00
categories: javascript
---

In JS, the only way to create scope is through functions. Unlike other
languages that have a more sane approach to programming, there is no block
scopes or anything like it. This leads to some curious behavior:

{% highlight js %}
(function() {
  var acc = 0;
  console.log('start');
  for (var i = 0; i < 3; i++) {
    setTimeout(function () {
      acc += i;
      console.log(acc);
    }, 0);
  }
  console.log('end');
})()
{% endhighlight %}

The output is:

{% highlight js %}
start
end
3
6
9
{% endhighlight %}

Since there is no block scope (or "for" scope for that matter), the reference
to "i" inside the setTimeout calls is updated for all functions. I'm using
setTimeout here as an example, but the same is true for anything that is called
asynchronously.

We need another function to get the desired behavior:

{% highlight js %}
(function() {
  var acc = 0;
  console.log('start');
  for (var i = 0; i < 3; i++) {
    (function (index) {
      setTimeout(function () {
        acc += index;
        console.log(acc);
      }, 0);
    })(i);
  }
  console.log('end');
})()
{% endhighlight %}


And now it makes sense!

{% highlight js %}
start
end
0
1
3
{% endhighlight %}


A final reminder: if you care about performance, don't create a function inside a
loop.
