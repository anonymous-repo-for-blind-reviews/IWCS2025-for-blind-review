<h1>Are They Truly Lost? Diagnosing and Mitigating Rare Term Loss in Domain-Specific Machine Translation </h1>
<p>
Machine translation (MT) in specialized domains often alters or omits rare and domain-specific terms, reducing semantic precision. Here, we present a framework to diagnose and address lexical loss by combining human annotation with automated tools. Drawing from the UN Parallel Corpus, our study identifies over 16,000 lost lemmas (4,503 unique) in MT outputs from Spanish and Arabic into English and categorizes them along three axes, namely, rarity, domain specificity, and semantic relationship to the replacement unit. Findings reveal that many losses result not from semantic gaps but from spelling variants, acronym expansions, or encoding issues, which mislead standard rarity metrics. We also propose LexDevEval, a new evaluation score to detect divergence. Needwise, our taxonomy informs targeted interventions. This work is grounded in human-in-the-loop analysis and offers a replicable path for domain-sensitive MT assessment. We highlight critical risks and show that vocabulary simplification is often misrepresented as information loss by current metrics.
</p>

<p>
  Here is a brief description of the folders, files and their purpose:
  <h2>Rare lemmas types, domain-specificity and manual annotations files</h2>
  The resources needed to replicate the results (the automatic portion of the annotation of the domain-specificity and rarity) and the file/s of the manual annotations.
  <h2>Lexical Divergence</h2>
  This folder contains the files for the implementation of a sentence-level evaluation metric designed to measure lexical divergence in machine-translated texts, particularly for political and humanitarian domains. It complements traditional MT metrics (e.g., BLEU, METEOR, BERTScore) by identifying whether domain-critical terms were preserved, omitted, or semantically drifted.
</p>
