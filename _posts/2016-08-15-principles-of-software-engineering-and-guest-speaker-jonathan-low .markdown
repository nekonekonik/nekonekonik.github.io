---
layout: post
comments: true
title:  "Principles of Software Engineering & Guest Speaker Jonathan Low"
date:   2016-08-15 09:26:00 +0800
categories: CS3216
---

Today, we had a review on Principles of Software Engineering conducted by Prof. Ben Leong, as well as a guest speaker, Jonathan Low, co-founder of [honestbee](https://honestbee.sg). It was a timely revision of software engineering concepts for me after being away from school for a year. Concepts like modularity, abstraction, and designing for change is often rooted at the core of my software engineering projects, yet sometimes it becomes something like second nature and I tend to forget the proper terminologies (that's not good for technical interviews! :()

Besides the theoreticals, I found the practical software engineering advice given by Prof Ben / Jonathan to be especially relevant given that I've seen how tech companies benefited / suffered by following / not following these good practices: 

**1) Always have a staging environment for testing before pushing to production:**  
A company that I knew of, which I won't disclose, had an issue of with server space due to fast growing customer data and large amount of legacy content. Pressured by the lack of company budget to acquire new servers and under misguided technical leadership, no server space was allocated for the staging environment and code from development were deployed straight into the production environment after testing. Unsurprisingly, there were often P1s whenever a new production version was deployed. Despite the testing done in the development environment, what the engineering team failed to account was that the configuration between development and production was different, and the staging environment was meant to mitigate this by mimicking the behaviour of the new code under production environment. What resulted was often lot of firefighting (huge wasted manpower on that!), delayed project completion and bad user experience. 

**2) Plan schema before coding and don't over-normalize database tables (+plan your features properly before implementing):**  
This is from a personal experience of mine. Under a project team that I was in, a backend engineer would often plan his schema according to the mock-ups given to him and do a good job normalizing his database tables. Unfortunately, unbeknownst to him, the product manager was not even sure of what he wanted in the feature and kept scope creeping. When the feature was finally done, the backend engineer had redid his schema about 3-4 times (seriously!) and the development schedule was delayed by 1-2 weeks because of bad scope creeps. On retrospect, even though it was not the engineer's fault that the schema had to keep changing, he would not have to redo his database that many times if he did not over-normalize his database tables :P 

**3) Adopt agile development, do iterations of development and product validation:**  
Personally, I feel that the people who came up with the agile methodology are geniuses. It is very satisfying to have a working MVP (minimum viable product) from the beginning of development following the agile methodology, so that developers will not have to feel demoralized thinking that the product is incomplete until the integration of the product happens at the end when using a waterfall model. The iterations of development and product validation are confirmation that the right product is being built so engineers would minimise their time spent building on the wrong stuff (which sadly, can happen quite often due to poorly documented specs).

Other than that, Jonathan also briefly mentioned about how designers can better contribute to the team by not only coming up with mock-ups for main features of the product, but by thinking about the in-betweens of different phases (e.g. such as empty state, one item in the display, too many items in the display). I came across this useful article that talks about the different states of a design that UI teams often neglect and I usually use it as a reference when designing mock-ups. I hope to share the article, [The Nine States of Design](https://medium.com/swlh/the-nine-states-of-design-5bfe9b3d6d85#.9iuf6wex7), with my readers and I hope you will find it useful too :D

