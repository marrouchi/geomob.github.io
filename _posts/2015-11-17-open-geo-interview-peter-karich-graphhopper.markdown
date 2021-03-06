--- 
layout: post
title: "Open Geo interview - Peter Karich, GraphHopper"
date: 2015-11-17 00:23:10 +0000
tags: interview graphhopper timetabling
---
Today’s installment in our ongoing interview series is with [Peter Karich](https://twitter.com/timetabling), one of the people behind [GraphHopper](https://graphhopper.com/), a popular routing service based on OpenStreetMap data.

Here’s a screenshot of GraphHopper in action calculating a walking route on the OpenStreetMap homepage.

![image](/images/tumblr_inline_nxxkmxYyDi1siukvl_540.png)

**1\. Who are you and what do you do? What got you into OpenStreetMap?**

_I’m Peter Karich, once a physicist and for the last few years a software developer - fighting against the bits and bytes mostly in Java and JavaScript these days. In 2011 I somehow discovered OSM, I cannot remember exactly how, but I found the open geo data fascinating from the beginning. I played with the street network data just for fun and found it disturbing that there was no simple to use and memory efficient software that can run on my resource restricted laptop to run some algorithms on them. Not even “Germany-only” was possible. From this GraphHopper grew into a real and healthy open source project and some customers asked me to improve it and get paid, so I went full time with it in 2014._

**2\. What is GraphHopper? What got you into routing? What’s the story behind the service?**  

_The GraphHopper routing engine is an active open source project written in Java under the Apache License 2.0 with a growing community that does exactly one thing: routing. It does not do the visualization, the geocoding, nor route optimization which all require completely different algorithms and even communities. Still we have a relative popular demo called [GraphHopper Maps](https://graphhopper.com/maps/) which combines geocoding, visualization and routing._

_When I decided to go full time with GraphHopper I knew doing consulting will always be important but that I need to create a product on-top of the open source software somehow, which I can then sell to ensure that the open source project prospers and is healthy and will always be so in the future. One big problem is to find a way to make money without reducing the value of your open source project!_

_And [together with Stefan the author of jsprit](https://graphhopper.com/blog/2015/09/04/graphhopper-and-jsprit-join-forces/), we’ve found a way for that with the GraphHopper Directions API - our commercial offering for routing services. The Directions API currently contains APIs for routing, route optimization and geocoding and is easy to use and cost effective for app developers to big companies. We already provide a free usage quota for many open source projects like [openstreetmap.org](http://www.openstreetmap.org) itself and e.g. Gnome Maps._

**3\. Routing seems to be a very hot topic, both in general and in the OSM community. There are several different efforts underway. Give us an overview of the space and the pros and cons of the different approaches.**

_Yes, I once counted over 10 active open source routing projects :) ! [Have a look](http://wiki.openstreetmap.org/wiki/Routing)._

_There is one category of projects which is not usable in commercial projects as they are licensed under the (A)GPL and there are other projects with more permissive licenses. We still think that GraphHopper with the Apache License 2.0 is the best choice for companies, without the need for attributing and with certain guarantees we give our users and the only project where you can get consulting ;)_

_The other big advantage over existing open source routing projects with more permissive licenses is not so easy to explain. But let me try._

_A first working solution for routing on OSM is implemented relative easy: just use an algorithm called “Dijkstra” and import the OSM data somehow and you are done. But if you want an easy to use mechanism which works for a planet import AND is fast, then you already need a lot more engineering. Once you got there you can add heuristics or expensive pre-processing to the stack to further make routing faster, but the problem will always be to decide between routing speed, routing optimality (heuristics) and flexibility. And GraphHopper is the only open source solution where you have a choice:  
* you can go with the so called “flexibility mode”, where you can change preferences per request (e.g. turn off sand surfaces for bike routes),  
* you can mix-in heuristics to make all a bit faster or  
* completely switch to the so called “speed mode” (the default one) where you pre-process the data to decrease the routing response times dramatically._

_Furthermore you can request a long distance route via the “speed mode” and other requests via the “flexibility mode” all with the same GraphHopper installation, even multiple profiles are now possible in both modes with the latest version 0.5.0 released in August. You won’t find all this flexibility and production quality resulting from a very big test suite anywhere else._

_And all that you get in the (relative) high level programming language Java and GraphHopper is easy to use: be it as a ready to use routing service or a customizable routing engine which you integrate directly in your JVM-based project._

_BTW: It is even possible to run [GraphHopper on iOS](https://github.com/graphhopper/graphhopper-ios) and runs natively in Android like used from [Pocket Maps or Locus](https://github.com/graphhopper/graphhopper/blob/master/docs/android/index.md#apps)._

A screenshot of GraphHopper in action, taken from the GraphHopper [blog post explaining how they address the infamous traveling salesman problem](https://graphhopper.com/blog/2015/11/09/how-does-graphhopper-send-out-traveling-salesmen/). 

![](/images/tumblr_inline_nxydtwzYZv1siukvl_540.png)

**4\. GraphHopper is opensource software. What is the best way for developers to get involved?**

_See the documentation about our open source software on github, [here](https://github.com/graphhopper/graphhopper/) and [here.](https://github.com/graphhopper/map-matching/) We have [a forum where you can ask us everything](https://discuss.graphhopper.com/). if you are interested in UI, data structures, OSM or algorithms, there will be a task for you :) Also you can read through some news [on our blog](https://graphhopper.com/blog/)._  

**5\. What steps could the global OpenStreetMap community take to help support the use of OSM in routing?**  

_There are many aspects. From our customers we often hear that “address-precise” geocoding is important for them, which is not really the routing but would help us offering more precise routing :) ! We now contribute a weekly update process of the world wide OSM data for the geocoding software photon to make mapping addresses more fun and sense :)_

_Furthermore we think truck restrictions is another interesting aspect and we’ll incrementally improve there, based on [our existing truck profiles](https://github.com/graphhopper/directions-api/blob/master/supported-vehicle-profiles.md) taking already into account width, height and weight limits._

**6\. You have a large and diverse customer base, from established brands to start-ups. What sort of feedback do you get from them about OpenStreetMap data?**

_Customers pay you only if they benefit from your product and their money is their “thanks” which we really like, of course :). But this also means that we do not hear much regarding OSM, which in my opinion still speaks many positive words for OSM although not explicitly. BTW: the same is true for GraphHopper, many people just use it and ask us only if they have problems :)_

_Still from time to time customers ask how we ensure the quality of OSM, which is still an open problem for us. But as we update our data nearly daily (geocoding weekly), we can convince them of all positive aspects. And especially from companies with a product for the “Outdoors” we hear from time to time: “OpenStreetMap is the future here”_

_Also sometimes they ask us to remove the GraphHopper attribution but customers mostly do not have a problem that they always need to attribute OSM. So I do not think that the license itself is a problem, still this can be improved and clarified. For example what about mixing OSM data with traffic data? If you combine the data on the fly this is not a problem but if you pre-calculate the weights like you can do with GraphHopper its “speed mode” one could potentially talk about a mix of data and that the results would need to be released under the ODbL, which often would not be okay for the data owner. And for OSM the data would not make sense as it does not fit there IMO._

**7\. Last year OSM celebrated its 10th birthday, where do you think the project will be in 10 years time, both globally and in terms of usage in routing?**

_I think that the project will be used by many parties, be it for routing, outdoors, visualization, governmental tasks etc. Maybe even big map providers will use OSM in specific geographical areas which complement their own data without violating the OSM license._

_And the more bigger companies are involved the more the pressure towards the community will be to find (better) procedures which are acceptable for both parties on how to:  
* map for money  
* create and enforce more restrictive tagging schemes_

_I do not think this is currently “bad” per se, but when a project grows certain structures need to be created to ensure the future growth. If not, a more serious problem could arise: the split of the project, where the more liberal ‘commercial providers’ will try to create a public domain geo database, as is already partly the case with [openaddresses.io](http://openaddresses.io/)._

_Regarding the license: the community and/or the foundation has to prove that they are able to fight for the license and against violations like they certainly happen already, otherwise the license is just words on an internet site and we could move to a more permissive license._  

Thank you Peter, for the detailed interview and your work on GraphHopper. I encourage anyone interested in routing to [follow the project’s blog](https://graphhopper.com/blog/) and [twitter feed](https://twitter.com/graphhopper). It’s a great example of how more and more complex services can be built on OpenStreetMap and OpenData as the underlying data becomes increasingly comprehensive. 

- [Ed](https://twitter.com/freyfogle)

You can see [all the Open Geo interviews here](http://blog.opencagedata.com/tagged/interview). If you are or know of someone we should interview, please get in touch, we’re [always looking to promote people doing interesting things with open geo data](http://blog.opencagedata.com/post/98139732993/call-for-open-geo-openstreetmap-interviewees).