---
layout: post
title: "On Modeling the Shape of Biofilm"
date: 2018-07-19
categories: Research
---

Biofilm is a community of bacteria that live on a surface or interface. If you’ve ever touched a slimy rock in a river or lake, you have touched a biofilm. They are also on the insides of our water pipes and in our bodies. They are on the vast majority of surfaces that are in constant contact with fluid. 

So what are we trying to model in a biofilm model? Often we want to know how biofilm consume nutrients and how they grow. Most biofilm get their nutrients from the flow of water around them, though sometimes they grow on a nutrient rich surface like an animal’s skin. Their growth direction is often directed toward nutrient sources. They typically grow upstream toward nutrients and in shapes like streamers and mushroom sprouts to maximize their surface area in contact with nutrients. However, these complex shapes carry the risk of mechanical failure, as in a streamer might break off. If the flow is fast around the biofilm, it will most likely grow flat to decrease its risk of detachment.

One part of my research is modeling the shapes that biofilm can take given different environmental conditions. In many scenarios one would think of a biofilm as being flat, in fact one of my projects makes a similar assumption. However, we can study and model all of the micro-scale complexities using something called a continuum model. Instead of looking at each individual cell, we assume that the biofilm is made up of smooth material and each part of the material acts like a cell. It consumes nutrients, releases products, and grows. By looking at the biofilm as an undifferentiated entity, we can use differential equations to solve for particle distributions, growth, and overall shape. 

A down side to the continuum model is that it is difficult to incorporate random effects of different cells. Some cells might happen to be growing faster than others and move in random directions. There are discrete models that can incorporate these effects, but they often have difficulties accurately solving for particle concentrations.

Below is an image of what a simulation might look like. This is taken from a paper by my advisor, David Chopp. You can see that fluid is flowing from right to left around a blob of biofilm. The simulation will then track the consumptions and growth of this collection of bacteria.

![Biofilm]({{"/assets/BiofilmModelDemonstration.png" | absolute_url}})


Duddu, R., Chopp, D., & Moran, B. (2009). A two‐dimensional continuum model of biofilm growth incorporating fluid flow and shear stress based detachment. Biotechnology and Bioengineering, 103(1), 92-104.