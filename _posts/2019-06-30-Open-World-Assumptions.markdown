---
title: "Open World Assumptions"
draft: false
layout: post
date: 2019-06-30 11:11
image: https://i.ibb.co/Vq1kp2v/schrodingers-cat-image.png
headerImage: true
tag:
- tools
- time
- database
- ontology
- semanticweb
star: true
category: blog
author: maximonakpil
description: Open World Assumptions vs. Closed World Assumptions.
---
## OWA and CWA
Checkout previous post on [Temporal Databases & Time Series](https://mxnkpl.com/blog/Chorno-Logics/)


## Greater Than First Order Logic & C.W.A. vs O.W.A.
Closed World Assumption (CWA) - temporal databases hold complete information about the truth

- _*we state what is possible*_   |   needs a place to put it.

[Open World Assumption (OWA)](https://www.dataversity.net/introduction-to-open-world-assumption-vs-closed-world-assumption/) - The alternative: to treat the relational structures representing temporal databases as incomplete specifications and use the OW Assumption to answer queries

- _*we state what is not possible*_    |    {} empty OWA - everything is possible; then constrain ontology iteratively, making it more restrictive as we go.

- NaF (Negation as Failure)

| Animal 	| CanFly? 	|
|-------------	|:-------:	|
| Penguine 	| No 	|
| Shark 	| No 	|
| Hummingbird 	| Yes 	|

Can pigs fly?
      - CWA = False: table does not contain fact.
      - OWA = We don't know: unless we can infer "pigs can or cannot fly"
        - NaF = only false if "pigs cannot fly"
OWA assumes incomplete information by default
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

**Extending Ontology:** we can add statements, but cannot take any away.
  - *Monotonic*: in extending ontology all existing true statements remain true.

UNAs: Unique Name Assumptions: Objects have different IDs by default
  - CWA creates UNA
  - OWA doesnt create UNA
    - to allow later assertion that two things are the same or different (or this maybe inferred)
    - _Negation is Required for Distinctness._
      - RDF cannot make assertions about objects being different
      - OW language and other logics can.

_**Constraints**_: can mean
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
Analyzing problem domains

| Open World Problem  	| Closed World Problem 	|
|-----------------------------------------------------------------------------------------------------	|:------------------------------------------------------------------------------------------:	|
| Does Rupaul know Kurt Cobain? 	| Is there a bus from  downtown to ocean beach  in 5 mins? (only x trains  & y destinations) 	|
| What are the potential  side effects of drug x?  (answers maybe found in  other resources) 	| Find me drugs that are not  licensed for x? (would  need closure for each) 	|
| What are the factors affecting climate change? (new studies may  improve or validate other factors) 	| When was the worst climate change instance ever recorded? 	|

#### Why Open World
Underspecification
  - Abstract, nested and unnamed entities
Easily reusable (and extendable)
Good at knowledge level (Ontology)
Good at "schema"-"schema" mapping
  - Asserting/Inferring equivalents
They naturally deal with incomplete information
  - Domain knowledge where answers are evolving (e.g. science)
Making an inference

#### Why Closed Worl
Paradigm Shift
  - Involves Technology/Experience Catch u
  Some problems are inherently closed world (often those that we ask "which are not... " or have a finite number of elements)
  - but is possible to close the open world (later
    Dealing with Defaults & Exception
    Dealing with Schema-Data mapping
  - integrity constraints, validation (parsing from generation)
  - data structures are typically close
  Meta-query
  - _What do we know??_

## Interpreting Knowledge on problems

I. Problem Domain A

Will there be a host for the pre-show?

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

_*Order made up for demonstration purposes. Data gathered from ff resources:*_
<br>
[VMA-Rupaul-Nirvana](http://www.papermag.com/vma-rupaul-nirvana-2597575353.html?rebelltitem=12#rebelltitem12)    |    [MTV Awards List](https://en.wikipedia.org/wiki/1993_MTV_Video_Music_Awards)

- Database says "No"
OWA says "Don't know" unless a blank is interpreted as "Activity and not(hasSpeaker)"

II. Problem Domain B
I want to treat my patient with a painkiller that is not an anticoagulant

| Drug 	| Effect 	|
|-------------	|---------------	|
| Aspirin 	| Painkiller 	|
| Wharfarin 	| Anticoagulant 	|
| Paracetemol 	| Painkiller 	|

- Database says "Aspirin", "Paracetamol"
- OWA can't say this unless we make explicit "Paracetamol is not an anticoagulant"

###### OWA is good for describing knowledge in a way that is extensible
###### CWA is good for constraining and validating data

![ORM verbalization](https://ai2-s2-public.s3.amazonaws.com/figures/2017-08-08/662d16cf1914d488022d75baaf7dbf7752066244/45-Figure2.2-1.png)

Resources:
[PDF - Open World Assumption -University of Manchester](http://www.cs.man.ac.uk/~drummond/presentations/OWA.pdf)
[Ontology Engineering](https://www.semanticscholar.org/paper/An-Introduction-to-Ontology-Engineering-Keet/662d16cf1914d488022d75baaf7dbf7752066244)


***

[Statipy Data Explorer](https://mxnkpl.com/blog/statipy_dataexplorer/)
<br>



[Elephants in the Room](https://elephantsintheroom.herokuapp.com)    |    [Elephants in the Room project on Github](https://github.com/mxayon/elephantsintheroom)

<br>

ERD - Entity Relationship Diagram for Elephants in the Room
![ERD for E.R.](https://i.ibb.co/yWVCN5P/er-erd.png)


---
