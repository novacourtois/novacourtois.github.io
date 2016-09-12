---
layout: post
title: Making CraigsList Better
---

A couple of years ago, I made a Chrome Extesion that extends CraigsList's functionality.

I decided to update it to remove a bunch of external dependencies, and make a nice landing page for the app as well. 

# Fixing Old Code

When I first made this, I was using jQuery for everything, and [Toastr](https://codeseven.github.io/toastr/) seemed to make itself useful as well.

Frameworks are better for everything, right?

Well, sometimes the best tool for the job is [Vanilla JS](http://vanilla-js.com/), and you should check it out sometime. 

It "is a fast, lightweight, cross-platform framework for building incredible, powerful JavaScript applications."

It required rewriting most of the code, but it was totally worth it, and it loads much quicker. I also wrote a simple pure css notification system for it that's much lighter than Toastr.

As far as bugs go, there was some issue with counting how many new posts there were, but that off-by-one error went away with the rewrite. 

# Conclusion

Check it out the project [here](https://lastvisited.herokuapp.com) and the code on [GitHub](https://github.com/novacourtois/craigslist-last-visited).
