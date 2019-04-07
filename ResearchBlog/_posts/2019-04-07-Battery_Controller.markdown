---
layout: post
title: "Optimizing Control of a Storage Battery"
date: 2019-04-07
categories: Research
---

This past quarter I took a class on energy and technology entrepreneurship. We worked in teams to create a mock startup. We developed an idea for a product and then assessed the market by talking to potential suppliers and customers and by creating financial projections. For the mock startup, I created a battery controller that used predicted prices and energy usage to store and deploy energy.

The program works by predicting energy and usage for the next 24 hour period, and then choosing an optimal battery deployment for that period. The controller will adjust its battery deployment using the actual energy usage, but doesn’t redo the optimization during the 24 hour period. If I had more time, I would have the battery continually re-optimize. I predicted the energy prices and usage using ARIMA modeling, which ended up being pretty good predictors. 

The following are images of predicted prices, usage, and battery deployment. You can find the code at https://github.com/noaford/BatteryController .

![PricePred]({{"/assets/pricepred.png" | absolute_url}})
![UsagePred]({{"/assets/UsagePred.png" | absolute_url}})
![BatteryControl]({{"/assets/BatteryControl.png" | absolute_url}})