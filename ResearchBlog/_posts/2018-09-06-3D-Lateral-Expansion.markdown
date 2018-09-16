---
layout: post
title: "3D Lateral Expansion of Biofilm"
date: 2018-09-16
categories: Research
---

I have been working the past two weeks to turn the lateral expansion that algorithm that I talked about in the last past into three-dimensions. I ran into many problems with the linear extrapolation required to extend the biofilm surface to the entire domain. The complicated interface between the region with biofilm and the region with no biofilm often led to algorithm failure in the fast marching method.

However, I was able to solve the problem (as long as spreading of the biofilm is slower than the grid size divided by the time step). Below is a picture of a biofilm that has grown from a small semicircle. You can see preferential growth toward the inlet on the left side of the figure. It's so cool to see a full three-dimensional biofilm simulation that reproduces the growth patterns of a real biofilm. 

![Growing3D]({{"/assets/Growing3D.jpg" | absolute_url}})