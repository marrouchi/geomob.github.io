--- 
layout: post
title: "Open Geo interview series - Chris Sheldrick"
date: 2014-10-06 11:28:33 +0000
tags: interview what3words ChrisSheldrick2
---
Welcome back to another round of our interview series with geo thought-leaders. Today we chat with [Chris Sheldrick](https://twitter.com/ChrisSheldrick2) of [what3words](http://what3words.com/). What3words takes a totally fresh approach to addressing/location finding, and is a great idea of innovation in the space. We recently [integrated what3word codes as an annotation into the OpenCage geocoder](http://blog.opencagedata.com/post/98146531423/what3words-now-provided-as-an-annotation).

**1\. Who are you, what is your background in geo?**

_I’m Chris Sheldrick, co-founder and CEO of what3words. Prior to starting what3words, I worked in the music & events businesses for 10 years, and it never dawned on me that I was in fact working (partly) in location: a big part of our job was getting a lot of people to a specific (normally unaddressed) location at a specific time on a specific day. We did this several days a week, all over the world. Having suffered the frustrations of the inefficiencies involved in this process for such a long period, I started thinking about ways to improve it, and I came up with what is now what3words._

**2\. What is What3Words, why does the world need it?**

_Street addresses were not intended to be all-encompassing references for every spot of land, all of the world, to be used by people of different languages and cultures. However, we now live in a world where people expect to be able to go anywhere, anytime, easily – street addresses are not a perfect universal point reference system to achieve this. Whilst efforts are made to bend street addresses for this purpose, we feel that starting at square one and producing a new system that bypasses street addresses, can serve users far better for point references. We’ve started by looking at the most accurate form of point referencing – GPS co-ordinates (latitude and longitude); perfect for immense accuracy and for doing maths within geo applications, but it’s unsuitable for everyday consumer use at 16 or so digits plus a few letters to get to a few meters’ accuracy. With what3words, we’ve preserved the accuracy of the 16 digits and few letters, but converted the format into something far more suitable for consumer use and understanding, sequences of 3 words. With 57 trillion squares of 3m x 3m around the world, we have assigned a unique combination of 3 words to each. By using just these 3 words, users can be talking about locations with high precision, before you can say 51° 39’ 21.434" N 0° 23’ 38.432" W – literally. We then replicate the system across a range of other languages (currently 8) – so each 3m x 3m square ends up with a 3 word combination in each language we are live in. Users can then choose to experience the world in their 3 word language of choice._

**3\. Where and how are people using it? Any surprises or differences to what you anticipated?**

_We’ve seen adoption all over the world, although most in Russia, The Middle East, India, and then the UK & US. The Middle East was always one of our focus areas as the entire region struggles with addressing – what3words will always be more useful and quicker to be adopted in areas where conventional addressing is worst. There is less resistance towards trying a new system in the places where the current systems are worst._

**4\. A new addressing system like What3Words is very useful if everyone uses it, but otherwise not. How are you breaking this classic chicken and egg conundrum?**

_That’s a fair point, but I think it’s also true to say that it’s also true for a particular community, and that’s how we approach it. We target communities, and get communities using what3words one at a time. A community can be any group of people at all: a social group, users of a particular app, people with a particular hobby, a village, or a country. We need sharers and receivers, and importantly the community leaders and influencers to advocate the use of what3words to those sharers and receivers – that’s a full ecosystem right there. We build ecosystem by ecosystem, then the users from one ecosystem find they can use what3words in another ecosystem, and ultimately the assumption is that what3words will be supported by default. That’s our path to global adoption._

**5\. How do you see w3w interplaying with the open geo movement generally or OpenStreetMap specifically?**

_By viewing both as ecosystems like the ones referred to above. Whilst the geo communities are much more au fait with co-ordinates than the everyday consumer, there are plenty of projects within these communities which do involve consumers who will likely be resistant to using co-ordinates. Because what3words is fully compatible with co-ordinate systems, it makes sense for what3words to be another layer in these kind of projects and interfaces, so that the back-end code is unaffected, but there is a simple human-friendly interface which will enable them to get more users interacting with their service. If projects are using addresses instead of co-ordinates, what3words can remove the ambiguity or inaccuracy of the address lookups as what3words is entirely based around co-ordinates with no lookups and universal coverage. A lot of people ask whether what3words can work offline – it can. The entire grid of 57 trillion 3 word sequences is populated by an algorithm, so it’s only the algorithm (a tiny file of just a few megabytes) which needs to be stored. This means that what3words can work on users’ handsets without a data connection, or on a local server for organisations who prefer to host all their tech locally. The fact that what3words is compact, flexible, and can work without a data connection makes it a good natural fit for a lot of the geo projects out there._

Many thanks Chris. For those that are interested, here’s a [video of a keynote speech](http://geospatialstream.com/geco-in-the-rockies-keynote/) Chris recently gave at the [GeCo in the Rockies 2014](http://www.gecointherockies.org/) conference, where he goes into much more detail on the thinking that lead to the creation of what3words. 

I leave you with the following food for thought:

![](/images/tumblr_inline_nd0qabz1yg1siukvl.png)

You can see [all the Open Geo interviews here](http://blog.opencagedata.com/tagged/interview). If you are or know of someone we should interview, please get in touch, we’re [always looking to promote people doing interesting things with open geo data](http://blog.opencagedata.com/post/98139732993/call-for-open-geo-openstreetmap-interviewees).