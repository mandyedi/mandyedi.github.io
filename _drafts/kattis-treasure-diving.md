---
layout: post
title:  "Kattis - Treasure Diving"
date:   2020-07-15 13:36:00
categories: challenge
tags: [challenge, kattis, tsp]
---

During the time of my job seeking I came across a really cood coding challenge. The company used the Kattis coding competition website for testing my coding competency. I was given three challange from easy to hard and I had to solve them in 48 hours. Unfortunetely I had time to solve only the first and second challenge. Because I really like coding challenges and always find for opportunites to improve myself I solved the problem.

At time of the writing this post the company is responded to me and found me eliglible to continue with the hiring process. :)

The Kattis problem is called [Treasure Diving][treasure-diving]{:target="_blank_"} and can be described brieflt as follows:
You are given an underwater network of caves that can be cyclic. Every tunel has a specific amount of air need to travel through. You are also given a determined amount of air that you van use for travelling through the network. Some of the caves have idols inside them and your goal is to collect as many idol as possible and come back to the starting point without losing all of your air.

Rewrite
1. found test cases
2. viusalized one of it
3. a-star?
4. not a start to destination problem, rather a tsp
5. greedy? simplifying the test case this might work

0.
My first thought was a greedy algorithm but this challenge is must be more compicated so I didn't even bother to implement one. After it, I did a little research on the internet and found more test cases that I can use in my [coding challenge engine][coding-challenge-engine]{:target="_blank_"}. As I assumed, most of the test cases would have a really high running time with a greedy algorithm.

1.


[treasure-diving]: https://open.kattis.com/problems/treasurediving
[coding-challenge-engine]: https://github.com/mandyedi/coding-challenge-engine