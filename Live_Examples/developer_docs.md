CompBioBase - Live-Examples
===========
Live-examples (LE) development guidelines
-----
Folder [TP_TEMPLATE](TP_TEMPLATE/) contains a template, use it to start the development of a new live-example, or reformat an existing example.

###Naming and version control
Every LE release which has substantial changes should be assigned a version number which sould appera in the header of README.md. A history of changes should be provided in HISTORY.md file together with hashes of commits that correspond to the current and previous versions.
Folder name should be concise but suggestive of the example nature and start whith a letter code from [this list](../folder_codes.md) depending on the LE topic.
If LE is forked to adjust it to slightly different conditions (eg. software or hardware version) the new folder name should be derived by appending a corresonding descriptor (eg. MD_nucleosome_NAMD_v1.9_wCUDA). For such forked LE the information about their parent (sister) LE should be provided in the header of README.md and the corresponding versions have to be specified.

###Tags
LE are organized with the help of tags (keywords) from the dictionary listed in [tags_list.md](../tags_list.md). Every LE folder should contain tags.md file which list tags from the dictionary one per line.

###LE status
If LE adheres to the strict guidelines described below its status is READY, otherwise it is RAW. The status should be stated in the header of README.md.

###Live-example components and directory structure
####README.md
The README.md file is the main file describing the live-example, theoretical background, goals, prerequisitives (including software), contents of the live-example, step-by-step instructions and anticipated outcomes.
The files should be written using Markdown or GitHub Markdown syntax understandable by [pandoc](http://pandoc.org).
Top line of the file should be human readable title marked as H1 header.

The file should have following sections:
######Metainfo
````
Name: folder_name
Status: READY/RAW
Version: 
Assosiated LE: comma separated list of other LE names
Parent LE name: name of parent LE if this LE was forked
Parent LE version: version of the parent LE
Tags: comma separated list of tags from [tags_list.md](../tags_list.md)
````
######Description
A short description of the LE in several sentences. What does the LE does?

######File structure
Describe what inidividual files and folders do in LE. If too much information make a link to a separte file file_structure.md

######Prerequisitives
List LE or lectures which have to be completed before. Access to computing facilities.

######Software requirements
List the software requirements with versions and links to the web sites or installation guidelines.

######Learning goals

######Introduction (optional)
Give theoretical background and introduction here with needed references.
######Software installation (optional)
If special software should be installed, provide instructions here.
This can link to the SOFT folder README.md if local folder needs to be populated with executables or symlinks to them.
######Running instructions

######Expected results
List here expected results, files, list reference result files.

######References
At this stage references are manually contructed unless we find a better alternative.
####Folder structure
The folder structure follows the CLICOS mnemonic
######code
all the code file and script relevant to this LE.
Ideally names should start with the numbers and underscore according to run sequence
######libs
library files or scripts that are not specific to this tutorial.
These ideally come from the Toolkit folder as symlinks.
######input
All the data files needed as input to this particular LE.
######common
Common parameter files, such as force filed files go here.
######OUTPUT
This is an empty directory that will be populated during execution.
Caps letters highlight that it is the main directory being changed.
The output directory is suggested to be further populated by subdirectories prefixed by numbers, corresponding to the scripts that reside in code.
######SOFT
The soft folder is intended to host small executable program that should be downloaded and installed from external sources. See the Software Requiremetns section. This directory should have the README.md file that directs the user how to populate this directory.

######sample-output
Examples of some output files, for reference.


###General considerations
Images files should be of low size or hosted externally.

