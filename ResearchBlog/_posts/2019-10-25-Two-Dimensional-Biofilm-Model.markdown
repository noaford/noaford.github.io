---
layout: post
title: "Potassium Effects in Biofilm Model"
date: 2019-10-25
categories: Research
---

I have been working to create a two-dimensional model for the oscillatory Bacillus Subtilis model. This system exhibits oscillatory growth behavior from potassium signalling. This project has required me to update the equations for the model because the model that I was using couldn't sustain the potassium wave efficiently enough in two dimensions. Often the oscillations would peter out.

The most important change in the model is that cells react and depolarize in response to changes in potassium instead of absolute potassium levels as shown in the figure below. Experiments show a potassium gradient from the middle to the edge of the biofilm, but the voltage change can propagate all the way to the edge of the biofilm. Change in potassium is a better representation of cellular stress since bacteria are able to adjust internal potassium levels to return to their preferred voltage differential over time. This propagation method is much more efficient in terms of transmitting the potassium signal.

I will show more of the effects of this change in following posts!

![PricePred]({{"/assets/PotassiumChangeDepiction" | absolute_url}})
