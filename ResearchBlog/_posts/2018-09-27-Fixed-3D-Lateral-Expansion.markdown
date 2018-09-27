---
layout: post
title: "Fixed 3D Lateral Expansion of Biofilm"
date: 2018-09-27
categories: Research
---

The approximation to lateral growth in the last post was a rough approximation that wasn't as accurate as it could be. The goal is to linearly extrapolate the biofilm surface into regions with no biofilm (the biofilm height values in these regions will be negative).

The first problem with my method was that I was using a directional derivative instead of the gradient as the slope for extrapolation. A gradient should be used because the gradient is normal to the isocontours of the biofilm surface, and we are tracking how far the other grid point is from the isocontour.

The second problem was with how I computed diagonal growth. I didn't have a good way to combine the slopes from two grid points to extrapolate to a third. I was just taking the average. Instead, I found a method developed by David Chopp (my advisor) in "Another Look at Velocity Extension in the Level Set Method" (2009) that performs this two point extension by solving

$$F||\nabla \phi || = 1,\hspace{5mm}\mbox{and}\hspace{5mm} \nabla F \cdot \nabla \phi = 0$$

where $$\phi$$ is the surface of the biofilm and $$F$$ is the magnitude of the gradient. Solving this system of equations leads to much better accuracy near the boundary when combining slopes from two nodes to extrapolate to a new node.