---
layout: post
title: "Python Version of Electical Signaling Paper"
date: 2019-12-06
categories: Research
---

I have wanted to revisit the model from my 2021 paper "A Two-Dimensional Model of Potassium Signaling and Oscillatory Growth in a Biofilm", but I don't have access to Matlab. I decided to convert the model to Python, which allows me to run the model, and might be easier for others to run as well.

The Python code can be found in the [GitHub Repo](https://github.com/noaford/Electrical-Potential-Biofilm).

Looking back on this paper, I think the main contribution is the paper's proposal that these cells require some spin up time in their nutrient consumption. They do not consume right away when the nutrient arrives in higher quantity, but take a bit of time to start growing again.

This delay allows the biofilm to create oscillations, which may not occur if the biofilm acclimates instantaneously to its environment. Instantaneous acclimation, I believe, would more likely lead to a non-oscillatory steady state.

![Potassium]({{"/assets/Potassium-12-29-24.jpg" | absolute_url}})
![Voltage]({{"/assets/Voltage-12-29-24.jpg" | absolute_url}})