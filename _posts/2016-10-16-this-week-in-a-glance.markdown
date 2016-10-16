---
layout: post
comments: true
title:  "This week in a glance"
date:   2016-10-16 00:26:00 +0800
categories: CS3216
---

This week wasn't as satisfactory as I would have hoped. The use of NativeScript was favoured over the use of Ionic 2 because it had been in the market longer than Ionic 2, which is currently in the alpha stage. After days of picking up NativeScript and dutifully implementing the UI for our native views, it was an oversight on our part in not checking whether the most crucial library we needed (Socket.io) is working in NativeScript first.  

(Although on a side note, Socket.io does work well with Angular 2 web framework and there are sufficient tutorials online.)  

It wasn't until midweek when we discovered that it was incredibly difficult to integrate Socket.io into NativesScript to work for both iOS and Android. (Just to prove my point, Larry and I had worked from 6pm to 2am on Thursday just trying to get it to work T.T ). The two Socket.io wrapper libraries for NativeScript that are easily found through Googling may seem promising but they don't work and their demos break. Sadly, we only tested them when we were at our wits end to realize that they are not functioning.  

Moving on from our unfortunate state, we have decided to return to one of our initial plans, which is to use React Web and React Native. With React Native being more mature than NativeScript, there is more community support for integrating Socket.io and it is quite unlikely that we would face another crisis from now on (I really hope so :x).  


**Will I still want to use NativeScript in the future?**  

With my one of week of dabbling with NativeScript, I would say that the experience is not the most pleasant. Here are a few of my grievances:  

- It expects you to be on the latest Xcode version, which is sadly not the best idea when you are being forced to upgrade your MacOS to a newer and buggier version which you are stuck with until further updates are available to make the new OS more stable.

- It does not recompile code after a few successful builds. As we are using Typescript with Angular 2 on NativeScript, what happens is that during the build, it will convert TypeScript to JavaScript before using them. Like a child playing a truant, it fails to compile the updated code after a few successful builds and you will be left scratching your head on why your code doesn't work. To hoax it back into recompiling files, you will have to delete a compiled file before it notices it has to recompile the code. Talk about wasting time looking at failed builds and trying to debug the framework instead of working on your code. 

- The build speed is much slower on mine than on other people's Mac :(

**Considering that Ionic 2 has just made its appearance, I would prefer to wait for its stable release than to use NativeScript if I had to use Angular 2 to develop native apps.**

