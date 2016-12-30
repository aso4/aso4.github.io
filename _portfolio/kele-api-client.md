---
layout: post
title: Kele API Client
feature-img: "img/sample_feature_img.png"
thumbnail-path: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Kele_Okereke_Cropped.jpg/220px-Kele_Okereke_Cropped.jpg"
short-description: A command line API client to access information and functionality in the Bloc.io API

---

## Summary

APIs are vital in modern web development, whether developed by a giant web presence such as Amazon or Google or internally, for use by other developers within a company's internal network of developers. Web APIs often offer complex functionality that would otherwise be difficult or excessively time-consuming for developers in a company to build on their own.

## Explanation

In this case, I was tasked with developing a client that accessed information and functionality within Bloc's API to perform tasks as if I were accessing the site from a browser. Tasks include initializing and authorizing users with a correct user email and password, retrieving user information, retrieving mentor schedule availability dates, retrieving student curriculum checkpoints and roadmaps, creating new message threads as well as responding to existing message threads, and submitting and updating of checkpoint assignments. This project marks the first API returning JSON objects that I've worked with.

## Problems and Solutions

At the beginning, acclimatizing myself to the syntax to the API calls and parsing through the data that was being returned was the biggest challenge. After this, I ran into a few problems with setting up the testing environment, particularly with the VCR gem and security gem.

After looking through API documentation and running through a number of different combinations of API calls in the Rails console, I was able to grasp the Bloc API syntax and make progress with the user stories. Testing using the VCR and figaro gem proved to be a bigger issue, as ENV variables were not being registered in RSpec or the console. After some googling for solutions, I consulted my mentor who suggested that I go with Webmock instead, which proved to be a handy solution.

Adding VCR to my test suite proved to be more difficult of a task. After reading through documentation and a few examples on stackoverflow, I was able to successfully use a "tape" for my initial test call to the API. Being that VCR "records" API responses to calls and "plays" the responses back after a given test is run, my expectation going in to the tests were that only a single, large, recorded response was necessary for multiple calls to the API. This proved to be a conceptual error, as multiple recordings were needed for multiple types of calls to the API.

## Conclusion

This project helped expand my knowledge of APIs and gem integrations in a few ways. It gave me an understanding of JSON objects, parsing the results, and the further use of those results to perform further functions with the API. It also helped me get a better grasp of how documentation is written differently, and where and why further research might be necessary. It also helped build a better understanding of the process that developers go through when trying to implement new tools or add new features to their project.
