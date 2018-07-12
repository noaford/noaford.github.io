---
layout: post
title: "Fitting Oscillator with Keras"
date: 2018-07-12
categories: Research
---

My advisor, a research collaborator, and I are working on a research proposal this week. I’ll post more about that later. This week I decided to do a minor machine learning project. I took a class in controls using machine learning last quarter and found it pretty cool. I want to look at using more of the packages (TensorFlow, Keras, PyCharm, etc.) since they are well optimized to training. 

In the following [GitHub Repository](https://github.com/noaford/FittingOscillator) I use packages from Keras to fit data generated from a harmonic oscillator, $$x''(t) = -2x'(t)-x(t)+a(t).$$  I first use a recurrent neural network to fit the data since it’s a time series. I realized however, that since I’m training the hidden state of the neural network to be the next predicted state while also feeding in the next state, there are redundancies in the inputs. To get rid of this redundancy, I instead use a linear one-level neural layer (which is just a linear predictor). The training is much faster using the fully connected layer than with the recurrent neural network. 

Recurrent neural networks are currently used heavily for word prediction sequences. In these systems the output (the next word in a sequence) is different from the internal state. Maybe recurrent neural networks make more sense in the context of passing preprocessed states to the next cell versus passing outputs (the next state) into the next cell. In the case of the oscillator, all I want is to pass the next position and the forcing function into the next cell, in which case a vanilla neural layer is what I one should use.

![Oscillator]({{"/assets/Oscillator.jpg" | absolute_url}})
