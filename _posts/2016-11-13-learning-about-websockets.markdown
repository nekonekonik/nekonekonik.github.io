---
layout: post
comments: true
title:  "Learning About WebSockets"
date:   2016-11-13 03:26:00 +0800
categories: CS3216
---

This post will be about websockets since my Final Project was on developing an anonymous chat app and using WebSockets is more suitable for real-time applications over other network protocols like HTTP or HTTPS. 

HTTP and HTTPS is built on a one-sided paradigm that the client's job is to request data from the server and the server's role is fulfil the request. This becomes a problem when trying to develop real-time application that requires the server to push data to the client as there is no way for the server to contact the client without a client request to allow a server response. Instead, the client will have to implement a long polling to the web server so that the server can provide a response whenever it has data. Yet, this is a waste of resources as the client has to generate many network requests in preparation for a response.

Here comes in WebSocket, a bidirectional, message-oriented streaming of data between client and server. It allows the server to push data to the client as long as the socket connection between the client and server is open (which doesn't work for HTTP and HTTPS since the socket connection is closed after the client receives data from the server). This is useful in terms of developing a chat application as there needs to be real-time updates for messages from other users and this requires the server to push new messages to the clients.

The advantage of using WebSockets is that the browser abstracts the complexity behind implementing raw socket connections. To further simplify the complexity behind implementing sockets, my team decided to use Socket.io, a NodeJs Socket library that handles cross-browser fallbacks for WebSockets.

As a customary habit of mine, I was only motivated to learn more about WebSockets after trouble has occured >< In the midst of developing for our Final Project, my team faced a big problem in our iOS app where it was unable to connect to the web socket even though it had worked previously. It turns out that after our server was upgraded to HTTPS, we could no longer connect using HTTP nor HTTPS for iOS e.g. `var socket = io('http://{url}')` or `var socket = io('https://{url}')`, and were required to use the WSS protocol instead `var socket = io('wss://{url}')`. Interestingly, Android did not catch our error of using the wrong protocol for setting up WebSocket connection. This was a good lesson learnt about handling WebSockets.