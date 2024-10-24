---
title: "Testing in Golang - An Introduction"
slug: testing-in-golang-01
description: An introduction to my approach of testing a Golang application.
date: 2024-10-23T21:13:36-04:00
image: cover.jpg
math: 
license:
hidden: false
comments: true
draft: true
categories: [Testing in Golang]
tags: [go, golang, testing, unit-test, integration-test, performance-test]
---
I've been thinking of writing this series of articles for a while now, without ever fully committing. This being my first written post ever written ([Hello, World!]({{< ref "/post/hello-world" >}}) really doesn't count), it took me some time to get over the hurdle of feeling enough confidence to put my thoughts out there on the www.

A whole year, yikes!

This will be a series of posts, I'm not too sure how long yet, where I will go over my thoughts on how to approach testing in Golang. This is meant both to inform, and to allow me to put my jumbled thoughts on the concept into the written word to hopefully clear up my own understanding of testing.

In my experience writing code nowadays, around half of what I write relates to testing. I've had the chance of working on some greenfield projects with top of the line tests written by Go veterans, but part of my current work involves developing against a monolithic app initially started back in... 2016? The original devs were not necessarily experts, and a lot of the standards we are used to nowadays weren't established back then. So it's understandable that the 

One of the greatest challenges we face in testing that legacy codebase is that the code was not initially written with dependency injection in mind, making it very hard to create unit tests that don't need a bunch of setup for dependencies. In a way, we end up with very little unit tests and mostly some freaky unit-integration test hybrid that takes a while to run and is horrible to write and to maintain.

> Cover Photo by <a href="https://unsplash.com/@nci?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">National Cancer Institute</a> on <a href="https://unsplash.com/photos/man-reading-papers-in-front-of-computer-pCqzMe04s8g?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a>
   