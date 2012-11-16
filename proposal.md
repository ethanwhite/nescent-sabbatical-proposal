Supporting Eco-Evolutionary Analyses by Integrating Evolutionary Data in the EcoData Retriever
==============================================================================================

Ethan P. White,
Department of Biology and the Ecology Center,
Utah State University,
5305 Old Main Hill,
Logan, UT 84341

Email: ethan.white@usu.edu

Phone: 435-797-2097

Project Summary
---------------



Public Summary
--------------
Large amounts of biological data are being collected every year and made available for analysis.
However, this data is collected by many different groups, in many different ways,
and this means that combining the data to answer broad, general, synthetic questions, is difficult.
To allow scientists to quickly and easily leverage this data,
we have started developing a software package that automatically downloads, cleans up,
and installs many of the most important datasets in synthetic ecology.
The proposed sabbatical will allow the extension of this software to evolutionary biology,
and will allow it to produce complete synthetic datasets to support evolutionary-ecological syntheses. 


Introduction and Goals
----------------------
One of the major challenges for synthetic science is the disconnectedness and heterogeneity of existing data.
This makes acquiring and using this data a time consuming and error prone process.

* General mention of data munging being large fraction of work

This is particularly true when trying to work across disciplinary boundaries,
because while researchers may be familiar with the general availability and structure of data in their own discipline,
they are rarely if ever familiar with the structure and availability of data in related disciplines.

Even when individual datasets can be relatively easily acquired,
combining them to be able to answer broad questions is difficult and time consuming for even experienced programmers.
Since most biologists are not computational experts this difficulty can present a strong limit on synthetic science.

It is increasingly recognized that ecological systems cannot be understood in the absence of evolution.
OR
It is increasingly recognized that evolution and ecology are inextricably linked,
and that even on ecological time scales that evolutionary processes have a strong influence on ecological systems.

**Goal 1: Incorporate taxonomic, phylogenetic, and evolutionary data into the Retriever** 

**Goal 2: Automatically build synthetic datasets to facilitate interdisciplinary synthesis**

**Goal 3: Train biologists to properly work with this type of data**

Proposed Activities
-------------------

* General improvements to the retriever
* Add infrastructure for handling common evolutionary data formats
* Add scripts for major evolutionary data formats
* Add infrastructure for producing synthetic datasets
    * major undertaking requiring major additions to the code base
    * requires extensive expansion of the associated script parser
    * requires homogenizing taxonomies (will leverage existing tools)
* Automated taxonomy cleaning via TNRS, ITIS, etc.

### Initial list of datasets to include
* Encyclopedia of Life
* Catalog of Life
* TreeBASE
* Tree of Life - http://tolweb.org/tree/
* Supertrees
    * Mammals - http://dx.doi.org/10.1038/nature05634
    * Birds - http://linnaeus.zoology.gla.ac.uk/~rpage/birdsupertree/
    * Angiosperms - http://dx.doi.org/10.1073%2Fpnas.0308127100



Rationale For NESCent Support
-----------------------------
NESCent is the international center of evolutionary informatics and is therefore the ideal location for this development.
At NESCent I will have access to both researchers actively developing software for synthetic evolutionary research,
and researchers who are trying to address interdisciplinary evolutionary ecology questions.

The former groups will provide me with colleagues to help me learn more about the structure of major evolutionary databases,
and how to best integrate them with ecological data.

The later group will


Collaborations
--------------



Proposed Timetable
------------------



Anticipated IT Needs & Plan For Making Data/Software Available
--------------------------------------------------------------
Linux workstation, Kinesis keyboard

I and my lab have a long history of open science activities including the publication of data and software under open source licenses (see our GitHub repositories for examples: http://github.com/weecology). The EcoData Retriever is under an MIT License and all code developed during this project will be released under either MIT or BSD licenses.

Anticipated Results
-------------------


