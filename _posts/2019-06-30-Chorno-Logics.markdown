---
title: "Chrono Logics"
draft: false
layout: post
date: 2019-06-30 11:11
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

Enter [Bitemporal Modeling](https://en.wikipedia.org/wiki/Bitemporal_Modeling):
<br>
> Bitemporal Modeling is a specific case of Temporal database information modeling technique designed to handle historical data along two different timelines. This makes it possible to rewind the information to "as it actually was" in combination with "as it was recorded" at some point in time. In order to be able to do so, information cannot be discarded even if it is erroneous. Within, for example, financial reporting it is often desirable to be able to recreate an old report both as it actually looked at the time of creation and as it should have looked given corrections made to the data after its creation.

> Implementations of Bitemporal Modeling are mostly done using relational databases. As such, Bitemporal Modeling is considered different from Dimensional Modeling and complementary to database normalization. The SQL:2011 standard provides language constructs for working with bitemporal data. However, many of current solutions are still vendor-specific.


## Time Series Databases

Time Series vs Temporal Databases is a matter of storing events in temporal design and as time series data is indexed on time and usually shows linear increases or decreases.

[Time Series, a Neglected Issue in Temporal Database Research?](https://link.springer.com/chapter/10.1007%2F978-1-4471-3033-8_12)

The following research about using Time-Series Data and when and how relational databases from [Timescale](https://blog.timescale.com/time-series-data-why-and-how-to-use-a-relational-database-instead-of-nosql-d0cd6975e87c/) provides insightful graphics on the process...


- **Relational databases include:** MySQL, MariaDB Server, PostgreSQL.
- **NoSQL databases include:** Elastic, InfluxDB, MongoDB, Cassandra, Couchbase, Graphite, Prometheus, ClickHouse, OpenTSDB, DalmatinerDB, KairosDB, RiakTS.

- [Design schema for your NoSQL database](https://www.dataversity.net/how-to-design-schema-for-your-nosql-database/)

The cost of swapping in and out of memory can be seen in this performance graph from PostgreSQL, where insert throughput plunges with table size and increases in variance (depending on whether requests hit in memory or require (potentially multiple) fetches from disk).
![https://blog.timescale.com/content/images/2018/12/gif3-1.gif](https://blog.timescale.com/content/images/2018/12/gif3-1.gif)


[On Adaptive Time and Space Chunking](https://blog.timescale.com/time-series-data-why-and-how-to-use-a-relational-database-instead-of-nosql-d0cd6975e87c/)

!["SPACE CHUNKING"](https://blog.timescale.com/content/images/2018/12/image-82.png)

!["Adaptive Chunks"](https://blog.timescale.com/content/images/2018/12/image-84.png)

> By recognizing that time-series data is different, we are able to organize data in a new way: adaptive time/space chunking. This minimizes swapping to disk by keeping the working data set small enough to fit inside memory, while allowing us to maintain robust primary and secondary index support (and the full feature set of PostgreSQL). And as a result, we are able to scale up PostgreSQL significantly, resulting in a 15x improvement on insert rates.

[Timescale on Github](https://github.com/timescale/timescaledb)

[Time Travelling!](https://fauna.com/blog/time-traveling-databases)

[History of Temporal Design](https://www.sciencedirect.com/topics/computer-science/temporal-data-management)

[Temporal Data Base Design](https://nftb.saturdaymp.com/temporal-database-design/)


## Time Complexity
Time is more complex than linearly ordered set of time instants.
- **Natural Numbers** integers, reals
- Durations, Temporal Distances, Periodic sets
- Query: use new _predicate symbols_ in the linear order < symbol has been used so far

***

[Check out this blog post on Open World Assumptions]()

***


"Constraining a Property / Subsetting"
<br>
![Subsetting](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/120-Figure5.6-1.png)
<br>

![Semantic Web Layer Cake](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/96-Figure4.3-1.png)

<div class="side-by-side">
  <div class="toleft">
    <img src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/93-Figure4.2-1.png">
  </div>
  <div class="toright">
    <img src="https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/86-Table4.2-1.png">
  </div>
</div>

![ORM verbalization](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/45-Figure2.2-1.png)

![E-Lico Architechture](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/32-Figure1.9-1.png)

[What are ORM's](https://blog.bitsrc.io/what-is-an-orm-and-why-you-should-use-it-b2b6f75f5e2a) | [UML: Succesor of OO analysis & design](https://www.tutorialspoint.com/uml/uml_overview.htm)

"Sequence Diagrams"
![SeqDiags](https://www.tutorialspoint.com/uml/images/uml_sequence_diagram.jpg)

"Statechart Diagrams"
![statchartdiags](https://www.tutorialspoint.com/uml/images/uml_statechart_diagram.jpg)

"Activity Diagrams"
![activitydiags](https://www.tutorialspoint.com/uml/images/uml_activity_diagram.jpg)

Resources:
[Handbook of Temporal Reasoning in Artificial Intelligence](https://www.semanticscholar.org/paper/Handbook-of-Temporal-Reasoning-in-Artificial-Fisher-Gabbay/eb14281c97a583248ddbff5ab71309a3849a8c78)


"Data Mapper" Martinfowler.com
[datamapper](https://martinfowler.com/eaaCatalog/dataMapper.html)



***

_*Statipy Data Explorer*_ uses time in first divide and conquer approach [Statipy Data Explorer](https://mxnkpl.com/blog/statipy_dataexplorer/). While exploring the best ways to group the data, time was a great constant variable
to use as an index for the table. The behavior that followed the graph results when compounding the date index to year level really affects performance of search query and for math functions in the future..
(WIP- also proves that data presentation is important in describing and documenting results)
<br>

Here is an example of observing the behaviors while using a primary key in a Data Table/ Join Table/ Data Mapper as a way to merge separate tables in one "pull".
<br>
ERD - Entity Relationship Diagram
![ERD for E.R.](https://i.ibb.co/yWVCN5P/er-erd.png)
<br> [Elephants in the Room](https://elephantsintheroom.herokuapp.com)    |    [Elephants in the Room project on Github](https://github.com/mxayon/elephantsintheroom)

<br>

---
