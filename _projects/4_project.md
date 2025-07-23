---
layout: page
title: "Two's Company, Three's a Conspiracy"  
description: Dynamic Network Analysis of 2 Samuel
img:
importance: 3
category: work
---

#### Overview
A conversation network of a literary text is a graph with a node for each character, and an edge between any two characters with dialogue between them.  We can think of a conversation network as being static by modeling a fixed snapshot of the text, or dynamic, by modeling the data as a sequence of static networks that shows the evolution of the network over time.

This work analyzes the Hebrew text of 2 Samuel using a dynamic conversation network.  By treating a verse as a unit of “time”, we construct a sequence of static conversation networks G1, G2, …, Gt (one per verse), that shows the evolution of the interconnectivity of the characters. 

As the network unfolds over time, we observe a shift take place in the ~125 verses spanning 2 Sam 13-16.  Specifically, we observe (i) a threefold increase in the number of triangles in the network, which is characterized by (ii) a probability shift in the interconnectivity of David’s neighboring nodes (30% to 67%).      

Inspection of these new triangles reveals exactly three nodes with the following characteristics:

    (1) They are all new to the narrative
    (2) They have a degree of exactly 2
    (3) Have the same Katz centrality value

These characters are:  the Woman of Tekoa, Hushai, and Jonadab.  While the first two of these characters are known to have subversive designs, Jonadab’s intentions remain mysterious.  We explore how his structural isomorphism to these characters supports reading Jonadab similarly to how the Woman of Tekoa and Hushai are understood:  as conspirators.

The work constitutes a case study in the ways computational techniques can yield results that are interesting not only in their own right, but can also open new interpretive insights to biblical texts.

#### Data and Analysis 
The author constructed the data set by manually working through the Hebrew text and recording in a database all instances of dialogue between characters.  All computational work was done by the author using the Python programming language.

