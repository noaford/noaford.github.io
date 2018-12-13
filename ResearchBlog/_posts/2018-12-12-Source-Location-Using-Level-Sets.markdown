---
layout: post
title: "Inverse Problem Using Level Sets"
date: 2018-12-12
categories: Research
---

I have been very busy this quarter, and haven't had as much time for research or for personal projects. But I just spent last weekend doing this really cool application for level sets.

The problem: If you can observe how something diffuses over a region and you know the source strength, can you figure out the location of the source? This is called an inverse problem, where you know the output of a differential equation but are trying to solve for the parameters (in this case the parameter is the source location).

I was able to program a gradient descent method to solve for this location. Below is an image that shows the location of the source and the reconstruction of the source. They match quite well with a bit of an error on the bottom left boundary. This boundary is a bit harder to detect because the lower gradient of the diffusion field at this location. All in all it works pretty well though!

![Reconstruction]({{"/assets/Reconstruction.jpg" | absolute_url}})