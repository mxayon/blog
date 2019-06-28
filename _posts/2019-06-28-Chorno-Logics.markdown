---
title: "Chrono Logics"
draft: false
layout: post
date: 2019-06-28 11:11
image: https://i.ibb.co/c1QkqBt/mechanicalclock.png
headerImage: true
tag:
- tools
- time
star: true
category: blog
author: maximonakpil
description: Looking at the logics of time based organization.
---
## A Reference Point
Going through turning points of evolution and trying to document the intersections, I created my [Evolution of Computer Science project: EvoEpochs-Chronomap](https://mxnkpl.com/chronomap.html). While researching precise dates, even BCE and CE are changing reference points and much like when to count the century - (almost like counting a 0 in the start of an index).

_**An interesting thought is to create roadmaps, each layered through multi- disciplinary perspective. This first layer is for inventions and the next layer is design.**_


[Bitemporal Modeling](https://en.wikipedia.org/wiki/Bitemporal_Modeling)



## Time Series Databases

Time Series vs Temporal Databases is a matter of storing events in temporal design and as time series data is indexed on time and usually shows linear increases or decreases.

[Time Series, a Neglected Issue in Temporal Database Research?](https://link.springer.com/chapter/10.1007%2F978-1-4471-3033-8_12)


The cost of swapping in and out of memory can be seen in this performance graph from PostgreSQL, where insert throughput plunges with table size and increases in variance (depending on whether requests hit in memory or require (potentially multiple) fetches from disk).
![https://blog.timescale.com/content/images/2018/12/gif3-1.gif](https://blog.timescale.com/content/images/2018/12/gif3-1.gif)


[On Adaptive Time and Space Chunking](https://blog.timescale.com/time-series-data-why-and-how-to-use-a-relational-database-instead-of-nosql-d0cd6975e87c/)

!["SPACE CHUNKING"](https://blog.timescale.com/content/images/2018/12/image-82.png)

!["Adaptive Chunks"](https://blog.timescale.com/content/images/2018/12/image-84.png)

> By recognizing that time-series data is different, we are able to organize data in a new way: adaptive time/space chunking. This minimizes swapping to disk by keeping the working data set small enough to fit inside memory, while allowing us to maintain robust primary and secondary index support (and the full feature set of PostgreSQL). And as a result, we are able to scale up PostgreSQL significantly, resulting in a 15x improvement on insert rates.

[Timescale](https://blog.timescale.com/time-series-data-why-and-how-to-use-a-relational-database-instead-of-nosql-d0cd6975e87c/)  |   [Timescale on Github](https://github.com/timescale/timescaledb)

[Time Travelling!](https://fauna.com/blog/time-traveling-databases)

[History of Temporal Design](https://www.sciencedirect.com/topics/computer-science/temporal-data-management)

[Temporal Data Base Design](https://nftb.saturdaymp.com/temporal-database-design/)

***

_*Statipy Data Explorer*_ uses time in first divide and conquer approach [Statipy Data Explorer](https://mxnkpl.com/blog/statipy_dataexplorer/)

An example of using a join table of primary keys to merge separate tables in one "pull".
[Elephants in the Room project on Github](https://github.com/mxayon/elephantsintheroom)


---
