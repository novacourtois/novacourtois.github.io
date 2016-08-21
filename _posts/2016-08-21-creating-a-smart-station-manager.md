---
layout: post
title: Creating a Smart Station Manager
tag: 🍞
---

# What's a Station Manager?
Running a tournament, even with bracketing software like [Challonge](http://challonge.com/) can be a difficult thing.

You need to keep track of how many 'stations' you have - a CRT + Gamecube, for SSBM tournaments, which ones are being occupied, and who is playing on them. 

The latest feature of my open source app, [ChallongeTO](http://challonge.com/), solves this problem.

Previously, I was just using an input field but that had too many problems: 

* Assigning multiple matches to the same station
* Not keeping track of a station's availability

Building this out was pretty tough from a technical standpoint. Having to talk to the [Challonge API](http://api.challonge.com/v1) and syncing the data with localStorage asynchronously took quite a bit coding and debugging. 

Populating the select options correctly was pretty neat!

```html
<option class="form-control" ng-repeat="station in stations | orderBy: ['name.length','name']" value="{{station.name}}" 
   ng-if="station.match == match.match.id || !station.id">
   	{% raw %}{{station.name}}{% endraw %}
</option>
```

I ran some test tournaments to verify everything was working, but I'm super excited to see how this holds up in the wild because tournaments can be hectic.