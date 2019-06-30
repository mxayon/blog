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

While researching Temporal databases, I found [Bitemporal Modeling](https://en.wikipedia.org/wiki/Bitemporal_Modeling):
<br>
Bitemporal Modeling is a specific case of Temporal database information modeling technique designed to handle historical data along two different timelines. This makes it possible to rewind the information to "as it actually was" in combination with "as it was recorded" at some point in time. In order to be able to do so, information cannot be discarded even if it is erroneous. Within, for example, financial reporting it is often desirable to be able to recreate an old report both as it actually looked at the time of creation and as it should have looked given corrections made to the data after its creation.

Implementations of Bitemporal Modeling are mostly done using relational databases. As such, Bitemporal Modeling is considered different from Dimensional Modeling and complementary to database normalization. The SQL:2011 standard provides language constructs for working with bitemporal data. However, many of current solutions are still vendor-specific.


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

## Greater Than First Order Logic & C.W.A. vs O.W.A.
Closed World Assumption (CWA) - temporal databases hold complete information about the truth

- _*we state what is possible*_   |   needs a place to put it.

[Open World Assumption (OWA)]() - The alternative: to treat the relational structures representing temporal databases as incomplete specifications and use the OW Assumption to answer queries

- _*we state what is not possible*_    |    {} empty OWA - everything is possible; then constrain ontology iteratively, making it more restrictive as we go.

- NaF (Negation as Failure)

| Animal 	| CanFly? 	|
|-------------	|:-------:	|
| Penguine 	| No 	|
| Shark 	| No 	|
| Hummingbird 	| Yes 	|

- Can pigs fly?
      - CWA = False: table does not contain fact.
      - OWA = We don't know: unless we can infer "pigs can or cannot fly"
        - NaF = only false if "pigs cannot fly"
- OWA assumes incomplete information by default
- We can intentionally underspecify and allow others to reuse and extend
  - e.g. All Sharks liveInHabitat; some waterHabitat
  - Are there fresh/ seawater sharks?
  - Do we care? Someone might.
- It can be useful to reuse

##### Ontology

![Ontology Map](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/24-Figure1.5-1.png)
<br>
Ontology Mapping
<br>

![Ontology Engineering](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/106-Figure5.1-1.png)
<br>
Ontology Engineering
<br>

Ontology Development
<br>
![Ontology Development](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/108-Figure5.2-1.png)

A Property Chain
<br>
![Data Table Join](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/120-Figure5.6-1.png)

- **Extending Ontology:** we can add statements, but cannot take any away.
  - *Monotonic*: in extending ontology all existing true statements remain true.

- UNAs: Unique Name Assumptions: Objects have different IDs by default
  - CWA creates UNA
  - OWA doesnt create UNA
    - to allow later assertion that two things are the same or different (or this maybe inferred)
    - _Negation is Required for Distinctness._
      - RDF cannot make assertions about objects being different
      - OW language and other logics can.

- _**Constraints**_: can mean
  - Integrity Constraints (CWA)
    - prevents invalid values from being asserted in a model
    - used for validation/parsing/data input
    - single model: constraints only facts are asserted
  - Logical Axioms (OWA)
    - restrictions, property domain/range
    - everything can be true unless proven otherwise
    - multiple possible models can satisfy the axioms
    - _this may cause some unintuitive inferences_

## Choosing OWA vs CWA
- Analyzing problem domains

| Open World Problem  	| Closed World Problem 	|
|-----------------------------------------------------------------------------------------------------	|:------------------------------------------------------------------------------------------:	|
| Does Rupaul know Kurt Cobain? 	| Is there a bus from  downtown to ocean beach  in 5 mins? (only x trains  & y destinations) 	|
| What are the potential  side effects of drug x?  (answers maybe found in  other resources) 	| Find me drugs that are not  licensed for x? (would  need closure for each) 	|
| What are the factors affecting climate change? (new studies may  improve or validate other factors) 	| When was the worst climate change instance ever recorded? 	|

#### Why Open World
- Underspecification
  - Abstract, nested and unnamed entities
- Easily reusable (and extendable)
- Good at knowledge level (Ontology)
- Good at "schema"-"schema" mapping
  - Asserting/Inferring equivalents
- They naturally deal with incomplete information
  - Domain knowledge where answers are evolving (e.g. science)
- Making an inference

#### Why Closed World
- Paradigm Shift
  - Involves Technology/Experience Catch up
- Some problems are inherently closed world (often those that we ask "which are not... " or have a finite number of elements)
  - but is possible to close the open world (later)
- Dealing with Defaults & Exceptions
- Dealing with Schema-Data mapping
  - integrity constraints, validation (parsing from generation)
  - data structures are typically closed
- Meta-query
  - _What do we know??_

## Interpreting Knowledge on problems

I. Problem Domain A
- Will there be a host for the pre-show?

  | Time 	| Activity 	| Hosts / Awardees 	|
  |---------	|-------------------------------------------------	|--------------------------------------------------	|
  | _**5:00pm**_ 	| _**Pre-show**_ 	| ____ 	|
  | 7:00pm 	| Enter 	| 1993 VMA doors open 	|
  | 7:10 	| First Performance 	| Madonna "bye bye baby" 	|
  | 7:30pm 	| Introduction 	| Christian Slater 	|
  | 8:000pm 	| Best Dance Video - "Free Your Mind" 	| Shaquille O'Neal introduces En Vogue 	|
  | 8:15pm 	| Best Rap Video - "People Everyday" 	| Martin Lawrence introduces Arrested Development 	|
  | _**8:30pm**_  	| _**Best Alternative Video - "In Bloom"**_ 	| _**Michael Richards introduces Nirvana**_ 	|
  | _**8:45pm**_ 	| _**Viewer's Choice Award** - "Living on the Edge"**_ 	| _**RuPaul & Milton Berle introduces Aerosmith**_ 	|
  | 9:00pm 	| Best Direction in Video - "Jeremy by Pearl Jam" 	| Sharon Stone introduces Director Mark Pellington 	|

<br>
* _*Order made up for demonstration purposes. Data gathered from ff resources:*_
<br>
[VMA-Rupaul-Nirvana](http://www.papermag.com/vma-rupaul-nirvana-2597575353.html?rebelltitem=12#rebelltitem12)    |    [MTV Awards List](https://en.wikipedia.org/wiki/1993_MTV_Video_Music_Awards)

- Database says "No"
- OWA says "Don't know" unless a blank is interpreted as "Activity and not(hasSpeaker)"

II. Problem Domain B
- I want to treat my patient with a painkiller that is not an anticoagulant

| Drug 	| Effect 	|
|-------------	|---------------	|
| Aspirin 	| Painkiller 	|
| Wharfarin 	| Anticoagulant 	|
| Paracetemol 	| Painkiller 	|

- Database says "Aspirin", "Paracetamol"
- OWA can't say this unless we make explicit "Paracetamol is not an anticoagulant"

###### OWA is good for describing knowledge in a way that is extensible
###### CWA is good for constraining and validating data

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
[PDF - Open World Assumption -University of Manchester](http://www.cs.man.ac.uk/~drummond/presentations/OWA.pdf)
[Handbook of Temporal Reasoning in Artificial Intelligence](https://www.semanticscholar.org/paper/Handbook-of-Temporal-Reasoning-in-Artificial-Fisher-Gabbay/eb14281c97a583248ddbff5ab71309a3849a8c78)
[Ontology Engineering](https://www.semanticscholar.org/paper/An-Introduction-to-Ontology-Engineering-Keet/662d16cf1914d488022d75baaf7dbf7752066244)



***

_*Statipy Data Explorer*_ uses time in first divide and conquer approach [Statipy Data Explorer](https://mxnkpl.com/blog/statipy_dataexplorer/). While exploring the best ways to group the data, time was a great constant variable
to use as an index for the table. The behavior that followed the graph results when compounding the date index to year level really affects performance of search query for math functions in the future..
(WIP- also proves that data presentation is important in describing and documenting results)
<br>

Here is an example of observing the behaviors while using a primary key in a Data Table/ Join Table/ Data Mapper as a way to merge separate tables in one "pull".
<br>
ERD - Entity Relationship Diagram
![ERD for E.R.](https://i.ibb.co/yWVCN5P/er-erd.png)
<br> [Elephants in the Room](https://elephantsintheroom.herokuapp.com)    |    [Elephants in the Room project on Github](https://github.com/mxayon/elephantsintheroom)

<br>

"Data Mapper" from Martinfowler.com
![datamapper](https://martinfowler.com/eaaCatalog/dataMapper.html)


---
