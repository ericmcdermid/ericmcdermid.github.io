---
layout: page
title: The Tree of the Knowledge of Praise and Lament
description: Algorithmic Form Criticism and the Psalms
img:  
importance: 1
category: work
related_publications: false
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/decision_tree_1080_1080.png"  title="What distinguishes praise from lament?" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    We can distinguish praise from lament surprisingly well knowing only the density of parts of speech
</div>

### Overview  
Suppose you are given all the lament and praise psalms in the Psalter, but each Hebrew word has been replaced with its part of speech, and the original word ordering has been lost.  Could you still distinguish lament from praise psalms?  

It turns out that:

1. Yes you can!  And there are a few simple rules that distinguish lament from praise psalms with high accuracy even if only the distribution of parts of speech is known. 

2. We can discover these rules through classical machine learning techniques, which are easily understood by non-experts and human-verifiable.  

3.  This analysis exposes differences between these two types of psalms at the sub-semantic level.  Combined with a close exegetical reading of individual texts, this constitutes a form of algorithmic criticism, in which a distant reading of a corpus informs our close textual analysis.  We demonstrate how this approach guides our interpretation of Psalms 126 and 123.   

#### Method

We identified a set of 42 lament and 41 praise psalms from a general scholarly consensus in the literature.  Next, we used an open-source digital database hosted by the Eep Talstra Centre for Bible and Computer (ETCBC) at Vrije University called the Biblia Hebraica Stuttgartensia Amstelodamensis, which provides detailed annotations of the BHS (Biblia Hebraica Stuttgartensia).  One of the annotations is a part-of-speech tag that specifies each Hebrew word’s grammatical role in each verse.

Through a combination of Python, SQL, and the ETCBC database, we mapped each Psalm to its TF-IDF vector representation (with l2-normalization), where each component of the vector corresponds to a distinct part of speech (e.g., adjective, adverb, noun, etc.).  

Our next step is knowledge discovery:  how can we learn what distinguishes praises from laments in a comprehensible way?  To this end, we built a decision tree, a classical machine learning technique that yields human-readable rules.  It turns out that the tree is surprisingly simple and identifies two rules that yield ~80% accuracy in discriminating a lament from a praise psalm, simply based on the density of a few parts of speech.

#### Exegetical Significance 
While interesting in its own right, we show how this form of “distant reading” of a corpus can inform the way that we approach certain psalms.  Two examples are Psalms 126 and 123.  While most researchers identify the form of Psalm 126 as lament, there are some well-known scholars that have argued its form is praise.  Our decision tree sees this psalm as having a high probability of lament, providing a new piece of empirical, sub-semantic data to the debate.  Psalm 123 is an example of a psalm our tree gets wrong -- why?  The decision tree’s misclassification of Psalm 123, based on its unusually low verbal density, hones the reader's attention to the psalm’s extended ellipsis. Once foregrounded, this observation invites an ideological reading in which the absence of verbs mirrors the psalmist’s constrained agency, intensifying the depiction of distress through the silence of the speaker.

   