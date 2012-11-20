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
Large amounts of biological data are being collected every year and made available for analysis and synthesis.
One of the primary challenges for synthetic research is the process of identifying the necessary data,
making individual datasets usable, and then integrating the different datasets.
This process is difficult because most biological data does not adhere to any standard format and
violates basic rules of proper data structure.
In addition, linking datasets is challenging due to differences in structure and problems with identifiers for linking data. 
This means that compiling and combining data to answer synthetic questions is difficult,
and requires computational skills and knowledge that many biologists lack.
My lab developed a software package (the EcoData Retriever) to begin to reduce these barriers to synthetic science in ecology.
This package automatically downloads data, cleans it, processes it into proper structure,
and stores it in a variety of common formats for easy analysis.
The proposed research would support a major expansion of the Retriever to:
1) Include evolutionary, taxonomic, and trait information of interest to evolutionary biologists; and
2) Automatically generate synthetic datasets combining data across datasets to allow researchers to rapidly conduct synthetic analyses.
These efforts will focus on facilitating eco-evolutionary synthesis,
since it is now widely recognized that evolution and ecology are inherently intertwined.
This sort of interdisciplinary synthetic research is particularly difficult due to differences in data structure among disciplines and the fact that most researchers are not experts in both evolutionary and ecological data.



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

**Goal 3 alt: Provenance baked in**
One of the current challenges with sythetic data analysis is tracking the many complicated steps involved in assemblying the data.
While much of this is well handled by workflows of various forms,
this process typically starts after much of the data download and munging has already occurred.
I will add functionality to the Retriever to store all of the information necessary for complete provenance with the resulting data.
Data sources, download dates, and the version of the Retriever used to process the data,
will all be recorded. In combination with the Retriever's open source, version controlled,
code base this will allow the entire process from data download through munging to be recorded.
This metadata will be stored in the appropriate table metadata systems for the database management systems,
and in structured comments in csv files.
I will also add an --archive option to the Retriever that will store this data in a log file,
and will store both the raw downloaded data and the processed form as exports/dumps from the chosen database management system.

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

Because the combinations of data for synthetic projects vary substantially,
I will expand our existing scripting system to allow users with limited computational backgrounds to quickly combine datasets in customized ways.

Rationale For NESCent Support
-----------------------------
NESCent is the international center of evolutionary informatics and is therefore the ideal location for this development.
At NESCent I will have access to both researchers actively developing software for synthetic evolutionary research,
and researchers who are trying to address interdisciplinary evolutionary ecology questions.

The former groups will provide me with colleagues to help me learn more about the structure of major evolutionary databases,
and how to best integrate them with ecological data.

The later group will

One of the primary sources for evolutionary and ecological data is DRYAD.
NESCent's active involvement in the development of DRYAD will facilitate the integration of DRYAD data into the Retriever.

Collaborations
--------------
* HIP: Hackathons, Interoperability, Phylogenies
* EvoIO
* Dryad


Proposed Timetable
------------------



Anticipated IT Needs & Plan For Making Data/Software Available
--------------------------------------------------------------
Linux workstation, Kinesis keyboard

I and my lab have a long history of open science activities including the publication of data and software under open source licenses. In fact, this entire proposal was developed in the open on GitHub under a CC-BY license (https://github.com/ethanwhite/ (https://github.com/ethanwhite/nescent-sabbatical-proposal). See my groups GitHub repositories for more examples: http://github.com/weecology). The EcoData Retriever is under an MIT License and all code developed during this project will be released under either MIT or BSD licenses.

Anticipated Results
-------------------
