--------------   -------------------------------------------
**Title**        Unifying workflow systems with the CWL
**Authors**      Peter Amstutz^0^, Nebojša Tijanić^1^, Stian Soiland-Reyes^2^, Abram Connelly^0^,
                 John Kern^3^, Luka Stojanovic^1^, Ward Vandewege[0], Tim Pierce[0], John Chilton[4],
                 Maxim Mikheev[5], Samuel Lampa[6][7], Hervé Ménager[8], Scott Frazer[9],
                 Venkat Sai Malladi[10], _Michael R. Crusoe_[11]
**Contact**      mcrusoe@msu.edu
**URLs**         <http://common-workflow-language.github.io/>
                 <https://github.com/common-workflow-language/common-workflow-language/>
**License**      Apache License, Version 2.0
--------------   -------------------------------------------

[0] Curoverse Inc.
[1] Seven Bridges Genomics, Inc.
[2] University of Manchester, School of Computer Science
[3] AccuraGen Inc.
[4] Penn State University, The Galaxy Project
[5] BioDatomics Inc.
[6] Uppsala University, Department of Pharmaceutical Biosciences
[7] BILS (Bioinformatics Infrastructure for Life Sciences)
[8] Institut Pasteur
[9] The Broad Institute
[10] Stanford University
[11] Michigan State University, Microbiology and Molecular Genetics

<!-- Prompts in HTML comments are from

http://phdtalk.blogspot.ro/2011/08/how-to-write-abstract-in-30-minutes.html -->

<!-- Motivation: Why do we care about the problem and the results? -->

Bioinformatic workflow platforms provide provenance tracking, execution and
data management, repeatability, and a platform for data exploration and
visualization. Example F/OSS bioinformatic workflow platforms are Arvados,
DiscoveryEnvironment, DNANexus, Galaxy, Mobyle, and Yabi. Each one represents
workflows using a different vocabulary and format and adding a new tool
requires a different procedure for each system.

<!-- Problem statement: What problem are you trying to solve? -->

Neither the description of the workflows nor the descriptions of the tools that
power them are usable outside of the workflow platforms they were written for.
This results in duplicated efforts and reduced reusability of these components.

<!-- Approach: How did you go about solving or making progress on the problem?
Did you use simulation, analytic models, prototype construction, or analysis of
field data for an actual product? -->

Three engineers (Peter Amstutz, John Chilton, and Nebojsa Tijanic) from leading
open source bioinformatic workflow groups (Curoverse, Galaxy Team, and Seven
Bridges Genomics) and a tool author (Michael R. Crusoe / khmer project /
Michigan State University) started working together at the BOSC 2014 Codefest
with an initial focus on developing a portable command line tool description
format. As the group grew the scope expanded to include workflow descriptions.
The group placed high value on re-using existing formats and ontologies; they
governed themselves with a lazy consensus / do-ocracy approach.

<!-- Results: What's the answer? -->

On March 31st, 2015 the group released their second draft of the Common
Workflow Language specification. The serialized form is a YAML document that is
validated by an Avro schema and can be interpreted using JSON-LD. The documents
are also valid Wf4Ever descriptions after a simple transformation. Future
drafts will include the use of the EDAM ontology to describe the tools enabling
tool discovery via the ELIXIR tool registry.

<!-- Conclusions: What are the implications of your answer? Is it going to
change the world (unlikely), be a significant "win", be a nice hack, or
simply serve as a road sign indicating that this path is a waste of time (all
of the previous results are useful)? -->

The popular bioinformatics platform Galaxy is going to be accepting CWL tool
and workflow descriptions with planned support for exporting workflows into the
CWL format. This will scientists, researchers and other analysts to share their
workflows and pipelines in an interoperable and yet human readable manner. Tool
authors and other community members will also benefit as they will only have to
describe their tool’s interface once. Uptake is expected by Curoverse and Seven
Bridges Genomics as they had dedicated considerable engineering resources to
the project.
