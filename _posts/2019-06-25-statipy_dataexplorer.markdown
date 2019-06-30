---
title: "Statipy Data Explorer"
draft: false
layout: post
date: 2019-06-25 11:11
image: https://i.ibb.co/6NBt21B/yearmax-Tpop-Xyfreq.png
headerImage: true
tag:
- statipy
- database
- explorer
- satiricalbuttrue
- time
star: true
category: blog
author: maximonakpil
description: Data Exploration for Statipy
---

## What's data got to do with it?
Switching up an approach to creating tools, I found data journalism or data digging a fun way to prove how small decisions affect the overall outcome.


> After setting your goal, you then need to determine how to measure this result. In this example, the primary metric is the number of active accounts, which is simple to measure. However, as you continue to build your product, you’ll want to consider additional metrics, such as the on-boarding drop-off rate, account closure rate and user account activity. Build these metrics into the product from the beginning so that you can verify that the product is meeting the market's needs.

> Now that you’ve identified metrics to define your goal, you can start building your product and defining the backlog. Prioritize the effort to create your metrics in the initial release so that you can continually evaluate whether you've reached your goal. Once you've measured results, you can start building functionality in a hypothesis-driven way to experiment and iterate on ideas. After each feature release, evaluate the status of your results and decide whether to iterate on the product more or move on to another goal.

-> from this [DevBridge Article - Build the Right Product with Results Driven Development](https://www.devbridge.com/articles/build-the-right-product-with-results-driven-development/)

Another interesting view, a common cultural connotation in work places, [Gung-Hoism, Competition, Merit-based rewards and Work-volume](https://workplace.stackexchange.com/questions/14348/what-is-meant-by-results-oriented-development-team)


> A point of confusion
When most people think of being results-driven, they are really thinking of being data-driven. The concepts are similar, but there is a subtle, yet important difference between the two. People who are data-driven track loads of data. They collect everything in the hopes that analyzing the data will uncover some unknown truths about their products or customers. People who are results-driven, track very little data. They only collect the data that most specifically tells them if their customers are doing more of the things they want them to do.

-> [Results Driven Culture](https://academy.taplytics.com/developing-a-results-driven-culture/)


[Probalistic Programming and Bayesian Methods for Hackers ](https://nbviewer.jupyter.org/github/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/blob/master/Chapter1_Introduction/Ch1_Introduction_PyMC3.ipynb)


[Bayesian Methods for Hackers](https://camdavidsonpilon.github.io/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/)   |   [BMH on Github](https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers)

_***"Satirical but True"***_

## What is Statipy?

Check out my previous post on the build process of [Statipy](https://mxnkpl.com/blog/statipy/) - using Spotipy python wrapper.

### Data Exploration

Using the superbly documented and structured Spotify Api I am able to make this diving work fruitful.

**If you want to try it on your own playlist, checking out the spotify api documentation on how the JSON data is structured definitely helped me in my approach..**

Due to the nature of tracks on _the shared_ playlists, I wanted to first explore the song population over time.

I. Dates in Years
Artists in Playlists grouped in to repeated track vs. non repeated track count - over all popularity in album years.


<a href="https://imgbb.com/"><img src="https://i.ibb.co/gDQ56M3/art-rpt-Xno-rpt-Tpop.png" alt="art-rpt-Xno-rpt-Tpop" border="0"></a>

<br />

Years w/ Most Tracks vs Yearly Average Track Popularity
<a href="https://imgbb.com/"><img src="https://i.ibb.co/6NBt21B/yearmax-Tpop-Xyfreq.png" alt="yearmax-Tpop-Xyfreq" border="0"></a>


<br />

Artists with Most Repeated Tracks (0-8 instances)
<a href="https://imgbb.com/"><img src="https://i.ibb.co/QbN2vdS/artists-maxrepeats.png" alt="artists-maxrepeats" border="0"></a>
<br />


Years with most track repeats
<a href="https://imgbb.com/"><img src="https://i.ibb.co/vBxytpW/dates-w-most-repeats.png" alt="dates-w-most-repeats" border="0"></a>

<br />

Yearly track count over time
<a href="https://imgbb.com/"><img src="https://i.ibb.co/KWqzZpM/lineplot-dates11.png" alt="lineplot-dates11" border="0"></a>

<br />

Newest Tracks - Stacked - (Yearly track count) x (Artist Track count) x (Track popularity)
<a href="https://imgbb.com/"><img src="https://i.ibb.co/wy8c00y/newest-tracks.png" alt="newest-tracks" border="0"></a>

<br />

Oldest Tracks - Stacked - (Yearly track count) x (Artist Track count) x (Track popularity)

<a href="https://imgbb.com/"><img src="https://i.ibb.co/gdbTFGL/oldest-tracks.png" alt="oldest-tracks" border="0"></a>

<br />

Artists: (Total popularity > 25%) & (frequency > 50%)
<a href="https://imgbb.com/"><img src="https://i.ibb.co/pQGyhHj/tpop25songfreq50.png" alt="tpop25songfreq50" border="0"></a>

<br />

Artists: (Total popularity > 25%) & (frequency over > 75%)

<a href="https://imgbb.com/"><img src="https://i.ibb.co/wYMjq8y/tpop25songfreq75.png" alt="tpop25songfreq75" border="0"></a>

<br />

## Using Jupyter Notebook and IPython Majick

[Jupyter notebooks tips & tricks](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/)

[Interesting Notebooks](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks)

## The Gist of it all

[Statipy Data Explorer 1](https://gist.github.com/mxayon/91d83b2f3bc6cd894bf26d5d71dc240a)
<br>

<script src="https://gist.github.com/mxayon/91d83b2f3bc6cd894bf26d5d71dc240a.js"></script>

[Artist Feature 1 (Rupaul Draft)](https://gist.github.com/mxayon/0888055e91991abe46d3fbf90ddddcf2)

<script src="https://gist.github.com/mxayon/0888055e91991abe46d3fbf90ddddcf2.js"></script>
