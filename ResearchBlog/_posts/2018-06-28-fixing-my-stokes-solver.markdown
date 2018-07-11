---
layout: post
title:  "Fixing My Stokes Solver"
date:   2018-06-28
categories: Research
---

A year ago, I wrote a Stokes-flow solver that runs on a GPU. It worked great for a whole year and then it recently broke after a software update to OpenCL. It started inputing NaNs into certain coordinates that propogated from a few points and filled the whole grid. I had to go back and look where the code was accessing this (non)data. Sure enough, the right side of each local grid was accessing local memory that had not been allocated. I guess before the update the GPU didn't use the NaNs that were already in memory from previous runs. Maybe it did though and it wasn't a problem because the local memory never contained NaNs.

Well now it works! The included image is of flow around a semicircle, particularly the x-directional velocity. It now runs super fast (flow for a 200 by 200 grid solved in a minute or less), maybe even faster than I remember it running. I can now finish running some tests I need for a manuscript I'm writing. I'm doing an even faster model for flow through a biofilm!

![fluidU]({{"../assets/fluidUplot.jpg" | absolute_url}})



<!--- {% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %} --->
