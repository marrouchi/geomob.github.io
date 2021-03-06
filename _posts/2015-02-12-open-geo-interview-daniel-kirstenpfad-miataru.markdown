--- 
layout: post
title: "Open Geo interview - Daniel Kirstenpfad - Miataru"
date: 2015-02-12 00:10:42 +0000
tags: bietiekay interview miataru
---
Today we talk with [Daniel Kirstenpfad](https://twitter.com/Bietiekay), creator of [Miataru](http://miataru.com/), an open source location tracking/brokering service. 

**1\. Who are you and what do you do? What got you into OpenStreetMap?**

_My name is Daniel Kirstenpfad and I started the project Miataru. On my daytime job I am working in a global eCommerce company and the spare-time I use to write open source software and do all kinds of things with technology ([also see my blog](http://technology-ninja.com))._

_I got into using OpenStreetMap with the Miataru project since it offered much higher detailed and up-to-date maps than any other data-source available. Being able to render out my own tiles in whatever style with whatever level of detail and points of interests was the definitive answer to my projects needs. About the same time I started contributing to OpenStreetMap to get my surroundings updated and enriched with details._

**2\. What is Miataru? What is your motivation for the project?**

_Miataru is a set of tools that allow it’s users to track and share their location. There is a server implementation as well as implementations for various mobile device platforms. All of the components are available as open source software. The idea behind Miataru is that the user is in full control of the data at all times. The client is in control of the amount of data stored on the server as well as the maximum duration the data is stored. In addition there is no sign-up necessary to use the service - you fire it up, and share your position if you want._

_My motiviation was of course first-and-foremost to solve my own problem of not having a multi-platform location tracker with an open API available to integrate into my home automation. Since all parts of the Miataru service are free-to-use it seems that other people had the same problem and started using it regularly. Some even have their location publicly accessible displayed on their own homepage._

_Everytime I am trying so solve my own problems, I am trying to make those solutions available to other people to either re-use or extend. Those projects I usually publish [on my GitHub page](https://github.com/bietiekay)._

**3\. It seems similar to Yahoo’s Fireeagle and Google’s Latitude in some ways, both of which were eventually closed. Is there a really demand for this type of service? Why do you think those projects failed?**

_I was using Google Latitude for years within the family to track members during gatherings or just because there was a lot of travelling going on. By the time Google announced to close it down I had it already deeply integrated in various home automation use-cases and applications at home and work: The position of members of the family controlled the heating at home (turn off if all leave). Instead of coming up with various meeting points we could just navigate to the position of each other. And of course the constant “where are you now” on the phone was gone completely._

_To keep this convenience in our life I had to find a replacement for Google Latitude. Since there were some offers from other companies I looked into them but never really gained trust in what would happen to the data and how I would be able to retrieve it through APIs to include it into the automation systems. So I came up with the simple sketch of a protocol, server and mobile client application and started watching out for smart people that could help with the implementation of both ends._

_The server implementation was mainly done by the very talented [Manuel Ernst](https://github.com/zaphod1984) and I could concentrate on the iOS client implementation as well as the browser client._

_Of course Google Latitude was indeed shutdown as a stand-alone service. But the functionality, which is quite useful, has been tied into Google+ from that time on. Of course its in the commercial interest of a company to keep gathering as much data as possible. This is why the product Latitude has reached it’s end of life, but the actual tracking of location kept on living within Google+. Unfortunately Google did not provide easy to use APIs to retrieve the user-generated-data. So I think the idea behind this type of service did not fail, the commercial providers just decided to monetize the data in a different way._

**4\. What is the best way to get involved in the project? How can people best help?**

_If you’re interested in the applications and toolset as a user you will find all applications on the miataru.com homepage. If you need help, the best way is to get in contact with us either through the home page or github._

_If you’re interested helping out with development all tools, specifications and source codes are freely available to you. If you need support or have questions, it’s best to use the available tools [on the repository GitHub page](https://github.com/miataru)._

**5\. What is the roadmap for the project going forward?**

_There are many different aspects that can be improved on the Miataru project. One is the way authentication works and how the sign-up process can be made easier for users._

_Another idea is to make Miataru and it’s reporting clients more versatile and have them report into other services as well. Less-known services like [APRS](http://aprs.fi)  that use specialized electronics in vessels to transmit location information. Miataru could act as a location data source to those kind of services for lesser costs to the user as specialized hardware._

**6\. OSM recently celebrated its 10th birthday, where do you think the project will be in 10 years time?**

_With all sorts of new applications and mash-ups built upon OpenStreetMap I think there’s going to be broader and deeper adoption of OpenStreetMap content and content-generation for users that do not even know that it’s OSM that poweres their favorite app or website._

_With the trends of the quantified-self or the Internet of Things you will always have to plot something onto a Map or create a route from A to B with taking all those details into the equation (“Guide me home only on streets that are lighted up”,…). This versatility is where OSM is and will always be unbeatable._

Many thanks Daniel. Great to learn of projects like this that provide the infrastructure behind the scenes to enable others to build real world applications on top of all the open geodata that has been contributed over the years. Good luck and hopeful this post will lead to more developers joining the effort.

- [Ed](https://twitter.com/freyfogle)

You can see [all the Open Geo interviews here](http://blog.opencagedata.com/tagged/interview). If you are or know of someone we should interview, please get in touch, we’re [always looking to promote people doing interesting things with open geo data](http://blog.opencagedata.com/post/98139732993/call-for-open-geo-openstreetmap-interviewees).