# Studying the Marvel Universe, the artificial world that takes place in the universe of the Marvel comic books, as an example of a social collaboration network. This lab assignment done in Azure Databricks uses Spark to study the relationship between Marvel characters and publications.

## The data used in this lab assignment comes from the Marvel Chronology Project (http://bioinfo.uib.es/~joemiro/marvel/porgat.txt)

###  Why study the Marvel Universe?
A graph is simply a mathematical tool. It consists of a set of points (called the nodes) joined by a set of lines (called the arcs). Graphs have many uses in science and engineering. They can model communication networks, electrical circuits, molecules, etc. In the last few years it has become of fashion to study very large graphs, with thousands or even millions of nodes and arcs, mainly because of the socioeconomic interest of networks that can be modeled as one of these graphs.

Some 'ideal' models of large graphs, very regular or completely random, are well known in physics and mathematics, but none seem suited to represent interesting real graphs of this kind. It is therefore necessary to develop new graph models that will allow us to understand these social networks. To be able to build these models it is necessary to know the data and the evolution of as many real graphs as possible, with as much variety in their nature as can be achieved. And here is where our analysis of the Marvel Universe enters.

We are analyzing the Marvel Comics collaboration graph. The Marvel Universe is a totally artificial social network that pretends to imitate a real social graph, and therefore its interesting to find out if the properties of this graph were similar to a real one. Of course, while doing this lab, we were aware that the subject was amusing and fun, and that physicists and mathematicians that were Marvel fans would like to know who was at the center/ diameter, of the Marvel Universe

Our analysis shows that the Marvel Universe is closer to a real social graph than one might expect, but is not exactly 'real.' This data, and a following analysis of how the graph has grown, can be used to contrast and refine the models for the social graphs that have been used to date, the ones that later on will imprint subjects as dissimilar as epidemiology or security.

# Understanding the data file

As mentioned above, the data file contains information about Marvel characters, publications, and which character appeared in each publication. There are two sections in the file:

Vertices (section begins in line 1 with a header in the form of *Vertices 19428 6486):

Characters: lines 2-6487 in the format 6481 "DETHSTRYK", where 6481 is the node id and the name is within double quotes

Publications: lines 6488-19429 in the same format as characters

Edgeslist (section begins in line 19430 with a header in the form of *Edgeslist): lines 19431 to the end of the file. 

The edge information is in the following format: 2 6488 6489 6490 6491 6492 6493 6494 6495 6496. 
This represents a relationship between the character id (the first number) and the publication id's (all other numbers.)
