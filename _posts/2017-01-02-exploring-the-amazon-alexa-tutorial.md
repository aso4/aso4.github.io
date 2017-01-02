---
layout: post
title: Exploring the Amazon Alexa Tutorial
---

> Publish a blog post about your experience with the Alexa Trivia Skill sample and share it with your mentor. Write about what you found interesting, challenging, and questions you have about Alexa in general.

The Bloc.io Amazon Alexa project gave me my first glimpse into the world of AWS. Amazon's setup process to becoming a developer and using amazing technology such as Alexa first involves signing up at two different portals: Amazon's developer portal and the AWS portal.

The first issues I ran into during this project was the tutorial. [The link](https://developer.amazon.com/appsandservices/community/post/TxDJWS16KUPVKO/New-Alexa-Skills-Kit-Template-Build-a-Trivia-Skill-in-under-an-Hour) I was provided with was several months old, which in terms of Alexa's release date is similar to a beta release. There were new menus and submenus to navigate during the setup of the new skill with new pieces of information that could be inputted that seemed important.

After finding a [more recent tutorial](https://github.com/alexa/skill-sample-nodejs-city-guide), I proceeded through the setup stage and began exploring how testing worked with Alexa. Lacking an Amazon voice-enabled device, I browsed the developer console and echosim.io - two links provided in the new tutorial. In the Alexa framework, each app has a "skill". The template provided in the city guide tutorial has several of them, integrating the New York Times to get local news and weather information, providing an overview of the given location, a top five list of local attractions, and a small selection of other attractions as well as the default Alexa skills of "Stop" "Repeat" "Yes" and "No".

My API key to the New York Times proved to be working, as "get local news" worked from the outset. "Get top five attractions" was also working. What seemed to not be working was the "location overview" skill: Alexa would randomly return one of the other local attractions instead of giving me more information about my city. Going to the developer console and manually typing in commands also proved to be tricky, as simple or even errant commands were also being interpreted as asking for other local attractions. Eventually, I began looking for more exact commands to ensure my queries to Alexa were bulletproof, and browsed over to the SampleUtterances.txt file and began typing those in verbatim. I found that hitting the "Reset" button in the developer console solved my problem.

Quick hits: Better go through a Node.js tutorial or two so I can get a better understanding of how Skills work. I'm curious as to what kind of algorithm Amazon is using for natural speech recognition, and what ways it can be tweaked.
