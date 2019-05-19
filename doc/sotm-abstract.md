
# A linguistic comparison: Software for OpenStreetMap data extraction and processing in python, R, C++, and rust

## Abstract

This talk will present a "reference manual" for comparing and contrasting
software for extracting, processing, and analysing OpenStreetMap data in four
of the most important contemporary computer languages (python, C++, R, and
rust). This "reference manual" will provide decisive support in choosing the
most appropriate software for a particular research aim.


## Introduction

Researchers working with OpenStreetMap data generally do so via one or more
computer languages, and there exists a wealth of software libraries in various
languages for extracting, processing, and analysing these data. Many people
nevertheless have personal preferences for particular computer languages that
will influence their choice of software. This talk will describe and compare
software for extracting and working with OpenStreetMap data in four of the
currently most important contemporary computer programming languages: python,
R, C++, and rust. 

## Methodology and Findings

The primary software for extracting, processing, and analysing OpenStreetMap
data in the four languages is:

1. In python, "osmnx" (Geoff Boeing, 2017. “OSMnx: New Methods for Acquiring,
   Constructing, Analyzing, and Visualizing Complex Street Networks.”
   Computers, Environment and Urban Systems. 65, 126-139.
   doi:10.1016/j.compenvurbsys.2017.05.004). 
2. In C++, "libosmium" (Jochen Topf, 2013).
3. In R, "osmdata" (Mark Padgham, Bob Rudis, Robin Lovelace, and Maëlle Salmon,
   2017. "osmdata" Journal of Open Source Software, 2(14).
   doi:10.21105/joss.00305).
4. In rust, "osm-xml" (Iivari Äikäs, 2016).

libosmium is designed to process pre-downloaded Protocol Buffer (pbf) files (as
well as xml files), such as the daily planet.pbf dumps, or the
semi-continental-scale pbf dumps provided by geofabrik, and is primarily
a data-extraction and conversion tool. In contrast, both osmnx and osmdata are
interfaces to the overpass server, and are designed to extract and process
smaller, user-specified data sets. libosmium remains the fastest and most
powerful library, particularly through being able to work with all aspects of
the OpenStreetMap data set, including changelogs. It is nevertheless not as
convenient to use as the python or R libraries, and is not as easy to integrate
within modern data-analytical workflows. There is much overlap in functionality
between osmnx (python) and osmdata (R), with both enabling highly customized
extraction of specific aspects of OpenStreetMap data. osmnx offers several
"convenience" functions which enable arguably simpler extraction than osmdata,
with the results stored in a custom "osmnx" graph format. Extraction with
osmdata is only slightly more complicated, yet more flexible for that, and
offers the additional advantage of returning results in a variety of formats,
including the Open Geospatial Consortium and ISO-standard "Simple Features" (an
ability also offered by libosmium). The ability to convert customised sets of
OpenStreetMap data into a widely-used standard format for spatial data analysis
grants "osmdata" a particularly useful place in complex spatial analyses.
"rust" is the newcomer in programming languages, yet was voted the most popular
language for the last 4 years running in the definitive StackOverflow user
survey. rust is a lower level language than either python or R, and current
libraries for extracting and processing OpenStreetMap data are correspondingly
"lower" level, focussing on direct extraction from either pbf or xml formats,
with no ability to convert to representations other than the underlying
OpenStreetMap representation itself, and only limited ability to process these
data. This is nevertheless likely to change rapidly in the near future, and in
OpenStreetMap realms, as in most other areas, rust remains an important
language to watch for future directions.

## Scientific contribution

This presentation will provide a broad overview of relative functionality of
software for extracting and processing OpenStreetMap data in four of the most
widely used contemporary computer programming languages. In doing so, it will
attempt to present a "reference manual" for comparing and contrasting software
for extracting, processing, and analysing OpenStreetMap data, and ultimately to
aid the decision of which software to choose for a particular research aim.

