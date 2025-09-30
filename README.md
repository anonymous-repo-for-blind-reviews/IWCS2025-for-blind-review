<h1>Beyond Surface Metrics:
  Relation-Aware Typology of Rare-Term Loss in Political-Conflict Machine Translation</h1>
<p>
Machine translation (MT) in specialized domains often alters or omits rare and domain-specific terms. This may reduce terminological precision, depending on the nature of the change. Current MT quality metrics often overcount rare-term loss, since many are merely altered in form (e.g., spelling variants, acronym expansions) and thus cannot distinguish harmless changes from true semantic loss, and they also don't provide a detailed, term-level analysis of the type of loss.<br>
This paper presents a human-in-the-loop diagnostic framework that (i) extracts lemmas present in the reference text but absent from MT back-translated output (\textit{lost lemmas}), (ii) labels each for rarity and domain specificity, and (iii) assigns a relation to its counterpart using a seven-class typology.<br>
The study focuses on Spanish->English (ES->EN) and Arabic->English (AR->EN) United Nations Security Council translations across multiple MT engines. We find that the majority (80-83%) of rare-lemma “losses” are harmless form changes that preserve meaning. True semantic loss is smaller, concentrated in the lower-resource Arabic->English direction, while we distinguish effect that bias metrics from those that reflect true semantic changes.<br>
We release a seven-category typology, a manually annotated corpus, and accompanying code to support diagnostic analysis of rare/domain-specific term loss and distinguish genuine semantic loss from surface-equivalent changes. These annotations substantiate metric overcounting and detail how rare and domain-specific terms are transformed or omitted. Accordingly, this work offers a diagnostic, relation-aware framework with a typology and annotations that render these transformations visible and quantifiable.
</p>

Here is a brief description of the folders and their purpose. The internal structure of each folder is described in detail within its corresponding README.md file.
  
# Rare lemmas types, domain-specificity and manual annotations files
This folder contains the manual annotations dataset for the **semantic relationships**, the resources needed to replicate the results and the automatic portion of the annotation of the domain-specificity and rarity.
