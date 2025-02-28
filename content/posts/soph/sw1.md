---
date: 2024-12-19
title: "soph week 12/16 - 12/20"
draft: false
categories: ["blog", "lightbox"]
---

this week was all about lightbox project, where i had lots of issues. 

generally with the lightbox, you use an atmega328p, but i decided to create as small of a lightbox as possible, and ended up using an attiny84

orignally, i was planning to use an attiny25, as the shop doesn't have an attiny85's, but the problem is that despite using lightweight libraries to allow the attiny25 to run the code, it just cannot handle the neopixel, and leads to plenty of errors.

using the attiny84 was just as frustrating, as the microcontroller stopped working randomly many times, setting me back quite a bit of time

in the end, i got a simple temperature sensor to partially work with my lightbox. (the 18b20 temp sensor im using is having connection issues, which leads to the code running half the time) which will be depicting the color of my box. 


![monkey](/img/soph/1/sw1.png)
###### why is this floating...
