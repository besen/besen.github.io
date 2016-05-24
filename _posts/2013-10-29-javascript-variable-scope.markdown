---
layout: post
title:  "Javascript variable scope"
date:   2013-10-28 21:00:00
categories: javascript
---

In JS, the only way to create scope is through functions. Unlike other
languages that have a more sane approach to programming, there is no block
scopes or anything like it. This leads to some curious behavior:

{% gist besen/d98d82b50fa6c4457db679f3bc4d6650 no-scope.js %}

The output is:

{% gist besen/d98d82b50fa6c4457db679f3bc4d6650 no-scope-output.txt %}


Since there is no block scope (or "for" scope for that matter), the reference
to "i" inside the setTimeout calls is updated for all functions. I'm using
setTimeout here as an example, but the same is true for anything that is called
asynchronously.

We need another function to get the desired behavior:

{% gist besen/d98d82b50fa6c4457db679f3bc4d6650 yes-scope.js %}


And now it makes sense!

{% gist besen/d98d82b50fa6c4457db679f3bc4d6650 yes-scope-output.txt %}


A final reminder: if you care about performance, don't create a function inside a
loop.
