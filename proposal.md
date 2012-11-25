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
and is further complicated by variable data structures, inconsistent use of unique linking fields,
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
it is limited both by its lack of evolutionary data,
and its lack of ability to automatically integrate evolutionary and ecological datasets.

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
Whenever possible this work will utilize existing informatics resources to avoid duplication of effort.

**Goal 2: Automatically build synthetic datasets to facilitate interdisciplinary synthesis**.
Once clean, well formatted, data exists for individual datasets,
the next major challenge is combining those datasets for analysis.
I will add the ability to combine datasets for synthesis by adding core architecture to
address this problem and by modifying our existing approach to allowing users
without strong computational backgrounds to use the Retriever to produce these datasets.

**Goal 3: Provenance baked in**.
It is increasingly recognized that in order for science to be replicable/reproducible that
the history of the entire process from data collection through analysis needs to be documented.
However, rigorous documentation of this process often begins after data acquisition and
munging has occurred.
I will add automated provenance recording and data archiving to the Retriever to make recording
the details of the data acquisition and processing phase of a project as simple as pushing a button.

In combination with further improvements to the software in general
(e.g., an improved testing framework with continuous integration and better documentation)
addressing these goals will result in a key tool for immediately supporting evolutionary and
eco-evolutionary synthesis using published data in the existing format,
while broader initiatives (e.g., Parr et al. 2012, DataONE) work
towards developing more complex and inclusive solutions based on new standards
and infrastructure for data publication.

Proposed Activities
-------------------

### Goal 1: Incorporate evolutionary, phylogenetic, and taxonomic data into the Retriever

A broad array of datasets relevant to evolutionary and eco-evolutionary synthesis
will be added to the Retriever. Thanks for a number of ongoing efforts by other
groups (including some based at NESCent) much of this work will simply involve
accessing web services to allow their data to be accessed through the Retriever
and readily integrated with other data sources.

This work will include integration with existing taxonomic and phylogenetic
informatics efforts (see below) and the development of the list of data to add will
be informed by actively interacting with working
group members and postdocs at NESCent to determine which types of data,
and which specific datasets, tend to be used most frequently by the evolutionary
synthesis community. I also plan to provide training to the NESCent community about
how to add datasets to the Retriever themselves, so that they can easily add whatever
data they need. This has the
potential to vastly expand the amount of data supported through contributions by
users of the Retriever.

#### Integration of taxonomic tools

One of the major challenges in linking datasets in biology are changes and inconsistencies
in taxonomies. As part of this project I will integrate the Retriever with existing resources
for accessing and standardizing taxonomic information
(e.g., the iPlant and/or Phylotastic's Taxonomic Name Resolution Services,
http://tnrs.iplantcollaborative.org/, http://www.evoio.org/wiki/Phylotastic/TNRS;
Integrated Taxonomic Information Service, http://www.itis.gov/;
Global Names Resolver, http://resolver.globalnames.org/).
When importing datasets users will be given the option to have the Retriever automatically
clean up and standardize the taxonomic information using these services.
Logs will be generated of all taxonomic changes
(either as log files or as tables added to the database)
to allow for full back tracking to the original data source.
In addition to improving analysis and reporting of individual datasets,
this integration of taxonomic tools will facilitate **Goal 2**.

#### Integration of phylogenetic tools

One of the key components to integrating evolutionary and ecological data
is the phylogenetic tree for the species involved. I will leverage existing informatics efforts
that are compiling and providing access to phylogenetic data
(e.g., Phylotastic, http://phylotastic.org; Tree of Life; http://tolweb.org; TreeBASE, http://treebase.org/)
through web services to integrate phylogenies with other biological data.

Accomplishing this goal will require the addition of code for interacting with web
services for other informatics efforts, adding the ability to handle evolutionary
data that is not currently covered by other initiatives, and adding scripts for
key datasets.

#### Trait and life history data

Publicly available trait and life history data is currently distributed across a wide array
of different sources
(e.g., Freshwater Biological Traits Database, http://www.epa.gov/ncea/global/traits/;
AnAge, http://genomics.senescence.info/species/;
USDA plants, http://plants.usda.gov/; and numerous publications). As much of this public data
as will made available by the Retriever. The data will be restructured to allow all of
the different trait databases to be consistently integrated with other data.

### Goal 2: Automatically build synthetic datasets to facilitate interdisciplinary synthesis

One of the biggest challenges in synthetic research is combining datasets.
I will develop tools in the Retriever to facilitate two different kinds of dataset combination.
First, I will build functionality to combine similar data from datasets
with different structures into single synthetic datasets.
For example, in White et al. 2012 we combined data from six different datasets,
with widely differing structures,
to analyze species abundance distributions across ecosystems and taxonomic groups.
However, we did this work by writing individual sets of queries for each dataset,
resulting in over 300 lines of Python + SQL that is fragile, scales poorly, and is not generalizable.
The updated Retriever will allow the specification of fields in different datasets
that should be combined into a single core field in a synthetic dataset.
The ability to use queries of the original dataset to generate the table with the
necessary fields will also be included.
Second, I will build functionality to allow different types of datasets to be combined
based on a set of common linking fields.
This is again work that my group has done in the past (e.g., Thibault et al. 2011 combines
trait and ecological data to analyze patterns of avian body size),
but in very project specific ways.
I will generalize the Retriever to allow taxonomic, phylogenetic, trait, and ecological data
to be combined into synthetic datasets for rapid analysis.

Because the combinations of data for synthetic projects vary substantially,
I will also expand our improve and expand our existing system to allow users with limited
computational backgrounds to quickly combine datasets in customized ways without programming.
In collaboration with Ben Morris, I will improve our existing approach to allowing
users with limited computational backgrounds to add information about datasets not currently
in the Retriever by transitioning our existing scripting system for describing the structure
of individual datasets to use the Resource Description Framework (RDF) with an ontology
written in Web Ontology Language(OWL). This will make it easier to describe the relationships
between different datasets and serve as a building block for integrating the Retriever more
thoroughly into the growing eco-evolutionary informatics ecosystem.

### Goal 3: Provenance baked in
One of the current challenges with synthetic data analysis is tracking the many complicated steps involved in assembling the data.
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

Rationale For NESCent Support
-----------------------------
NESCent is the international center of evolutionary informatics and is therefore
the ideal location for this development.
At NESCent I will have access to both researchers actively developing software
for synthetic evolutionary research,
and researchers who are trying to address interdisciplinary evolutionary ecology questions.
The first group will allow me to learn more about what kinds of datasets and what data
combinations are most needed by the evolutionary synthesis community.
All of my efforts will draw as much as possible on existing initiatives to avoid
duplicating effort,
and the second group will provide me with colleagues developing the cutting edge of
informatics resources which will help facilitate the integration of the Retriever
with existing initiatives.
In addition, one of the primary sources for evolutionary and ecological data is DRYAD.
NESCent's active involvement in the development of DRYAD will facilitate the integration of
DRYAD data into the Retriever.

Collaborations
--------------
Ben Morris, the undergraduate student in my lab who lead the development of the
Retriever, is now in graduate school at the University of North Carolina and part of the
NESCent informatics group. Ben has agreed to collaborate on this expansion of the Retriever,
and being in the same location as will facilitate this effort.
In addition, I hope to meet regularly with members of the NESCent IT group to coordinate
integration of evolutionary tools into the Retriever.


Proposed Timetable
------------------

I propose a 12-month sabbatical from August 15, 2013 to August 15, 2014.
The two months will be spent shoring up the fundamentals of the Retriever
by improving the testing framework, adding continuous integration, and
improving the documentation.
This will make adding new features faster and safer, and make the code
more maintainable in the long run (Wilson et al. 2012).
While conducting this ground work I plan to interact actively with
the NESCent informatics and scientific communities to identify the
best areas to focus effort in **Goals 1 & 2**.
Months 3-6 will focus on **Goal 1** including the integration of
taxonomic tools, which is crucial to the next phase.
Months 7-10 will focus on implementing **Goal 2**.
Finally months 11-12 will combine the implementation of **Goal 3**, wrap
up of remaining tasks from the other two goals.
Releases will occur throughout the year as new features are developed
and datasets added.



Anticipated IT Needs & Plan For Making Data/Software Available
--------------------------------------------------------------
I will be developing software as part of this proposal,
but I will be handling all of the development myself and therefore will not require IT support
(though I greatly look forward to the possibility of interacting with this group).
I will require only a Linux workstation.

I and my lab have a long history of open science activities including the publication of data and software under open source licenses. In fact, this entire proposal was developed in the open on GitHub under a CC-BY license (https://github.com/ethanwhite/nescent-sabbatical-proposal). See my group's GitHub repositories for more examples: http://github.com/weecology). The EcoData Retriever is released under an MIT License (an approved OSI open source license) and all code developed during this project will be released under MIT or compatible licenses.


Anticipated Results
-------------------
I anticipate that this proposal will result in 2-3 new major releases of the Retriever.
This will include substantial expansions and improvements of the website
(http://ecodataretriever.org) and associate documentation.
In addition, the rOpenSci team and I are planning do work on wrapping the Retriever's 
command line interface for their system to allow it to be used from inside of R.
This work will likely occur during my sabbatical and will result in a new R package published on CRAN.

References Cited
----------------

Jones, M. B., M. P. Schildhauer, O. J. Reichman, and S. Bowers. 2006. The New Bioinformatics: Integrating Ecological Data from the Gene to the Biosphere. Annual Review of Ecology, Evolution, and Systematics 37: 519-544.

Parr, C.S., R. Guralnick, N. Cellinese, and R.D.M. Page. 2012. Evolutionary informatics: unifying knowledge about the diversity of life. Trends in Ecology & Evolution 27:94 - 103. 

Reichman, O. J., Jones, M. B. & Schildhauer, M. P. 2011. “Challenges and Opportunities of Open Data 	in Ecology.” Science 331, 703–705.

Thibault, K.M., E.P. White, A.H. Hurlbert, and S.K.M. Ernest. 2011. Multimodality in the individual size distribution of bird communities. Global Ecology and Biogeography 20:145-153.

White, E.P., K.M. Thibault, and X. Xiao. 2012. Characterizing species-abundance distributions across taxa and ecosystems using a simple maximum entropy model. Ecology 93:1772–1778.

Whitlock, M.C., M.A. McPeek, M.D. Rausher, L. Rieseberg, and A.J. Moore. 2010. Data Archiving. American Naturalist 175:145-146.