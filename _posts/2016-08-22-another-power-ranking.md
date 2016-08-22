---
layout: post
title: Another Power Ranking
---

# Intro

Power Ranking systems go hand-in-hand with competitive (e)sports. [SkillKeeper](https://github.com/SugoiFactory/SkillKeeper) is used often in the Smash community because it integrates with [Challonge](https://challonge.com), but updating results takes some time. 

The general process goes something like:
* Adding a new tournament link
* Manually handling player aliases
* Running the program
* Copy / pasting results - usually onto some Google Spreadsheet
* Adding characters
* maybe some more steps depending on the region

Most (if not all) of that can be automated and improved on.

# FGC Rank

I've been working on an automated PR system that hopefully alleviates this process for every region using Challonge for brackets. 

Once I release the beta version, I'll open source the code on my [GitHub](https://github.com/novacourtois).


## Technical Details

It's a MEAN Stack app that'll probably get hosted on Heroku. 

The front-end will be done with Angular Material + SASS. There probably won't be too much spectacular here, but I plan on throwing player data into charts so people can track their progress. 

All the excitement will be done on the back-end. Regions will be able to select their ranking algorithm (ELO / TrueSkill), and sit back after some initial set-up. 

Caveats:
* Aliases have to be dealt with manually (just once).
* Automation requires either the use of their Challonge account's api key, or manually entering a url (just one click).

## Current State

The back-end currently works(?) with ELO, and I've been testing with some data from my local SSBM scene.

Not sure when I'll be confident enough to share a link or code for this.

Working on [ChallongeTO](http://challonge-to.herokuapp.com/) is priority for me. Both are needed but time is limited.