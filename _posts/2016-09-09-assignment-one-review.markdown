---
layout: post
comments: true
title:  "Connectr - Assignment 1 Afterthoughts"
date:   2016-09-09 09:26:00 +0800
categories: CS3216
---

This week marks the week after the concurrent deadlines of Assignment 1 and 2. As I have not properly introduced my 
team's project, [Connectr](https://connectr.tk/), I think this is the best chance to review about it right when the end is still fresh in my mind. On the surface, Connectr is a travel-related application for you to discover where your friends have travelled to so you can consult them for advice on the places that you are interested in visiting. This app is inspired by [5 Ways To See Your Facebook Friends On A World Map](http://www.makeuseof.com/tag/5-ways-facebook-friends-world-map/) where the (mostly broken) apps allows you to view where your friends are on a world map. I find these apps a bit stalkerish by making public information more easily accessible at the convenience of a click (and possibly sacrificing you and your friends' Facebook information), so why not make it more exciting by bringing the stalking up another level by retrieving the places your friends have checked into before :D Hence, on a deeper level, Connectr was made to visualize how much personal information we are feeding Facebook through the places we checked-in to and at the same time we can have some fun peeping at the places our friends have been to.


![Landing Page](/images/connectr/landing.png)
*This is Connectr's landing page, it has the facade of an innocent looking travel application. :P*

![Main Page](/images/connectr/main.png)
*This is the main view that a logged in user would see. They would see the list of friends who have an account with Connectr and they can toggle on/off the data points of their friends on the map by clicking on the visibility icon on their friend.*

![Heat Map of Singapore](/images/connectr/singapore.png)
*A heat map showing the people who checked into Singapore!*

![Final Facebook Button](/images/connectr/individual.png)
*Heat map showing an individual's check-ins around the world. What an exciting way to stalk your friends!*

Through the process of developing Connectr, I am amazed at the type of information Facebook has of us, and how often users unwittiingly give up information of themselves. For me, I saw Facebook check-ins or location-based posts as a innocent and fun feature to inform your friends where you have been just in case something happens. Yet, as a collection of data points, Connectr has shown that we can collect more information about someone from the places they often visit, their travel / food lifestyle etc. As much as I am fine with Facebook having my data (I am a social media slave :( ) , this process led me to be more wary of how external apps may be using our data. For one, I never use apps/ friends similarity quizzes that attempts to have all my data just to compare with my friends'.

I had a lot of fun developing Connectr and I have my awesome teammates to thank for. As mentioned on my [first post](https://nekonekonik.github.io/cs3216/2016/08/02/what-i-hope-to-learn-in-cs3216.html), I tend to be lenient on myself and not push myself to my limits. However, while I was working under Jiang Sheng as the Product Manager, I saw how nothing less than the market standards should be delivered, even if it was for school project. 

For Connectr, I had implemented the Facebook in three times. The first time I implemented it, I used the documentation under [Facebook Login for the Web with the JavaScript SDK](https://developers.facebook.com/docs/facebook-login/web), which didn't fit well for our app because we were using AngularJS as a front-end framework. I ended up trying to find the easy way out by using external login libraries such as [Satellizer](https://github.com/sahat/satellizer), of which I later found out that it was giving its small set of problems by adding unnecessary headers to http requests. Even though we could made do with Satellizer, I was made to redo the Facebook login and this time round I managed to find a [Facebook Login documentation meant for Angular apps](https://blog.brunoscopelliti.com/facebook-authentication-in-your-angularjs-web-app/). As much as the third implementation was smoother than the first two, the Facebook Login button that came with the official plugin had lag time before it gets rendered and it affects the user experience negatively even though it was the official login button (thumbs down to Facebook >:( ). The final Facebook login that you see is a walkaround to the ugly and slow Facebook login button by replacing the official login button totally and it is thanks to Jiang Sheng and his high expectations ;). 

![Selection of Individual Checkins](/images/connectr/facebookbtn.png)  

I also benefitted from working beside the UI prodigy Jinghan and trying to gain some UI skills / techniques through diffusion. The styles in the map view are selected by him :D

<img src="/images/connectr/nicholette-logo.png" width="140">
*The logo I created for Connectr.*

<img src="/images/connectr/jinghan-logo.png" width="140">
*The logo that Jinghan created for Connectr.*

The differences between me and Jinghan's design skills. I've still got much to learn...

Overall, it had been a very fruitful experience for me working with my team for Connectr. 10/10 would do it again if I had to. :D