Supporting Evolutionary Synthesis by Integrating Evolutionary Data in the EcoData Retriever
===========================================================================================

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
Increasingly large quantities of biological data are being generated and
made publicly available for analysis.
This data includes the results from: 1) large coordinated sampling efforts
such as the National Ecological Observatory Network (http://neoninc.org);
2) compilations of results into standardized repositories
such as GenBank (http://www.ncbi.nlm.nih.gov/genbank/) or the Tree of Life (http://tolweb.org/tree);
and 3) the publication of individual datasets in repositories like Dryad (http://www.datadryad.org)
due to increasing journal requirements for data deposition (Whitlock et al. 2010).

As a result of this rapidly expanding availability of data,
synthetic research in biology is increasingly limited by the rate at which available data can be acquired, organized, and analyzed.
Unfortunately, this process of assembling data for synthesis is time consuming and
error prone, because most biological datasets do not adhere to any agreed-upon standards in format,
data structure or method of access (Jones 2006).
This problem persists despite repeated attempts to improve the structure and
usability of data in a number of biological disciplines (e.g., Jones 2006, Reichman et al. 2011).

Even when individual datasets can be relatively easily acquired,
combining them to be able to answer broad questions is difficult and time consuming,
even for experienced data scientists.
This task is inherently both labor and knowledge intensive,
and is further complicated variable data structures, inconsistent use of unique linking fields,
and changes in taxonomies and other common sources of connecting different datasets.

These problems with biological data mean that scientists spend a lot of time simply assembling,
cleaning, and combining datasets.
This takes time away from the scientific aspects of the research (Morris & White in review).
In addition, the skills and tools required to assemble data are often not required for
actually conducting synthetic science *per se*.
This means that the difficulty of assembling data can serve as a major barrier,
preventing many scientists from conducting synthetic research at all.
These challenges are magnified further when trying to work across disciplinary boundaries.
While researchers may be familiar with the general availability and structure of data in their own discipline,
they are rarely, if ever, familiar with the structure and availability of data in related disciplines.

My lab has begun to address these challenges by developing a software package (the EcoData Retriever; http://ecodataretriever.org) to make it easier to conduct synthetic science in ecology.
This package automatically downloads data from individual datasets,
cleans it, processes it into proper structure,
and stores it in a variety of common formats for easy analysis.
While this package has proved useful to us and a growing number of other researchers,
it is limited by its lack of evolutionary data,
and support for automatically integrating evolutionary and ecological datasets.

With the leadership of NESCent over the past decade, evolutionary synthesis has now
come to the forefront of synthetic research in biology.
In addition, it is increasingly recognized that evolution and ecology are inextricably linked,
and that even on ecological time scales that evolutionary processes have a strong influence
on ecological systems (citations). This means that in order to best facilitate synthesis
in both evolution and ecology that the Retriever needs to expand to include evolutionary data.
It also needs to move beyond helping researchers at the level of the individual dataset and
begin facilitating the combination of datasets to automate the process of producing data
for synthetic projects as much as possible.
Finally, it needs to be expanded to address the challenge of documenting the provenance of
both data and processing the occurs in the formation of synthetic datasets.
I propose to address these critical needs by addressing three major goals:

**Goal 1: Incorporate evolutionary, phylogenetic, and taxonomic data into the Retriever**.
To facilitate evolutionary and eco-evolutionary synthesis I will add an array of evolutionary data
to the Retriever including phylogenetic, taxonomic, and trait data as well as other useful data
identified through interactions with individuals visiting or in residence at NESCent.

**Goal 2: Automatically build synthetic datasets to facilitate interdisciplinary synthesis**.
Once clean, well formated, data exists for individual datasets,
the next major challenge is combining those datasets for analysis.
I will add the ability to combine datasets for synthesis by adding core architecture to address this problem and
by modifying the existing scripting language to allow users without strong computational backgrounds to use
the Retriever to produce these datasets.

**Goal 3: Provenance baked in**.
It is increasingly recognized that in order for science to be replicable/reproducible that the history of the
entire process from data collection through analysis needs to be documented.
However, rigorous documentation of this process often begins after data acquisition and munging has occurred.
I will add automated provenance recording and data archiving to the Retriever to make recording the details
of the data munging process as simple as pushing a button.

In combination with further improvements to the software in general
(e.g., an improved testing framework with continuous integration and better documentation)
addressing these goals will result in a key tool for supporting evolutionary and
eco-evolutionary synthesis.

Proposed Activities
-------------------

**Goal 1: Incorporate evolutionary, phylogenetic, and taxonomic data into the Retriever** 

**Goal 2: Automatically build synthetic datasets to facilitate interdisciplinary synthesis**

**Goal 3: Provenance baked in**
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
and will store both the raw downloaded data and the processed form as exports/dumps from the chosen database

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

I and my lab have a long history of open science activities including the publication of data and software under open source licenses. In fact, this entire proposal was developed in the open on GitHub under a CC-BY license (https://github.com/ethanwhite/nescent-sabbatical-proposal). See my groups GitHub repositories for more examples: http://github.com/weecology). The EcoData Retriever is under an MIT License and all code developed during this project will be released under either MIT or BSD licenses.

Anticipated Results
-------------------
