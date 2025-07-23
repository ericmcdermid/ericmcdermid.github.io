---
layout: page
title: Stylistic Hotspots
description: How densities of stylistic features shape our interpretations
img: 
importance: 4
category: work
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/exodus_density.png"  title="Verb density" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Heatmap of a sliding verb-density window on the Hebrew text of Exodus
</div>

The Hebrew Bible is rich with stylistic literary features.  This project asks how we might use computation to detect textual "hotspots"
where the text is statistically dense with one or more such features.  Examples include:

- Anagrams or consonantal reversals
- Alliteration
- Sound play (similar niqqud patterns)
- Key word repetition
- Part of speech density
- Verb tense distribution

Imagine we chose one or more of these stylistic features, and slid a window of a fixed length k across the text of a given book, algorithmically computing the number of occurrences of the feature within the window.  Upon completion, we could make quantifiable statements such as "this window of text has more of 
feature X than 99.7% of all windows of similar length".

How might that then shape our interpretation?  As a proof-of-concept, I implemented this method on the Hebrew text of the book of Exodus, and simply scanned for 
verbal hotspots -- places where the text is overly dense with verbs.  One of the outlying sections is Exodus 2:X-Y, in which Moses kills a man, hides his body, flees to Midian, and waits by a well.  Might we say this portion of the text is kinetically charged and read it through a post-colonial lens:  despite his privileged upbringing in the house of Pharaoh, violence and unstructured action remain the only tools available to him.  Might it be seen as contrasting the later Moses who confronts Pharaoh with prophetic speech, or "Moses the lawgiver" at Sinai? 



