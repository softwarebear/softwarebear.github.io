---
layout: post
title: Google Chrome preferences file exposes your browsing history
date: 2016-05-02T11:00:00Z
categories: jekyll update
---

So there's been a few emails circulating recently about Internet Explorer and Edge exposing your private browsing history and horror of horrors not being on our side.

Well how many of you have thought that Chrome was immune to this ... ?

Have a look inside your Preferences file ...

```
C:\Users\<username>\AppData\Local\Google\Chrome\User Data\Default\Preferences
```
... search for bits of your favourite website url inside this file ... chances are you will find it embedded in there somewhere ... along with it's friends.

Clearing your browser history cache of urls and such makes no difference to the content of this file.

The file also contains a mysterious section at the bottom ... encrypted ... would love to know what's in there.

You will need to kill ALL running Chrome instances in order to be able to successfully (and permanently) delete this file ... don't worry ... it doesn't seem to make much difference to your browsing experience (including passwords etc)... it's just the dodgy urls are now gone.

If the file returns within a few seconds and you haven't launched Chrome ... you didn't kill them all before you deleted the file ... this new file will have your urls in it again.

Not sure when they are written to this file though ... or if they still are ... but they seem to be historical from other machines on which I use Chrome with the same google account.