---
layout: project
title: Shadow Analysis
description: Shadow Analysis of Places Around the World
image: /assets/
category: "Personal Projects"
order: 2
---

Key Words: Shadows, MATLAB, Greyscale Analysis, Google Earth, Geospatial

The curiosity question here is, how can one quantify the amount of shadow that a city or town has? Sure, a city will have more shade than a rural town, but by how much? And, is there a meaningful relationship between population density and amount of shade? 

I first looked at Manhattan. Qualitatively, the "darker" spots are shade. To find "darker sports" I used MATLAB Image Analysis to understand the numerical greyscale values of the pixels. But then, trouble. Trees and rivers also showed up within my defined greyscale range for shade. So, I had to look into the RGB values as well to remove the greener and bluer objects. This whole project involved a large amount of tuning and working with messy data. 


<div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center;">

  <img src="{{ '/assets/images/shadow-analysis/greyscale-table.png' | relative_url }}" width="200px">
  <img src="{{ '/assets/images/shadow-analysis/ny-shadow-graph.png' | relative_url }}" width="200px">
  <img src="{{ '/assets/images/shadow-analysis/portfolio1.png' | relative_url }}" width="200px">
  <img src="{{ '/assets/images/shadow-analysis/portfolio2.png' | relative_url }}" width="200px">
  <img src="{{ '/assets/images/shadow-analysis/portfolio3.png' | relative_url }}" width="200px">
  <img src="{{ '/assets/images/shadow-analysis/Shadow-pop-density.png' | relative_url }}" width="200px">
  <img src="{{ '/assets/images/shadow-analysis/threshold-table.png' | relative_url }}" width="200px">

</div>
