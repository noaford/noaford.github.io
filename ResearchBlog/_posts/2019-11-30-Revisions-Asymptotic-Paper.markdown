---
layout: post
title: "Revisions on Asymptotic Biofilm Model Paper"
date: 2019-11-30
categories: Research
---

I submitted my paper on a new asymptotic model for biofilm growth to the Bulletin of Mathematical Biology, the official journal of the Society for Mathematical Biology. An editor told me a few changes that he would like to see along with some reviewers' comments. The comments were quite positive. One reviewer even said that my paper is an important contribution to multi-scale modeling which helps answer questions about length scale that are only recently being addressed. I was very happy that the reviewers both understood what I was trying to accomplish and recognized the value in it.

One issue that the reviewers did want me to address is the question of computational complexity. They would like to know just how much faster my model runs than current models. Even with high-performance algorithms in the traditional method, my model still runs at least 100 times faster, and the difference is even larger for more refined grids. Below are graphs of the run time for the asymptotic 2D and 3D model. We compare these run times to the full 2D model, but cannot compare to a 3D model since we do not have one implemented.

![2DTime]({{"/assets/CompTimeCompare.pdf" | absolute_url}})

![3DTime]({{"/assets/CompTime3D.pdf" | absolute_url}})
