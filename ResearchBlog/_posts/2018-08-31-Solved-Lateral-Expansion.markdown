---
layout: post
title: "Fixed Lateral Expansion of Biofilm"
date: 2018-08-22
categories: Research
---

Last post I talked about the problem I was having with boundary pinning during biofilm expansion. I was trying to model a biofilm that was supposed to expand outward. However, the boundary would not move when the biofilm height was barely positive. The derivative of the biofilm shape near the boundary couldn't compensate for this minuscule height.

My solution is to no longer calculate growth on a boundary grid point. Instead I extrapolate from the growth of one node in. This interior node has a better approximation of growth and will not get pinned like the boundary node.

I ran a preliminary test comparing this new model with a full two-dimensional simulation. Both simulations start with biofilm as a semi-circle centered at .2mm with radius of .1mm. The top image show the functional representation model initially and after growing for one day. The second image just shows the biofilm interface of the full two-dimensional model after one day. The functional representation model poorly predicts growth on the leading edge of the biofilm, but it agrees well with the growth on the trailing edge, which is where the assumptions of the model are satisfied. This is as good as we could hope for!

![FunctionalModel]({{"/assets/GrowingBiofilm.jpg" | absolute_url}})
![2DModel]({{"/assets/GrowingBiofilmFull.jpg" | absolute_url}})
