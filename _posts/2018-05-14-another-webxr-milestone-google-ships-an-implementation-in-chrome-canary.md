---
title: 'Another WebXR Milestone:  Google Ships an Implementation in Chrome Canary '
date: 2018-05-14 14:43:50 -04:00
permalink: 2018/05/14/-canary-webxr
categories:
- webxr
tags:
- chrome
- canery
- webxr
author: blair
layout: post
---

It's exciting to see us cross another threshold on the way to pervasive Web-based AR/VR:  last week at Google IO, Google [released an experimental version of WebXR in Chrome](https://developers.google.com/web/updates/2018/05/welcome-to-immersive).

For me, this has been a long time coming. My research group at Georgia Tech started working on web-based AR browsers when we started the [Argon Project](http://argon.gatech.edu) back in 2009, and we're now on the fourth version of the browser on iOS and Android (including having a pretty nice [open source AR framework called argon.js](https://argonjs.io)). WebVR started more than three years ago, with implementations available now in most major browsers. Last year, Trevor Smith and I [proposed some initial ideas for a WebXR API](https://github.com/mozilla/webxr-api)  that supported both AR and VR, and implemented it in an [experimental web framework](https://mozilla/webxr-polyfill) and browser for iOS (the [WebXR Viewer](https://itunes.apple.com/us/app/webxr-viewer/id1295998056?mt=8)) that we and others are using to do Web-based AR experiements, and explore ideas for future capabilities for WebXR.

{% marginnote "webxr" "The differences between the version of WebXR we proposed last year and the WebXR Device API are small, so updating will be easy.  But, I don't want to break experiments people are doing with the WebXR Viewer multiple times, so I've been waiting for the API to be more settled before making the jump."%}If you use VR on desktop or Android, and want to experiment with the evolving WebXR API, check out Chrome Canary and give it a try! They'll be releasing Android AR support in Canary soon, too.  I've been waiting until the WebXR Device API is a bit more settled before updating the WebXR API we use in the WebXR Viewer to match it, but I'm looking forward to us and other companies in the [Immersive Web Community Group](https://github.com/immersive-web) shipping WebXR in other browsers.

WebXR is coming! 
